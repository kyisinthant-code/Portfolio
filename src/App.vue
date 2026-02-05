<template>
  <div class="page" ref="root">
    <div class="grain" aria-hidden="true"></div>
    <div class="glow-orb orb-one" aria-hidden="true"></div>
    <div class="glow-orb orb-two" aria-hidden="true"></div>
    <div class="glow-orb orb-three" aria-hidden="true"></div>

    <header class="nav">
      <div class="logo">KST</div>
      <!-- <nav class="nav-links">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav> -->
      <a class="ghost-btn" href="/resume.pdf" download>Download Resume</a>
    </header>

    <main>
      <section class="hero" id="home" data-reveal>
        <div class="hero-content">
          <p class="eyebrow">Front-end Developer · 6 Years Experience</p>
          <h1>
            KYI SIN THANT
            <span>Building elegant, high-performance web experiences.</span>
          </h1>
          <p class="lead">
            Senior developer with over 6 years of experience delivering
            high-quality web applications. I focus on front-end excellence,
            intuitive UI/UX, and designing scalable, well-structured APIs that
            support long-term growth.
          </p>
          <div class="hero-actions">
            <a class="primary-btn" href="#contact">Let’s Work Together</a>
            <a class="secondary-btn" href="#projects">See Projects</a>
          </div>
          <div class="stat-grid">
            <div class="stat-card" data-reveal>
              <span>6+</span>
              <p>Years Building</p>
            </div>
            <div class="stat-card" data-reveal>
              <span>12+</span>
              <p>Tech Stacks</p>
            </div>
            <div class="stat-card" data-reveal>
              <span>Full-Stack</span>
              <p>Vue · React · ASP.NET</p>
            </div>
          </div>
        </div>
        <div class="hero-visual">
          <div class="floating-card card-one" data-reveal>
            <p class="card-title">Focus Areas</p>
            <ul>
              <li>Vue + Nuxt ecosystems</li>
              <li>React + Next platforms</li>
              <li>Node backends</li>
            </ul>
          </div>
          <div class="floating-card card-two" data-reveal>
            <p class="card-title">Specialties</p>
            <div class="pill">TypeScript</div>
            <div class="pill">Tailwind</div>
            <div class="pill">Design Systems</div>
            <div class="pill">Animations</div>
          </div>
          <div class="floating-card card-three" data-reveal>
            <p class="card-title">Currently</p>
            <p class="card-body">
              Open to new collaborations and ambitious builds.
            </p>
          </div>
        </div>
      </section>

      <section class="about" id="about" data-reveal>
        <div class="section-title">
          <h2>About Me</h2>
          <p>I love clean UI, smooth motion, and scalable codebases.</p>
        </div>
        <div class="about-grid">
          <div class="about-card" data-reveal>
            <h3>Profile</h3>
            <p>
              Senior developer with over 6 years of experience delivering
              high-quality web applications. I focus on front-end excellence,
              intuitive UI/UX, and designing scalable, well-structured APIs that
              support long-term growth.
            </p>
          </div>
          <div class="about-card" data-reveal>
            <h3>Approach</h3>
            <p>
              I balance visual polish with performance. Clean architecture,
              reusable components, and scalable patterns are at the heart of
              every build.
            </p>
          </div>
          <div class="about-card" data-reveal>
            <h3>Mindset</h3>
            <p>
              I’m a fast learner, team player, and always eager to explore new
              technologies and improve development practices.
            </p>
          </div>
        </div>
      </section>

      <section class="skills" id="skills" data-reveal>
        <div class="section-title">
          <h2>Skills & Tools</h2>
          <p>Full-stack experience across modern frameworks and UI systems.</p>
        </div>
        <div class="skills-grid">
          <div
            v-for="(skill, index) in skills"
            :key="skill"
            class="skill-chip"
            data-reveal
            :style="{ '--delay': `${index * 0.05}s` }"
          >
            {{ skill }}
          </div>
        </div>
      </section>

      <section class="timeline" id="experience" data-reveal>
        <div class="section-title">
          <h2>Professional Experience</h2>
          <p>Selected roles and impact delivered.</p>
        </div>
        <div class="timeline-grid">
          <article
            v-for="(job, index) in experiences"
            :key="job.title"
            class="timeline-card"
            data-reveal
            :style="{ '--delay': `${index * 0.1}s` }"
          >
            <div class="timeline-header">
              <h3>{{ job.title }}</h3>
              <span>{{ job.company }}</span>
              <span>{{ job.period }}</span>
            </div>
            <ul>
              <li v-for="detail in job.details" :key="detail">{{ detail }}</li>
            </ul>
          </article>
        </div>
      </section>

      <section class="projects" id="projects" data-reveal>
        <div class="section-title">
          <h2>Selected Projects</h2>
          <p>Recent work and craft-focused builds.</p>
        </div>
        <div class="project-grid">
          <article
            v-for="(project, index) in projects"
            :key="project.title"
            class="project-card"
            data-reveal
            :style="{ '--delay': `${index * 0.1}s` }"
          >
            <div class="project-badge">{{ project.tag }}</div>
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <div class="project-stack">
              <span v-for="tech in project.stack" :key="tech">{{ tech }}</span>
            </div>
          </article>
        </div>
      </section>

      <section class="cta" id="contact" data-reveal>
        <div class="cta-card" data-reveal>
          <div>
            <h2>Let’s build something beautiful.</h2>
            <p>
              Available for freelance, full-time, or contract work. Tell me
              about your idea and I’ll help make it real.
            </p>
          </div>
          <div class="cta-actions">
            <a class="primary-btn" :href="`mailto:${email}`">Email Me</a>
            <a class="ghost-btn" href="/resume.pdf" download>Download Resume</a>
          </div>
        </div>
      </section>
    </main>

    <footer class="footer">
      <div>
        <span>Front-End Developer · Vue · React · TypeScript</span>
      </div>
      <div class="footer-links">
        <a :href="`mailto:${email}`">{{ email }}</a>
        <span>© 2026</span>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { onMounted, onUnmounted, ref } from "vue";

const root = ref<HTMLElement | null>(null);

let observer: IntersectionObserver | null = null;
let rafId = 0;

const handleMouseMove = (event: MouseEvent) => {
  if (!root.value) return;
  if (rafId) cancelAnimationFrame(rafId);
  rafId = requestAnimationFrame(() => {
    const { innerWidth, innerHeight } = window;
    const x = (event.clientX / innerWidth - 0.5) * 2;
    const y = (event.clientY / innerHeight - 0.5) * 2;
    root.value?.style.setProperty("--mx", x.toFixed(3));
    root.value?.style.setProperty("--my", y.toFixed(3));
  });
};

onMounted(() => {
  if (root.value) {
    root.value.style.setProperty("--mx", "0");
    root.value.style.setProperty("--my", "0");
  }

  observer = new IntersectionObserver(
    (entries) => {
      for (const entry of entries) {
        if (entry.isIntersecting) {
          entry.target.classList.add("in-view");
          observer?.unobserve(entry.target);
        }
      }
    },
    { threshold: 0.2 },
  );

  document
    .querySelectorAll("[data-reveal]")
    .forEach((el) => observer?.observe(el));
  window.addEventListener("mousemove", handleMouseMove);
});

onUnmounted(() => {
  observer?.disconnect();
  window.removeEventListener("mousemove", handleMouseMove);
});

const email = "kyisinthant.kst97@gmail.com";

const skills = [
  "Vue",
  "React",
  "Node",
  "TypeScript",
  "Tailwind",
  "CSS",
  "HTML",
  "JavaScript",
  "Bootstrap",
  "Nuxt",
  "Next",
  "RESTful APIs",
  "Azure",
  "AWS",
  "Jest",
  "Agile/Scrum",
  "Git",
  "English",
  "Japanese (N3)",
];

const experiences = [
  {
    title: "Senior Front-End Developer",
    company: "Codigo | City Development Limited",
    period: "2023 – 2025",
    details: [
      "Migrated a large-scale application from Vue 2 to Vue 3 using Nuxt.js with minimal user disruption.",
      "Built reusable components and improved performance with the Composition API, virtual DOM, and clean state flow.",
      "Delivered responsive, accessible UI with Tailwind CSS and TypeScript across devices and browsers.",
      "Integrated front-end with backend APIs, keeping data flow consistent and reliable.",
      "Used Jest for unit testing and maintained quality gates for new features.",
      "Partnered with designers and backend engineers to ship high‑quality releases.",
    ],
  },
  {
    title: "Senior Full-Stack Developer",
    company: "Thetys | Fusion Solution",
    period: "2019 – 2023",
    details: [
      "Built full‑stack web applications with Vue.js, React.js, and ASP.NET Core.",
      "Designed secure RESTful APIs with robust validation and data handling.",
      "Led small Agile teams, supported sprint planning, and performed code reviews.",
      "Implemented authentication and authorization using OAuth, JWT, and ASP.NET Identity.",
      "Optimized SQL queries and application performance for scale and stability.",
      "Troubleshot production issues and delivered fast, reliable fixes.",
      "Defined architecture and technical solutions for new business requirements.",
      "Mentored junior developers to improve team productivity and code quality.",
    ],
  },
];

const projects = [
  {
    title: "Human Resource Management System",
    tag: "Vue + ASP.NET",
    description:
      "Built responsive UI for HR tasks like employee data, payroll, and work hours, plus secure backend services for real-time data.",
    stack: ["Vue.js", "Vuetify", "ASP.NET", "SQL Server"],
  },
  {
    title: "Employee Management System",
    tag: "React + Next",
    description:
      "Digital clock-in/out with real-time tracking, GPS validation, and automated HR reporting workflows.",
    stack: ["React.js", "Next.js", "TypeScript"],
  },
  {
    title: "Smart Lifestyle Experience Platform",
    tag: "Nuxt + Vue 3",
    description:
      "Vue 2 to Vue 3 migration with Nuxt SSR, modular components, and performance-focused code splitting.",
    stack: ["Nuxt.js", "Vue 3", "TypeScript"],
  },
];
</script>
