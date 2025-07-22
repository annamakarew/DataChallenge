<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "pie",
    },
    title: {
      text: "Racial Breakdown of El Dorado County",
    },
    plotOptions: {
      pie: {
        allowPointSelect: true,
        dataLabels: [
          {
            enabled: true,
            distance: 20,
          },
          {
            enabled: true,
            distance: -40,
            format: "{point.percentage:.1f}%",
            style: {
              fontSize: "1.2em",
              textOutline: "none",
            },
            filter: {
              operator: ">",
              property: "percentage",
              value: 10,
            },
          },
        ],
      },
    },
    series: [
      {
        name: "Count",
        data: [
          {
            name: "Asian",
            y: 10082,
          },
          {
            name: "Black",
            y: 1644,
            selected: true,
          },
          {
            name: "Hispanic",
            y: 27230,
          },
          {
            name: "White",
            y: 153632,
          },
        ],
      },
    ],
  };
</script>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
      <div>
        <p class="caption">
          Data is from <a
            href="https://public.tableau.com/shared/HT3M483BB?:display_count=n&:origin=viz_share_link&:embed=y"
            >here!</a
          >
        </p>
      </div>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        El Dorado County, nestled in the Sierra foothills, is known for it's
        natural beauty and Gold Rush history, but also has striking racial
        homogeneity.
      </ArticleText>

      <ArticleText>
        Only about 0.9% of El Dorado County residents are Black, and that's just
        over 1,600 people in a county of nearly 200,0000.
      </ArticleText>

      <ArticleText>
        In El Dorado County, the Black homeownership rate is 65.5%. At first
        glance, that might seem encouraging.
      </ArticleText>

      <ArticleText>
        However, that 65.5% comes from a very small population of just 1,600
        Black residents. With such a small sample, the number may be skewed by a
        handful of longtime homeowners.
        <br /> <br />
        It doesn't mean Black families are moving here. It means that very few ever
        have.
      </ArticleText>

      <ArticleText>
        Next, let's look at the income divide in El Dorado County.
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
  .chart {
    width: 90%;
    margin: 0px auto;
  }

  .caption {
    text-align: center;
  }

  .toggle-button {
    margin: 20px;
    padding: 20px;
    color: #007052;
    background-color: #0bd956;
    border: solid 2px #007052;
    border-radius: 16px;
    font-size: large;
    cursor: pointer;
    transition: all 0.2s ease;
    box-shadow: 0 4px 0 #007052;
  }

  .toggle-button:active {
    transform: translateY(2px);
    box-shadow: 0 2px 0 #007052;
  }
</style>
