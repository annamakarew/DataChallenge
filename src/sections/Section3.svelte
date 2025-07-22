<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "column",
      height: 600,
      width: 700,
      backgroundColor: "#f8f9fa",
    },
    title: {
      text: "Income Divide in El Dorado County",
    },
    plotOptions: {
      column: {
        pointPadding: 0.2,
        borderWidth: 0,
      },
    },
    xAxis: {
      categories: ["Median Income", "Black Median Income"],
      crosshair: true,
    },
    series: [
      {
        name: "Median Income",
        data: [106190, 46432],
        colorByPoint: true,
        colors: ["#2f7ed8", "#910000"],
      },
    ],
  };
</script>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
      <p class="caption">
        Data from <a
          href="https://public.tableau.com/shared/D3PB7ZTKY?:display_count=n&:origin=viz_share_link&:embed=y"
          >here!</a
        >
      </p>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        The median household income in El Dorado County is $106,190. <br />
        <br />
        For Black households, it's just $46,432.
        <br /> <br />
        That's less than <strong>half</strong> the income of the average household.
      </ArticleText>

      <ArticleText>
        This makes the 65.5% homeownership rate for Black residents feel a bit
        misleading.
        <br /><br />
        Income affects everything: loan approvals, down payments, monthly costs.
        And with such a low median income, homeownership is not broadly accessible.
        The 65.5% homeownership rate likely reflects a small group of longtime or
        higher-income homeowners, not widespread access.
      </ArticleText>

      <ArticleText>
        So even if the rate of homeownership among Black households is high, the <strong
          >barriers to entry are steep</strong
        >. The real question isn't how many Black residents own homes - it's
        <strong
          >why are there so few Black residents here to begin with,
        </strong>
        and <strong>why the economic playing field is so uneven</strong>.
      </ArticleText>

      <ArticleText>
        The racial makeup of El Dorado County, and who owns property here, is
        the result of long-standing policies and decisions, not chance.
      </ArticleText>
      <ArticleText>
        For much of the 20th century, Black families were legally excluded from
        buying homes in many parts of the county through racially restrictive
        rules. <a
          href="https://www.cbsnews.com/sacramento/news/whites-only-racist-home-ownership-rules-still-on-the-books-in-el-dorado-hills-community/"
          >Some of the rules were still put in writing as late as the 1950s.</a
        >
      </ArticleText>

      <ArticleText>
        In the 1940s and 1950s, Black families like the Monroe's and Burgess's
        owned property in Coloma until their land <a
          href="https://www.newyorker.com/news/dispatch/the-black-families-seeking-reparations-in-californias-gold-country"
          >was seized by the state to build a State Park.</a
        >
      </ArticleText>

      <ArticleText>
        That loss isn't just about land. It's about stability, wealth, and the
        right to belong. And while the tactics may have changed, Black residents
        in El Dorado County still face barriers to this day.
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
  .caption {
    text-align: center;
  }
</style>
