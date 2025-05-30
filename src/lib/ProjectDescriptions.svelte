<script> 
    let ProjectList = [
        {
            type: "self",
            title: "SIP Portal",
            description: "A web application for managing student internship programs, including application tracking and communication.",
            link: "",
            image: "./images/projects/sip_portal.png",
            tags: ["Web Development", "JavaScript", "Node.js"]
        }
    ]
    import { projectType } from "../utils/state.svelte";
</script>

<div class="recent-project">
 {#each ProjectList as project, i (i)}
    {#if projectType.type == project.type}
    <div class="project-item">
        <img src={project.image} alt={project.title} class="project-image" />
        <h3 class="project-title">{project.title}</h3>
        <p class="project-description">{project.description}</p>
        <div class="skill-box">
            {#each project.tags as tag}
                <span class="tag">{tag}</span>
            {/each}
        </div>
        {#if project.link}
            <a href={project.link} target="_blank" rel="noopener noreferrer" class="project-link">View Project</a>
        {/if}
    </div>
    {/if}
 {/each}
</div>

<style>
    .project-image{
        max-width: 500px;
        margin: 0 auto;
        border-radius: 12px;
        display: block;
    }
</style>