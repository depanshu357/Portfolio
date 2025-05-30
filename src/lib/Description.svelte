<script>
    import arrow from '../assets/images/arrow.png';
    import recentProject from '../assets/images/projects/sip_portal.png';
</script>
<div class="recent-project">
          <section
            style="
              display: flex;
              justify-content: space-between;
              align-items: center;
            "
          >
            <span style="font-weight: 500">Recent Project</span>
            <span
              ><img src={arrow} alt="arrow" width="24px"
            /></span>
          </section>

          <div>
            <img
              src={recentProject}
              alt="sip_portal"
              width="100%"
              style="border-radius: 12px"
            />
          </div>
          <div class="project-descripiton">
            <div
              style="
                display: flex;
                flex-direction: row;
                justify-content: space-between;
              "
            >
              <span style="font-weight: bold">SIP Portal </span>
              <span
                style="
                  display: flex;
                  align-items: center;
                  border: 2px solid black;
                  border-radius: 8px;
                  padding: 2px 4px;
                "
                ><a href="https://sipp.iitk.ac.in/sign-in" target="_blank"
                  >Live Demo</a
                ></span
              >
            </div>
            <div>
              Developed an open-source internship application portal for IIT
              Kanpur's Startup Internship Program. Implemented authentication
              with Auth.js, email verification, and deployed on Red Hat Linux
              using Nginx. Designed the UI with Shadcn and Tailwind CSS,
              ensuring type safety with TypeScript and enabling file
              upload/download functionalities.
            </div>
            <div class="skill-box">
              <span>Next.js</span>
              <span>Golang</span>
              <span>PostgreSQL</span>
              <span>nginx</span>
              <span>Red-Hat</span>
            </div>
          </div>
        </div>