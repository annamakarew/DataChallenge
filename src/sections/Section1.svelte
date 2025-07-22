<script>
  import "highcharts/modules/exporting";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div
        class="tableauPlaceholder"
        id="viz1753147230053"
        style="position: relative"
      >
        <noscript
          ><a
            href="https:&#47;&#47;blackwealthdata.org&#47;explore&#47;homeownership"
            ><img
              alt="Time Series "
              src="https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;JM&#47;JMK5FXMCN&#47;1_rss.png"
              style="border: none"
            /></a
          ></noscript
        ><object
          class="tableauViz"
          style="display:none;"
          aria-label="Median Property Value by Race"
          ><param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F" />
          <param name="embed_code_version" value="3" />
          <param name="path" value="shared&#47;JMK5FXMCN" />
          <param name="toolbar" value="yes" /><param
            name="static_image"
            value="https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;JM&#47;JMK5FXMCN&#47;1.png"
          /> <param name="animate_transition" value="yes" /><param
            name="display_static_image"
            value="yes"
          /><param name="display_spinner" value="yes" /><param
            name="display_overlay"
            value="yes"
          /><param name="display_count" value="yes" /><param
            name="language"
            value="en-US"
          /><param name="origin" value="viz_share_link" /><param
            name="filter"
            value="padding=0"
          /><param name="filter" value="position=relative" /></object
        >
      </div>
      <script type="text/javascript">
        var divElement = document.getElementById("viz1753147230053");
        var vizElement = divElement.getElementsByTagName("object")[0];
        vizElement.style.width = "1244px";
        vizElement.style.height = "727px";
        var scriptElement = document.createElement("script");
        scriptElement.src =
          "https://public.tableau.com/javascripts/api/viz_v1.js";
        vizElement.parentNode.insertBefore(scriptElement, vizElement);
      </script>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        <strong
          >Homeownership is one of the most powerful tools for building
          generational welath in the United States, but not all communities have
          equal access.</strong
        >
      </ArticleText>

      <ArticleText>
        Let's take a look at property values, which is a key driver of long-term
        wealth through home equity.
      </ArticleText>

      <ArticleText>
        Homes purchased by Black borrowers are valued lower than those purchased
        by other races.
      </ArticleText>

      <ArticleText>
        Lower property values mean less home equity over time, smaller returns
        on investment, and less intergenerational wealth.
      </ArticleText>

      <ArticleText>
        Black homeowners often start with less and earn less from their homes,
        which makes it harder to move, reinvest, or build finanical security.
      </ArticleText>

      <ArticleText>
        Now that we've seen the national trend, let's zoom in on what this looks
        like in El Dorado County, California.
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
  .tableauPlaceholder {
    width: 90%;
    margin: 0px auto;
  }
</style>
