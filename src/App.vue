<script setup>
import { computed, ref } from 'vue'

const skillGroups = [
  {
    title: 'Frontend',
    items: [
      'JavaScript',
      'JSX',
      'DOM Manipulation',
      'Responsive Design',
      'Component Thinking',
      'Debugging'
    ]
  },
  {
    title: 'HTML & CSS',
    items: [
      'HTML5',
      'Semantic HTML',
      'CSS3',
      'Flexbox',
      'Grid',
      'Transitions',
      'Layout & Design'
    ]
  },
  {
    title: 'Vue.js',
    items: [
      'Vue 3',
      'Vue Router',
      'Vuex',
      'Components',
      'Props & Events',
      'Vite'
    ]
  },
  {
    title: 'Backend',
    items: [
      'Python',
      'Node.js',
      'REST APIs',
      'JSON',
      'SQL Basics',
      'Databases',
      'Authentication Basics',
      'Postman'
    ]
  },
  {
    title: 'Design',
    items: [
      'Creative Design',
      'Colour & Typography',
      'Visual Layout',
      'Attention to Detail'
    ]
  },
  {
    title: 'Tools',
    items: [
      'Git',
      'GitHub',
      'VS Code',
      'npm',
      'Chrome DevTools',
      'Microsoft Office'
    ]
  },
  {
    title: 'Soft Skills',
    items: [
      'Communication',
      'Teamwork',
      'Research',
      'Time Management',
      'Problem Solving',
      'Willingness to Learn'
    ]
  }
]

const projects = [
  {
    title: 'CampusSwap SA',
    description:
      'A student marketplace platform built as a group project. I built the Academic Marketplace page.',
    tech: ['Vue.js', 'Vue Router', 'Vuex'],
    link: 'https://campusswap-fontend.onrender.com'
  },
  {
    title: 'HTML & CSS Showcase',
    description:
      'A website that shows my HTML and CSS skills through clean layouts and thoughtful design.',
    tech: ['HTML', 'CSS', 'Vue.js'],
    link: 'https://html-css-showcase.onrender.com/',
    github: 'https://github.com/Zaarah-Okkers/HTML-CSS-Showcase'
  },
  {
    title: 'Python Mini Toolkit',
    description:
      'A beginner-friendly, menu-based Python program with a Study Planner and a Daily Motivation Generator.',
    tech: ['Python'],
    github: 'https://github.com/Zaarah-Okkers/Python-Mini-Toolkit'
  }
]

const filters = ['All', 'Vue.js', 'HTML', 'CSS', 'Python']
const activeFilter = ref('All')

const visibleProjects = computed(() => {
  if (activeFilter.value === 'All') return projects
  return projects.filter((project) => project.tech.includes(activeFilter.value))
})

const strengths = [
  {
    title: 'I learn fast',
    text: 'I went from my first HTML pages in 2022 to building Vue.js applications, and I keep adding new tools to my toolkit.'
  },
  {
    title: 'I work well in a team',
    text: 'I contributed to the CampusSwap SA group project, where I owned the Academic Marketplace page, and I collaborated in group sessions during my technology programme.'
  },
  {
    title: 'I am reliable',
    text: 'I completed a structured programme from February to September 2025 and deliver my work live, so you can see it running.'
  },
  {
    title: 'I care about design',
    text: 'I pay attention to how a site looks as well as how it works, with clean layouts, consistent colour and responsive pages.'
  }
]

const journey = [
  {
    when: '2022',
    title: 'Started learning to code',
    text: 'I began with HTML, CSS and JavaScript, driven by curiosity about how websites are built.'
  },
  {
    when: 'Dec 2024',
    title: 'Job shadowing at The Gemini Solution',
    text: 'I observed developers writing, testing and reviewing code, and gained exposure to real software workflows.'
  },
  {
    when: '2025',
    title: 'Gender Rights in Technology programme',
    text: 'I built research, communication and presentation skills, and learned about digital safety and responsible technology use.'
  },
  {
    when: '2025',
    title: 'National Senior Certificate',
    text: 'I completed Grade 12, including Computer Applications Technology.'
  },
  {
    when: 'Feb 2026',
    title: 'Built my first website from scratch',
    text: 'I applied HTML and problem-solving skills to design and structure my own pages.'
  },
  {
    when: 'Now',
    title: 'Building with Vue.js',
    text: 'I am working on full-stack projects, including the CampusSwap SA team project and this portfolio.'
  }
]
</script>

<template>
  <header class="nav">
    <span class="logo">Zaarah Okkers</span>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#why">Why Me</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section class="hero">
      <span class="deco deco-dots" aria-hidden="true"></span>
      <span class="deco deco-stripes" aria-hidden="true"></span>
      <span class="deco deco-stripes-peach" aria-hidden="true"></span>
      <span class="deco deco-square" aria-hidden="true"></span>
      <span class="deco deco-square-dark" aria-hidden="true"></span>

      <div class="hero-text">
        <p class="intro">Hello, I'm</p>
        <h1>Zaarah Okkers</h1>
        <p class="role">Junior Web Developer</p>
        <p class="tagline">
          I build clean, responsive websites with Vue.js, based in Cape Town.
        </p>
      </div>
    </section>

    <section id="about" class="about">
      <div class="about-content">
        <div class="about-media">
          <div class="photo-frame">
            <span class="photo-tag" aria-hidden="true">&lt;/&gt;</span>
            <img
              class="about-photo"
              src="/9e1adbde-3d5a-e986-35cb-a8939642a81e.jpg"
              alt="Portrait of Zaarah Okkers"
            />
            <span class="photo-bar" aria-hidden="true"></span>
          </div>
          <div class="about-social">
            <a
              href="https://www.linkedin.com/in/zaarah-okkers-3688b1377/"
              target="_blank"
              rel="noopener"
              aria-label="LinkedIn"
            >
              in
            </a>
            <a
              href="https://github.com/Zaarah-Okkers"
              target="_blank"
              rel="noopener"
              aria-label="GitHub"
            >
              GH
            </a>
            <a href="mailto:zaarahokkers7@gmail.com" aria-label="Email">@</a>
          </div>
        </div>

        <div class="about-body">
          <h2 class="about-heading"><span>About</span> Me.</h2>
          <div class="about-text">
            <p>
              I am a junior web developer based in Cape Town, with a strong
              interest in creativity and design. I began learning to code in
              2022 and have since built a solid foundation in web development.
            </p>
            <p>
              My interest in coding began with curiosity about how websites are
              built and how they function. Through my work with HTML, CSS and
              JavaScript, I have come to appreciate the possibilities of
              creating attractive and functional websites.
            </p>
            <p>
              Outside of coding, I enjoy reading, art and design. I believe that
              creativity is central to web development, and I aim to bring a
              considered, artistic approach to every project I undertake.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="skills" class="skills">
      <h2>Skills</h2>
      <div class="skill-grid">
        <div v-for="group in skillGroups" :key="group.title" class="skill-card">
          <h3>{{ group.title }}</h3>
          <ul>
            <li v-for="item in group.items" :key="item">{{ item }}</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="projects" class="projects">
      <h2>Projects</h2>

      <div class="filter-bar" role="group" aria-label="Filter projects">
        <button
          v-for="filter in filters"
          :key="filter"
          type="button"
          class="filter-button"
          :class="{ active: activeFilter === filter }"
          :aria-pressed="activeFilter === filter"
          @click="activeFilter = filter"
        >
          {{ filter }}
        </button>
      </div>

      <TransitionGroup name="project" tag="div" class="project-grid">
        <article
          v-for="project in visibleProjects"
          :key="project.title"
          class="project"
        >
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <ul class="tech">
            <li v-for="item in project.tech" :key="item">{{ item }}</li>
          </ul>
          <div v-if="project.link || project.github" class="project-links">
            <a
              v-if="project.link"
              class="project-link"
              :href="project.link"
              target="_blank"
              rel="noopener"
            >
              View project
            </a>
            <a
              v-if="project.github"
              class="project-link"
              :href="project.github"
              target="_blank"
              rel="noopener"
            >
              View code
            </a>
          </div>
        </article>
      </TransitionGroup>
    </section>

    <section id="why" class="why">
      <h2>Why Work With Me</h2>
      <p class="why-intro">
        A quick look at what I bring to a team, and how I got here.
      </p>

      <div class="strength-grid">
        <div v-for="item in strengths" :key="item.title" class="strength-card">
          <h3>{{ item.title }}</h3>
          <p>{{ item.text }}</p>
        </div>
      </div>

      <h3 class="journey-heading">My Journey</h3>
      <ol class="journey">
        <li v-for="step in journey" :key="step.title" class="journey-item">
          <span class="journey-when">{{ step.when }}</span>
          <h4>{{ step.title }}</h4>
          <p>{{ step.text }}</p>
        </li>
      </ol>
    </section>

    <section id="contact" class="contact">
      <h2>Contact</h2>
      <p>I'm open to junior developer opportunities. Let's talk.</p>
      <div class="actions">
        <a class="button" href="mailto:zaarahokkers7@gmail.com">Get in touch</a>
        <a class="button button-outline" href="/Zaarah-Okkers-CV.pdf" download>
          Download CV
        </a>
      </div>
      <div class="social">
        <a
          href="https://www.linkedin.com/in/zaarah-okkers-3688b1377/"
          target="_blank"
          rel="noopener"
        >
          LinkedIn
        </a>
        <a
          href="https://github.com/Zaarah-Okkers"
          target="_blank"
          rel="noopener"
        >
          GitHub
        </a>
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Zaarah Okkers</p>
  </footer>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Barlow:wght@400;500;600;700&family=Barlow+Condensed:wght@700&display=swap');

:root {
  --cream: #e8e3cf;
  --cream-dark: #dcd6bd;
  --olive: #5b594a;
  --olive-dark: #4a483c;
  --sage: #a2a38d;
  --stripe: #8b9680;
  --peach: #b79a86;
  --peach-dark: #8a6650;
  --text: #4a483c;
  --text-soft: #625f50;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: 'Barlow', system-ui, -apple-system, 'Segoe UI', sans-serif;
  background: var(--cream);
  color: var(--text);
  -webkit-font-smoothing: antialiased;
}

a:focus-visible,
button:focus-visible {
  outline: 2px solid var(--peach-dark);
  outline-offset: 3px;
}

/* ---------- Navigation ---------- */

.nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 10%;
  background: rgba(232, 227, 207, 0.92);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  border-bottom: 1px solid var(--cream-dark);
  z-index: 10;
}

.logo {
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: var(--olive-dark);
}

.nav nav {
  display: flex;
  gap: 1.75rem;
}

.nav a {
  color: var(--text-soft);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
  transition: color 0.2s;
}

.nav a:hover {
  color: var(--peach-dark);
}

section {
  padding: 0 10%;
  scroll-margin-top: 4rem;
}

/* ---------- Decorative shapes ---------- */

.deco {
  position: absolute;
  pointer-events: none;
}

.deco-dots {
  width: 130px;
  height: 70px;
  background-image: radial-gradient(var(--peach) 3px, transparent 3.5px);
  background-size: 16px 16px;
}

.deco-stripes {
  border-radius: 50%;
  background: repeating-linear-gradient(
    135deg,
    var(--stripe) 0 10px,
    var(--cream) 10px 20px
  );
}

.deco-stripes-peach {
  border-radius: 50%;
  background: repeating-linear-gradient(
    135deg,
    var(--peach) 0 10px,
    var(--cream) 10px 20px
  );
}

.deco-square {
  background: var(--cream);
}

.deco-square-dark {
  background: var(--olive-dark);
}

/* ---------- Hero ---------- */

.hero {
  position: relative;
  overflow: hidden;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: var(--olive);
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  width: 68%;
  background: var(--cream);
  border-radius: 0 60% 30% 0 / 0 50% 40% 0;
}

.hero-text {
  position: relative;
  z-index: 1;
  max-width: 560px;
}

.hero .deco-dots {
  top: 18%;
  right: 12%;
}

.hero .deco-stripes {
  width: 280px;
  height: 280px;
  right: 14%;
  bottom: 8%;
}

.hero .deco-stripes-peach {
  width: 220px;
  height: 220px;
  left: 14%;
  bottom: -90px;
  opacity: 0.9;
}

.hero .deco-square {
  width: 36px;
  height: 36px;
  right: 4%;
  bottom: 6%;
}

.hero .deco-square-dark {
  width: 42px;
  height: 42px;
  left: 0;
  bottom: 16%;
}

.intro {
  margin: 0;
  color: var(--text-soft);
  font-size: 1.15rem;
  font-weight: 500;
}

h1 {
  margin: 0.5rem 0;
  font-size: clamp(2.4rem, 6vw, 4.5rem);
  font-weight: 700;
  line-height: 1.02;
  letter-spacing: 0.01em;
  text-transform: uppercase;
  color: var(--olive-dark);
}

.role {
  margin: 0;
  color: var(--peach-dark);
  font-size: 1.5rem;
  font-weight: 600;
}

.tagline {
  margin: 1.25rem 0 0;
  max-width: 440px;
  color: var(--text-soft);
  font-size: 1.15rem;
  line-height: 1.6;
}

/* ---------- Content sections ---------- */

.about,
.skills,
.projects,
.why,
.contact {
  position: relative;
  overflow: hidden;
  padding-top: 5.5rem;
  padding-bottom: 5.5rem;
}

.about > *,
.skills > *,
.projects > *,
.why > *,
.contact > * {
  position: relative;
  z-index: 1;
}

.skills,
.why {
  background: var(--cream-dark);
}

.about::before,
.skills::before,
.projects::before {
  content: '';
  position: absolute;
  top: -60px;
  left: 5%;
  width: 150px;
  height: 150px;
  border-radius: 50%;
  background: repeating-linear-gradient(
    135deg,
    var(--peach) 0 8px,
    transparent 8px 16px
  );
  opacity: 0.8;
}

.about::after,
.skills::after,
.projects::after {
  content: '';
  position: absolute;
  right: -90px;
  bottom: -90px;
  width: 240px;
  height: 240px;
  border-radius: 50%;
  background: var(--sage);
  opacity: 0.7;
}

h2 {
  margin: 0 0 2rem;
  text-align: center;
  font-size: 2.2rem;
  font-weight: 700;
  letter-spacing: 0.02em;
  color: var(--olive-dark);
}

/* ---------- About ---------- */

.about-content {
  display: flow-root;
  max-width: 1000px;
  margin: 0 auto;
}

.about-media {
  float: left;
  width: 260px;
  margin: 0 3.5rem 1.5rem 1.25rem;
}

.photo-frame {
  position: relative;
  padding: 0.75rem;
  background: #ffffff;
  box-shadow: 0 8px 24px rgba(74, 72, 60, 0.2);
}

.about-photo {
  display: block;
  width: 100%;
  aspect-ratio: 3 / 4;
  object-fit: cover;
  object-position: top;
}

.photo-tag {
  position: absolute;
  top: 1.5rem;
  left: -1.25rem;
  z-index: 2;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.6rem;
  height: 2.6rem;
  background: var(--cream);
  color: var(--olive-dark);
  font-size: 0.85rem;
  font-weight: 700;
  box-shadow: 0 4px 10px rgba(74, 72, 60, 0.2);
}

.photo-bar {
  position: absolute;
  right: -0.75rem;
  bottom: 2.5rem;
  width: 0.9rem;
  height: 3.2rem;
  background: var(--peach-dark);
}

.about-social {
  display: flex;
  flex-direction: row;
  gap: 0.6rem;
  margin: 1.5rem 0 0;
}

.about-social a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.8rem;
  height: 2.8rem;
  background: var(--olive);
  color: var(--cream);
  font-size: 0.95rem;
  font-weight: 700;
  text-decoration: none;
  transition: background 0.2s;
}

.about-social a:hover {
  background: var(--peach-dark);
}

.about-heading {
  position: relative;
  display: inline-block;
  margin: 0 0 1.5rem;
  text-align: left;
  font-family: 'Barlow Condensed', 'Barlow', sans-serif;
  font-size: clamp(2.6rem, 6vw, 4rem);
  font-weight: 700;
  line-height: 1;
  letter-spacing: 0.01em;
  text-transform: uppercase;
  color: var(--olive-dark);
}

.about-heading span {
  position: relative;
}

.about-heading span::before {
  content: '';
  position: absolute;
  top: -0.2em;
  right: -0.4em;
  z-index: -1;
  width: 55%;
  height: 1.1em;
  background: var(--peach);
  opacity: 0.6;
}

.about-text p {
  margin: 0;
  color: var(--text-soft);
  font-size: 1.1rem;
  line-height: 1.8;
}

.about-text p + p {
  margin-top: 1.25rem;
}

/* ---------- Skills ---------- */

.skill-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
}

.skill-card {
  padding: 1.5rem;
  background: var(--cream);
  border-top: 4px solid var(--peach);
  border-radius: 4px;
  box-shadow: 0 4px 12px rgba(74, 72, 60, 0.1);
  transition: transform 0.2s, box-shadow 0.2s;
}

.skill-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 20px rgba(74, 72, 60, 0.15);
}

.skill-card h3 {
  margin: 0 0 1rem;
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--olive-dark);
}

.skill-card ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.skill-card li {
  padding: 0.35rem 0.8rem;
  background: var(--olive);
  color: var(--cream);
  border-radius: 4px;
  font-size: 0.9rem;
  font-weight: 500;
}

/* ---------- Projects ---------- */

.filter-bar {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 0.6rem;
  margin: -0.5rem 0 2rem;
}

.filter-button {
  padding: 0.5rem 1.2rem;
  background: transparent;
  color: var(--olive-dark);
  border: 1px solid var(--olive);
  border-radius: 999px;
  font-family: inherit;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.2s, color 0.2s, border-color 0.2s;
}

.filter-button:hover {
  border-color: var(--peach-dark);
  color: var(--peach-dark);
}

.filter-button.active {
  background: var(--olive);
  color: var(--cream);
  border-color: var(--olive);
}

.project-grid {
  counter-reset: project;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

.project {
  counter-increment: project;
  position: relative;
  padding: 1.75rem 1.75rem 1.75rem 5rem;
  background: var(--olive);
  color: var(--cream);
  border-radius: 4px;
  transition: transform 0.2s;
}

.project:hover {
  transform: translateY(-4px);
}

.project-enter-active,
.project-leave-active {
  transition: opacity 0.3s ease, transform 0.3s ease;
}

.project-enter-from,
.project-leave-to {
  opacity: 0;
  transform: scale(0.96);
}

.project::before {
  content: counter(project);
  position: absolute;
  top: 1.75rem;
  left: 1.5rem;
  width: 2.4rem;
  height: 2.4rem;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: var(--cream);
  color: var(--olive-dark);
  font-weight: 700;
}

.project h3 {
  margin: 0 0 0.5rem;
  font-size: 1.35rem;
  font-weight: 700;
}

.project p {
  margin: 0 0 1rem;
  color: #e0dbc6;
  line-height: 1.6;
}

.tech {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tech li {
  padding: 0.2rem 0.65rem;
  border: 1px solid var(--peach);
  border-radius: 4px;
  font-size: 0.8rem;
  color: #e3c9b6;
}

.project-links {
  display: flex;
  flex-wrap: wrap;
  gap: 1.25rem;
  margin-top: 1.25rem;
}

.project-link {
  color: var(--cream);
  font-size: 0.95rem;
  font-weight: 600;
  text-decoration: underline;
}

.project-link:hover {
  color: #e3c9b6;
}

/* ---------- Why work with me ---------- */

.why-intro {
  max-width: 620px;
  margin: -0.5rem auto 2.5rem;
  text-align: center;
  color: var(--text-soft);
  font-size: 1.1rem;
  line-height: 1.7;
}

.strength-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
  max-width: 1000px;
  margin: 0 auto;
}

.strength-card {
  padding: 1.5rem;
  background: var(--cream);
  border-top: 4px solid var(--peach);
  border-radius: 4px;
  box-shadow: 0 4px 12px rgba(74, 72, 60, 0.1);
  transition: transform 0.2s, box-shadow 0.2s;
}

.strength-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 20px rgba(74, 72, 60, 0.15);
}

.strength-card h3 {
  margin: 0 0 0.6rem;
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--olive-dark);
}

.strength-card p {
  margin: 0;
  color: var(--text-soft);
  font-size: 0.98rem;
  line-height: 1.65;
}

.journey-heading {
  margin: 4rem 0 2rem;
  text-align: center;
  font-family: 'Barlow Condensed', 'Barlow', sans-serif;
  font-size: 2.4rem;
  font-weight: 700;
  letter-spacing: 0.02em;
  text-transform: uppercase;
  color: var(--olive-dark);
}

.journey {
  list-style: none;
  max-width: 720px;
  margin: 0 auto;
  padding: 0 0 0 2rem;
  border-left: 3px solid var(--peach);
}

.journey-item {
  position: relative;
  padding-bottom: 2rem;
}

.journey-item:last-child {
  padding-bottom: 0;
}

.journey-item::before {
  content: '';
  position: absolute;
  top: 0.35rem;
  left: -2.7rem;
  width: 0.85rem;
  height: 0.85rem;
  background: var(--olive);
  border: 3px solid var(--cream-dark);
  border-radius: 50%;
  box-sizing: content-box;
}

.journey-when {
  display: inline-block;
  margin-bottom: 0.3rem;
  padding: 0.15rem 0.6rem;
  background: var(--peach);
  color: var(--olive-dark);
  border-radius: 4px;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.03em;
  text-transform: uppercase;
}

.journey-item h4 {
  margin: 0.25rem 0 0.35rem;
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--olive-dark);
}

.journey-item p {
  margin: 0;
  color: var(--text-soft);
  font-size: 1rem;
  line-height: 1.65;
}

/* ---------- Contact ---------- */

.contact {
  background: var(--olive);
  text-align: center;
}

.contact::before {
  content: '';
  position: absolute;
  top: -80px;
  right: 8%;
  width: 240px;
  height: 240px;
  border-radius: 50%;
  background: repeating-linear-gradient(
    135deg,
    var(--stripe) 0 10px,
    var(--cream) 10px 20px
  );
  opacity: 0.9;
}

.contact::after {
  content: '';
  position: absolute;
  left: 8%;
  bottom: 2rem;
  width: 130px;
  height: 70px;
  background-image: radial-gradient(var(--peach) 3px, transparent 3.5px);
  background-size: 16px 16px;
}

.contact h2 {
  color: var(--cream);
}

.contact p {
  margin: 0 0 1.75rem;
  color: #e0dbc6;
  font-size: 1.15rem;
}

.actions {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
}

.button {
  display: inline-block;
  padding: 0.8rem 1.7rem;
  background: var(--cream);
  color: var(--olive-dark);
  text-decoration: none;
  border: 1px solid var(--cream);
  border-radius: 4px;
  font-size: 1rem;
  font-weight: 600;
  transition: background 0.2s, color 0.2s;
}

.button:hover {
  background: var(--peach);
  border-color: var(--peach);
}

.button-outline {
  background: transparent;
  color: var(--cream);
}

.button-outline:hover {
  background: var(--cream);
  color: var(--olive-dark);
  border-color: var(--cream);
}

.social {
  display: flex;
  justify-content: center;
  gap: 1.75rem;
  margin-top: 2rem;
}

.social a {
  color: #e0dbc6;
  font-size: 0.95rem;
  text-decoration: none;
  border-bottom: 1px solid var(--peach);
  transition: color 0.2s;
}

.social a:hover {
  color: var(--peach);
}

/* ---------- Footer ---------- */

footer {
  padding: 1.5rem 10%;
  background: var(--olive-dark);
  color: #cfc9b2;
  font-size: 0.9rem;
}

footer p {
  margin: 0;
}

/* ---------- Mobile ---------- */

@media (max-width: 640px) {
  .nav {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.75rem 6%;
  }

  .nav nav {
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.5rem 1rem;
  }

  section {
    padding-left: 6%;
    padding-right: 6%;
    scroll-margin-top: 7rem;
  }

  footer {
    padding-left: 6%;
    padding-right: 6%;
  }

  .hero::before {
    width: 100%;
    bottom: 14%;
    border-radius: 0 0 60% 0 / 0 0 25% 0;
  }

  .hero .deco-stripes {
    width: 150px;
    height: 150px;
    right: 6%;
    bottom: 4%;
  }

  .hero .deco-stripes-peach {
    width: 130px;
    height: 130px;
    left: 4%;
    bottom: -50px;
  }

  .hero .deco-dots {
    top: 12%;
    right: 4%;
    width: 80px;
  }

  .role {
    font-size: 1.2rem;
  }

  .about,
  .skills,
  .projects,
  .why,
  .contact {
    padding-top: 3.5rem;
    padding-bottom: 3.5rem;
  }

  .about-media {
    float: none;
    max-width: 260px;
    margin: 0 auto 2.5rem;
  }

  .photo-tag {
    left: -0.5rem;
  }

  .project {
    padding-left: 4.5rem;
  }

  .journey-heading {
    margin-top: 3rem;
  }
}
</style>
