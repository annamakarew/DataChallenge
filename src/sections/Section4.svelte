<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "column",
    },
    title: {
      text: "Officer-Initiated Stop Rate per 1,000 people",
    },
    plotOptions: {
      column: {
        pointPadding: 0.2,
        borderWidth: 0,
      },
    },
    xAxis: {
      categories: ["Black Residents", "All Residents"],
      crosshair: true,
    },
    series: [
      {
        name: "Officer-Initiated Stop Rate per 1,000 people",
        data: [333.3, 64.3],
        colorByPoint: true,
        colors: ["#2f7ed8", "#910000"],
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
      <p class="caption">
        Data from <a
          href="https://www.racecounts.org/county_races/el-dorado/?race=black"
          >here!</a
        >
      </p>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        Even in a county where Black residents make up less than 1% of the
        population, policing disparities are severe.
      </ArticleText>

      <ArticleText>
        In El Dorado County, law enforcement officers initiate stops of Black
        resdients at a rate of <strong>333.3 per 1,000 people</strong>, which is
        more than <strong>5 times the county-wide average</strong>.
      </ArticleText>

      <ArticleText>
        These disparities don't just reflect over-policing. They create a
        climate where Black residents feel surveilled, unsafe, and unwelcome.
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
  .tableauPlaceholder {
    width: 90%;
    margin: 0px auto;
  }
  .caption {
    text-align: center;
  }
</style>
