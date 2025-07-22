<script>
  import Section1 from "./sections/Section2.svelte";
  import Section2 from "./sections/Section1.svelte";
  import Section3 from "./sections/Section3.svelte";
  import Section4 from "./sections/Section4.svelte";
  import TitleSection from "./sections/TitleSection.svelte";
  import InteresectionObserverBasicExample from "./sections/InteresectionObserverBasicExample.svelte";
  import IntersectionObserverAlertExample from "./sections/IntersectionObserverAlertExample.svelte";
  import DisappearingDuckExample from "./sections/DisappearingDuckExample.svelte";
  import IntersectionObserverSectionCard from "./sections/IntersectionObserverSectionCard.svelte";
  import IntersectionObserverListExample from "./sections/IntersectionObserverListExample.svelte";
</script>

<main>
  <TitleSection />
  <Section2 />
  <Section1 />
  <Section3 />
  <Section4 />

  <IntersectionObserverSectionCard />
  <InteresectionObserverBasicExample />
  <IntersectionObserverAlertExample />
  <DisappearingDuckExample />
  <IntersectionObserverListExample />
</main>
