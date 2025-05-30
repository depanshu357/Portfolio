<script>
  import { state } from "../utils/state.svelte.js";

  function onContactClick() {
    state.variant = "contact";
    let rightBox = document.querySelector('.right-content')
    rightBox.classList.add('flex-4')
  }

  function onHomeClick() {
    state.variant = "default";
    let rightBox = document.querySelector('.right-content')
    rightBox.classList.remove('flex-4')
  }

  function onResumeClick() {
    window.open(
      "https://drive.google.com/file/d/1IH1mdSeYSNXpV2HDCLFHOwtzVCtGA8z0/view?usp=drive_link",
      "_blank"
    );
  }

  function onProjectClick() {
    onHomeClick();
    state.variant = "projects";    
    let rightBox = document.querySelector('.right-content')
    rightBox.classList.add('flex-4')
  }
</script>

<nav class="nav">
  <div class="name">Depanshu Sahu</div>
  <div class="options">
    <section class="open-icon">
      <span></span>
      <span></span>
      <span></span>
    </section>
    <section class="default-options">
      <button class="option" onclick={onHomeClick}>Home</button>
      <button class="option">About</button>
      <button class="option" onclick={onProjectClick}>Projects</button>
      <button class="option" onclick={onContactClick}
        >Contact</button
      >
      <button class="option" onclick={onResumeClick}>Resume</button>
    </section>
  </div>
</nav>

<style>
  button {
    /* remove all button style */
    border: 0;
    background: none;
    cursor: pointer;
  }
</style>
