<script>
  const name = 'Karla Berumen';
  const role = 'Software Developer';

  const interests = ['Kotlin', 'Java', 'Ktor', 'Unity', 'Python', 'SQL'];

  const links = [
    {
      label: 'LinkedIn',
      description: 'Professional profile',
      href: 'https://www.linkedin.com/in/karlaberumen',
      icon: 'linkedin'
    },
    {
      label: 'GitHub',
      description: 'Projects and code',
      href: 'https://github.com/Ka7suk0',
      icon: 'github'
    },
    {
      label: 'Download CV',
      description: 'Resume · PDF',
      href: '/cv.pdf',
      icon: 'file'
    },
    {
      label: 'Email',
      description: 'Get in touch',
      href: 'mailto:karla.berumen.0709@gmail.com',
      icon: 'mail'
    }
  ];
</script>

<svelte:head>
  <title>{name} — {role}</title>
</svelte:head>

<main class="page">
  <article class="profile-card">
    <header class="profile-header">
      <img
              class="avatar"
              src={`${import.meta.env.BASE_URL}profile.jpg`}
              alt=""
      />

      <h1>{name}</h1>
      <p class="role">{role}</p>
      <p class="location">Mexico <span>·</span> Software Engineering <span>·</span> Game Development</p>
    </header>

    <div class="section">
      <div class="section-heading">
        <h2>Professional Profile</h2>
        <span class="language-tag">English</span>
      </div>
      <p class="profile-description">
        Software developer interested in software architecture, backend engineering,
        cross-platform applications and game development.
      </p>
    </div>

    <div class="section">
      <h2>Technical Interests</h2>
      <div class="tags" aria-label="Technical interests">
        {#each interests as interest}
          <span class="tag">{interest}</span>
        {/each}
      </div>
    </div>

    <nav class="links" aria-label="Contact and portfolio links">
      {#each links as link}
        <a
          class="link-card"
          href={link.href}
          target={link.icon === 'mail' ? undefined : '_blank'}
          rel={link.icon === 'mail' ? undefined : 'noreferrer'}
        >
          <span class="link-icon" aria-hidden="true">
            {#if link.icon === 'linkedin'}
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M5.2 3.5a2.2 2.2 0 1 0 0 4.4 2.2 2.2 0 0 0 0-4.4ZM3.4 9.5H7v11H3.4v-11Zm5.8 0h3.4V11h.1c.5-.9 1.6-1.9 3.4-1.9 3.6 0 4.3 2.3 4.3 5.2v6.2h-3.6V15c0-1.3 0-3-1.9-3s-2.2 1.4-2.2 2.9v5.6H9.2v-11Z"/>
              </svg>
            {:else if link.icon === 'github'}
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 .9a11.1 11.1 0 0 0-3.5 21.6c.6.1.8-.3.8-.6v-2.1c-3.2.7-3.9-1.4-3.9-1.4-.5-1.3-1.3-1.6-1.3-1.6-1-.7.1-.7.1-.7 1.1.1 1.7 1.1 1.7 1.1 1 .1.8 2.1 3.4 1.5.1-.7.4-1.2.7-1.5-2.6-.3-5.3-1.3-5.3-5.8 0-1.3.5-2.3 1.2-3.1-.1-.3-.5-1.5.1-3.1 0 0 1-.3 3.2 1.2a11 11 0 0 1 5.8 0c2.2-1.5 3.2-1.2 3.2-1.2.6 1.6.2 2.8.1 3.1.8.8 1.2 1.8 1.2 3.1 0 4.5-2.7 5.5-5.3 5.8.4.3.8 1 .8 2v3c0 .3.2.7.8.6A11.1 11.1 0 0 0 12 .9Z"/>
              </svg>
            {:else if link.icon === 'file'}
              <svg
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="1.6"
                      stroke-linecap="round"
                      stroke-linejoin="round"
              >
                <path d="M7 2.8h7l4.5 4.5v13.9H7a2 2 0 0 1-2-2V4.8a2 2 0 0 1 2-2Z"/>
                <path d="M14 2.8v4.8h4.5M8.5 13h7M8.5 16.5h7"/>
              </svg>
            {:else}
              <svg
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="1.6"
                      stroke-linecap="round"
                      stroke-linejoin="round"
              >
                <rect x="3" y="5" width="18" height="14" rx="2"/>
                <path d="m4 7 8 6 8-6"/>
              </svg>
            {/if}
          </span>
          <span class="link-copy">
            <strong>{link.label}</strong>
            <small>{link.description}</small>
          </span>
          <svg class="external-icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <path d="M14 4h6v6M20 4l-9 9"/>
            <path d="M18 13v5a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h5"/>
          </svg>
        </a>
      {/each}
    </nav>
  </article>
</main>