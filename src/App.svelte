<script>
  import Nav from "./lib/Nav.svelte";
  import Status from "./lib/Status.svelte";
  import Dp from "./lib/Dp.svelte";
  import About from "./lib/About.svelte";
  import Contact from "./lib/Contact.svelte";
  import Description from "./lib/Description.svelte";
  import Socials from "./lib/Socials.svelte";

  import { state, projectType } from "./utils/state.svelte.js";
  import ClickedContact from "./lib/ClickedContact.svelte";
  import SendMessage from "./lib/SendMessage.svelte";
  import ProjectType from "./lib/ProjectType.svelte";
  import ProjectDescriptions from "./lib/ProjectDescriptions.svelte";
  import ClickedAbout from "./lib/ClickedAbout.svelte";
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
      {:else if state.variant === "about"}
      <div style="flex: 1; display: flex;">
        <Status />
      </div>
      <div style="flex: 8; display: flex;">
        <About />
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
      {:else if state.variant === "about"}
        <ClickedAbout />
      {/if}
    </section>
  </main>
</main>
