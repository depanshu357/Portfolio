<script>
    import { projectType } from "../utils/state.svelte.js";
    import { onMount } from "svelte";
    
    onMount(() => {
        let projectTypeBox = document.querySelector('.project-list');
        console.log(projectTypeBox);
        let buttons = projectTypeBox.querySelectorAll('button');
        buttons.forEach(button => {
            button.addEventListener('click', () => {
                let type = button.getAttribute('name');
                projectType.type = type;
                // buttons.forEach(btn => btn.style.backgroundColor = '#f0f0f000');
                // button.style.backgroundColor = '#f0f0f0';
            });
        });
    });
</script>

<div class="project-list">
    <button name="company">Projects under Companies</button>
    <button name="self">Self Projects</button>
    <button name="professor">Projects under Professor</button>
</div>

<style>
    .project-list{
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    .project-list div {
        padding: 10px;
        border-radius: 5px;
        font-size: 16px;
        font-weight: bold;
    }
    button{
        padding: 10px;
        font-size: 16px;
        font-weight: bold;
        background-color: #f0f0f000;
        border: none;
        cursor: pointer;
        text-align: left;
        border-bottom: 2px solid black;
    }
</style>