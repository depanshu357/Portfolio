<script>
  import Nav from "./lib/Nav.svelte";
  import Status from "./lib/Status.svelte";
  import Dp from "./lib/Dp.svelte";
  import About from "./lib/About.svelte";
  import Contact from "./lib/Contact.svelte";
  import Description from "./lib/Description.svelte";
  import Socials from "./lib/Socilas.svelte";

  import { state, projectType } from "./utils/state.svelte.js";
  import ClickedContact from "./lib/ClickedContact.svelte";
  import SendMessage from "./lib/SendMessage.svelte";
  import ProjectType from "./lib/ProjectType.svelte";
  import ProjectDescriptions from "./lib/ProjectDescriptions.svelte";
</script>

<main class="main">
  <Nav />
  <main class="content">
    <section class="left-content">
      {#if state.variant === "default"}
        <div class="left-top-content">
          <Status />
          <Dp />
        </div>
        <div class="left-bottom-content">
          <About />
          <Contact />
        </div>
      {:else if state.variant === "contact"}
        <div>
          <ClickedContact />
        </div>
      {:else if state.variant === "projects"}
      <div>
        <ProjectType />
      </div>
      {/if}
    </section>
    <section class="right-content">
      {#if state.variant === "default"}
        <Description />
        <Socials />
      {:else if state.variant === "contact"}
        <SendMessage />
      {:else if state.variant === "projects"}
        <ProjectDescriptions />
      {/if}
    </section>
  </main>
</main>
