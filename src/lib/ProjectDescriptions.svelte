<script>
  import arrow from "../assets/images/arrow.png";
  let ProjectList = [
    {
      type: "self",
      title: "SIP Portal",
      description: `Developed an open-source internship application portal for IIT
              Kanpur's Startup Internship Program. Implemented authentication
              with Auth.js, email verification, and deployed on Red Hat Linux
              using Nginx. Designed the UI with Shadcn and Tailwind CSS,
              ensuring type safety with TypeScript and enabling file
              upload/download functionalities.`,
      link: "https://github.com/depanshu357/SIP-Portal-Backend",
      image: "./images/projects/sip_portal.png",
      tags: [
        "Web Development",
        "JavaScript",
        "Node.js",
        "TypeScript",
        "Tailwind CSS",
        "Shadcn",
        "Nginx",
        "Red Hat Linux",
      ],
    },
    {
      type: "self",
      title: "Scribble Board Hackathon Project",
      description:
        "Developed an interactive scribble board web app using Fabric.js. Implemented drawing and erasing functionalities with advanced support for shapes, brush types, inks, colors, and shape resizing. Integrated ResNet-34 for image processing and shape classification to enable shape autocompletion.",
      link: "https://github.com/depanshu357/PClub-PS2",
      image: "./images/projects/scribble_board.png",
      tags: [
        "Fabric.js",
        "ResNet-34",
        "Image Processing",
        "Deep Learning",
        "Shape Classification",
        "Hackathon",
        "Interactive UI",
        "JavaScript",
        "Web App",
      ],
    },
    {
      type: "professor",
      title: "Compiler for Python Course Project, CS335",
      description:
        "Developed a compiler for Python using Flex and Bison. Parsed Python code and implemented grammar with syntax analysis. Generated Abstract Syntax Tree (AST), Three Address Code (3AC), and symbol table using Syntax Directed Definitions. Enabled x86 assembly code generation with support for recursion, constructors, and type checking through semantic analysis.",
      link: "https://github.com/depanshu357/CS335-Compiler",
      image: "./images/projects/python_compiler.png",
      tags: [
        "Compiler Design",
        "Flex",
        "Bison",
        "Python",
        "AST",
        "3AC",
        "Semantic Analysis",
        "x86 Assembly",
        "Recursion",
        "Course Project",
      ],
    },
    {
      type: "professor",
      title: "CSE Bubble Course Project, CS220",
      description:
        "Created a custom processor with 32 registers, inspired by the MIPS-32 Instruction Set Architecture. Designed a finite state machine to manage control signals for executing each instruction within a single clock cycle. Implemented an Arithmetic Logic Unit (ALU) using a top-down modular approach to support a range of instructions.",
      link: "https://github.com/depanshu357/CSE-Bubble",
      image: "./images/projects/cse_bubble.png",
      tags: [
        "Processor Design",
        "MIPS-32",
        "FSM",
        "ALU",
        "Hardware Architecture",
        "Digital Design",
        "Top-Down Design",
        "CS220",
        "Course Project",
      ],
    },
    {
      type: "professor",
      title: "TrackIT - CS253 Software Development and Operations",
      description:
        "Collaborated in a team of 10 to develop a web application for tracking user expenses and borrowings. Built the backend logic and data integration between user and shopkeeper using the MERN stack. Contributed to software process formalization by preparing documentation and defining project timelines.",
      link: "https://github.com/depanshu357/TrackIT",
      image: "./images/projects/trackit.png",
      tags: [
        "MERN Stack",
        "Expense Tracking",
        "Team Project",
        "Backend Development",
        "Software Engineering",
        "Project Planning",
        "CS253",
        "Web App",
        "MongoDB",
        "React",
        "Node.js",
      ],
    },
    {
  "type": "others",
  "title": "Youth Entrepreneurship Challenge (YEC) Website",
  "description": "Developed the official website for the Youth Entrepreneurship Challenge (YEC) organized by the Entrepreneurship Cell at IIT Kanpur. Utilized HTML, CSS, and JavaScript to create an interactive and responsive platform that provides information about the challenge, timelines, incentives, and registration details. Implemented smooth animations and transitions to enhance user engagement and experience.",
  "link": "https://www.ecelliitk.org/YEC/",
  "image": "./images/projects/yec_website.png",
  "tags": [
    "HTML",
    "CSS",
    "JavaScript",
    "Web Development",
    "Responsive Design",
    "Animations",
    "Youth Entrepreneurship Challenge",
    "IIT Kanpur",
    "E-Cell"
  ]
},
{
  "type": "others",
  "title": "E-Summit'23 Website – Inquisition of Infinity",
  "description": "Developed the official website for E-Summit'23, the flagship event of the Entrepreneurship Cell at IIT Kanpur, themed 'Inquisition of Infinity'. Utilized HTML, CSS, and JavaScript to craft a responsive and engaging platform. Integrated GSAP (GreenSock Animation Platform) to implement smooth, scroll-triggered animations, enhancing user interaction and visual appeal.",
  "link": "https://www.ecelliitk.org/esummit-23/index.html",
  "image": "./images/projects/esummit23.png",
  "tags": [
    "HTML",
    "CSS",
    "JavaScript",
    "GSAP",
    "Web Animations",
    "Responsive Design",
    "Event Website",
    "E-Summit",
    "IIT Kanpur",
    "E-Cell"
  ]
}


  ];
  import { projectType } from "../utils/state.svelte";
</script>

<div
  class="recent-project"
  style="overflow-y: scroll;max-height: calc(100vh - 80px);"
>
  {#each ProjectList as project, i (i)}
    {#if projectType.type == project.type}
      <div class="project-item">
        <h3 class="project-title">
          {project.title}
          <a href={project.link} target="_blank"
            ><img src={arrow} alt="arrow" width="20px" /></a
          >
        </h3>
        <img src={project.image} alt={project.title} class="project-image" />
        <p class="project-description">{project.description}</p>
        <div class="skill-box">
          {#each project.tags as tag}
            <span class="tag">{tag}</span>
          {/each}
        </div>
      </div>
    {/if}
  {/each}
</div>

<style>
  .project-image {
    max-width: 500px;
    margin: 0 auto;
    border-radius: 12px;
    display: block;
  }
  .project-title {
    display: flex;
    align-items: center;
    gap: 4px;
  }
  .project-item {
    display: flex;
    flex-direction: column;
    gap: 12px;
    border-bottom: 2px solid black;
    padding-bottom: 8px;
  }
</style>
