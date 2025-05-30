<script>
    import { projectType } from "../utils/state.svelte.js";
    import { onMount } from "svelte";
    
    onMount(() => {
        let projectTypeBox = document.querySelector('.project-list');
        let buttons = projectTypeBox.querySelectorAll('button');
        buttons.forEach(button => {
            button.addEventListener('click', () => {
                let type = button.getAttribute('name');
                projectType.type = type;
                // button.style.backgroundColor = 'rgba(113, 113, 113, 0.216)'
                buttons.forEach(e => e.classList.remove('selected'))
                button.classList.add('selected')
                // buttons.forEach(btn => btn.style.backgroundColor = '#f0f0f000');
                // button.style.backgroundColor = '#f0f0f0';
            });
        });
        buttons.forEach(button => {
            let type = button.getAttribute('name')
            if(type == projectType.type){
                button.classList.add('selected')
                // button.style.backgroundColor = 'rgba(113, 113, 113, 0.216)'
                // console.log("hone")
            }
        })
    });
</script>

<div class="project-list">
    <button name="self">Self Projects</button>
    <button name="professor">Projects under Professor</button>
    <button name="others">Others</button>
</div>

<style>
    .project-list{
        display: flex;
        flex-direction: column;
        gap: 10px;
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
        position: relative;
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
    }
    button:hover{
        background-color: rgba(113, 113, 113, 0.216);
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
    }
    
</style>