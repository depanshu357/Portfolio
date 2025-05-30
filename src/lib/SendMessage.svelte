<script>
  let name = '';
  let email = '';
  let topic = '';
  let message = '';

  const handleSubmit = () => {
    // Replace with actual email sending logic or API call
    alert(`Message sent!\nName: ${name}\nEmail: ${email}\nTopic: ${topic}\nMessage: ${message}`);
  };
</script>

<style>
  .contact-form {
    max-width: 600px;
    margin: auto;
    padding: 2rem;
    border-radius: 12px;
    background: #f9f9f9;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    font-family: 'Roboto', sans-serif;
  }

  input, textarea, select {
    width: 100%;
    padding: 0.75rem;
    margin: 0.5rem 0 1rem;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 1rem;
  }

input:focus,
textarea:focus,
select:focus {
  outline: none;
  box-shadow: none; /* optional: removes browser-specific shadows */
  border-color: #888; /* optional: customize border color on focus */
}

  button {
    background: #222;
    color: #fff;
    border: none;
    padding: 0.75rem 1.5rem;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
  }

  .social-links {
    display: flex;
    justify-content: space-around;
    margin-top: 1.5rem;
    flex-wrap: wrap;
  }

  .social-links a {
    text-decoration: none;
    color: #444;
    font-weight: 600;
    margin: 0.5rem;
  }

  .social-links a:hover {
    color: #000;
  }
</style>

<div class="recent-project">
  <p>Send me a message or connect via any of the links below — whether it’s to collaborate, brainstorm, ask for help, or just chat.</p>

  <form on:submit|preventDefault={handleSubmit}>
    <label for="name-input">Name</label>
    <input id="name-input" type="text" bind:value={name} required placeholder="Your name" />

    <label for="email-input">Email</label>
    <input id="email-input" type="email" bind:value={email} required placeholder="Your email" />

    <label for="topic-select">Topic</label>
    <select id="topic-select" bind:value={topic} required>
      <option value="" disabled>Select a topic</option>
      <option value="collaboration">Collaboration</option>
      <option value="ideas">Idea Discussion</option>
      <option value="career">Career Advice</option>
      <option value="general">General Inquiry</option>
    </select>

    <label for="message-input">Message</label>
    <textarea id="message-input" rows="5" bind:value={message} required placeholder="Write your message here..."></textarea>

    <button type="submit">Send Message</button>
  </form>

  <div class="social-links">
    <a href="mailto:your.email@example.com" target="_blank" rel="noopener noreferrer">
        <img src="/images/email.png" alt="Email" width="24" height="24" />
    </a>
    <a href="https://github.com/depanshu357" target="_blank" rel="noopener noreferrer">
        <img src="/images/github.png" alt="GitHub" width="24" height="24" />
    </a>
    <a href="https://www.linkedin.com/in/depanshu-sahu-429358230/" target="_blank" rel="noopener noreferrer">
        <img src="/images/linkedin.png" alt="LinkedIn" width="24" height="24" />
    </a>
    <a href="https://x.com/DepanshuSahu3" target="_blank" rel="noopener noreferrer">
        <img src="/images/x.png" alt="X (Twitter)" width="24" height="24" />
    </a>
  </div>
</div>
