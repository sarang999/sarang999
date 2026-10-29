<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B0D12,50:FF6B35,100:5CE1E6&height=180&section=header&text=Sarang%20Chaudhary&fontSize=56&fontColor=F2F0EA&fontAlignY=38&desc=Senior%20Software%20Engineer%20%C2%B7%20React%20%C2%B7%20Next.js%20%C2%B7%20React%20Native&descSize=18&descAlignY=58&animation=fadeIn" alt="Sarang Chaudhary — Senior Software Engineer" width="100%" />
</div>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=2600&pause=1200&color=5CE1E6&center=true&vCenter=true&width=900&lines=I+ship+the+storefronts+behind+Chili's%2C+Starbucks+%26+Hard+Rock;29%2B+countries+%C2%B7+1.29M%2B+users+%C2%B7+%2416M+revenue+in+month+one;800+ms+%E2%86%92+under+50+ms+with+a+3-layer+cache+I+designed;React+%C2%B7+Next.js+%C2%B7+React+Native+%C2%B7+TypeScript+%C2%B7+AI-augmented+delivery" />
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=2600&pause=1200&color=C2410C&center=true&vCenter=true&width=900&lines=I+ship+the+storefronts+behind+Chili's%2C+Starbucks+%26+Hard+Rock;29%2B+countries+%C2%B7+1.29M%2B+users+%C2%B7+%2416M+revenue+in+month+one;800+ms+%E2%86%92+under+50+ms+with+a+3-layer+cache+I+designed;React+%C2%B7+Next.js+%C2%B7+React+Native+%C2%B7+TypeScript+%C2%B7+AI-augmented+delivery" alt="I ship the storefronts behind Chili's, Starbucks and Hard Rock. 29+ countries, 1.29M+ users, $16M revenue in month one. 800 ms to under 50 ms with a 3-layer cache I designed." />
  </picture>
</p>

<p align="center">
  <a href="https://sarangchaudhary.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-FF6B35?style=for-the-badge&logo=firefox&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/sarang-chaudhary-401405178/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://drive.google.com/file/d/10e7faVK4nKOi4UGJ8tb-E3sKYqGwnUBY/view"><img src="https://img.shields.io/badge/Resume-4285F4?style=for-the-badge&logo=google-drive&logoColor=white" alt="Resume" /></a>
  <a href="https://www.linkedin.com/in/sarang-chaudhary-401405178/details/recommendations/"><img src="https://img.shields.io/badge/Testimonials-FFD700?style=for-the-badge&logo=linkedin&logoColor=black" alt="Testimonials" /></a>
  <a href="mailto:sarangchaudhary2014@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=sarang999&label=Profile%20views&color=5CE1E6&style=flat-square" alt="Profile views" />
  <img src="https://img.shields.io/github/followers/sarang999?label=Followers&style=flat-square&color=5CE1E6" alt="GitHub followers" />
  <img src="https://img.shields.io/badge/Open%20to-Senior%20Frontend%20%2F%20Full--stack%20roles-FF6B35?style=flat-square" alt="Open to senior frontend and full-stack roles" />
</p>

> [!TIP]
> **Thirty-second version.** Senior engineer at **GALE** in Bengaluru who builds and ships production web and mobile products for North American brands: **Chili's, Starbucks, Hard Rock, Creative Planning, Pella.** I own the whole slice: Next.js and React Native front ends, the caching and CDN layers under them, CI/CD to AWS, 90%+ test coverage, and the AI tooling that lets the team move faster without losing architectural control.

## Impact in numbers

<table align="center">
  <tr>
    <td align="center"><h2>29+</h2>countries served<br/><sub>Chili's global platform</sub></td>
    <td align="center"><h2>1.29M+</h2>users · 2.09M+ sessions<br/><sub>web &amp; mobile</sub></td>
    <td align="center"><h2>$16M</h2>revenue in month one<br/><sub>after stack migration</sub></td>
    <td align="center"><h2>800→50 ms</h2>API response<br/><sub>3-layer cache, 150k+ entries</sub></td>
    <td align="center"><h2>-80%</h2>CDN cost<br/><sub>batched invalidation</sub></td>
    <td align="center"><h2>90%+</h2>test coverage<br/><sub>every major project</sub></td>
  </tr>
</table>

## How I think about a request

Instead of listing "caching" as a skill, here is the layer I designed for Creative Planning. Every hop is a cache; the origin is the last resort.

```mermaid
flowchart LR
  U([Visitor]) -->|HTTPS| CF["CloudFront edge<br/>batched invalidation"]
  CF -->|miss| ISR["Next.js ISR<br/>stale-while-revalidate"]
  ISR -->|miss| VK[("Valkey<br/>shared app cache")]
  VK -->|miss| GQL["Dual GraphQL clients<br/>Contentful · WordPress"]
  GQL -.->|publish webhook| VK
  VK -.->|revalidate tag| ISR
  ISR -.->|invalidate path batch| CF
  classDef edge fill:#12151D,stroke:#5CE1E6,color:#F2F0EA,stroke-width:2px
  classDef hot fill:#FF6B35,stroke:#FF6B35,color:#0B0D12,stroke-width:2px
  class CF,ISR,VK edge
  class U,GQL hot
```

<sub>Result on production traffic: p95 **800 ms → under 50 ms**, CDN spend **−80%**, sitemap engine validated at **150,000+ entries** with O(1) per-category updates.</sub>

## About me

```ts
const sarang = {
  pronouns: "he/him",
  role: "Senior Associate (Software Engineer) @ GALE",
  base: "Bengaluru, India 🇮🇳 · working with North American teams and clients",
  years: 4,
  builds: ["Next.js storefronts", "React Native apps", "headless CMS platforms", "AI-augmented workflows"],
  askMeAbout: ["web performance", "caching & CDNs", "mobile apps", "AI tooling for teams"],
  offHours: { tea: "fuel for deep work 🍵", markets: "charts & stocks 📈", world: "geopolitics 🌍" },
  goal: "ship scalable products that matter, at global scale",
} satisfies Record<string, unknown>;
```

## Stack

<table>
  <tr>
    <td><b>Core</b></td>
    <td>
      <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
      <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
      <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
      <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React Native" />
      <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
    </td>
  </tr>
  <tr>
    <td><b>UI</b></td>
    <td>
      <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
      <img src="https://img.shields.io/badge/Material_UI-0081CB?style=for-the-badge&logo=mui&logoColor=white" alt="Material UI" />
      <img src="https://img.shields.io/badge/Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=white" alt="Storybook" />
      <img src="https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white" alt="Redux" />
      <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
      <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
    </td>
  </tr>
  <tr>
    <td><b>APIs &amp; data</b></td>
    <td>
      <img src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white" alt="GraphQL" />
      <img src="https://img.shields.io/badge/Contentful-2478CC?style=for-the-badge&logo=contentful&logoColor=white" alt="Contentful" />
      <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js" />
      <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
    </td>
  </tr>
  <tr>
    <td><b>Cloud &amp; delivery</b></td>
    <td>
      <img src="https://img.shields.io/badge/AWS_CloudFront-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS CloudFront" />
      <img src="https://img.shields.io/badge/Redis_%2F_Valkey-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis / Valkey" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
      <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions" />
    </td>
  </tr>
  <tr>
    <td><b>Quality &amp; tools</b></td>
    <td>
      <img src="https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white" alt="Jest" />
      <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white" alt="Vitest" />
      <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
      <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman" />
      <img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" alt="VS Code" />
      <img src="https://img.shields.io/badge/Xcode-007ACC?style=for-the-badge&logo=xcode&logoColor=white" alt="Xcode" />
      <img src="https://img.shields.io/badge/Android_Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white" alt="Android Studio" />
    </td>
  </tr>
  <tr>
    <td><b>AI workflow</b></td>
    <td>
      <img src="https://img.shields.io/badge/GitHub_Copilot-000000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Copilot" />
      <img src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude" />
      <img src="https://img.shields.io/badge/ChatGPT-74AA9C?style=for-the-badge&logo=openai&logoColor=white" alt="ChatGPT" />
      <img src="https://img.shields.io/badge/Prompt_Engineering-6C63FF?style=for-the-badge&logo=openai&logoColor=white" alt="Prompt Engineering" />
    </td>
  </tr>
</table>

## Work that shipped

Expand any card for the engineering detail.

<details open>
<summary><b>🏦 Creative Planning · enterprise CMS platform</b> — Next.js 16 monorepo, 3-layer cache, 150k-entry sitemap engine · <a href="https://creativeplanning.com/">creativeplanning.com</a></summary>

- Built a **production pnpm monorepo (6 packages)** on Next.js 16 + React 19 with Turbopack, proxy middleware, async APIs and CSS-first Tailwind v4, so every service deploys independently.
- Designed the **3-layer cache** (Valkey + ISR + CloudFront with batched invalidation) and a **hash-per-category sitemap engine** with O(1) updates, Contentful/WordPress merging and international variants, validated at **150,000+ entries**: response time **800 ms → under 50 ms**, CDN cost **−80%**.
- Integrated **Contentful** through dual GraphQL clients, 12+ content types, full SEO metadata (OG, Twitter, canonical, robots) and the Live Preview SDK with Inspector Mode, so editors publish without a redeploy.
- Delivered **24+ accessible React components** (React Aria + Tailwind v4), a type-safe PageBuilder, **Storybook 10** visual regression, nonce-based CSP, HSTS and PII-safe logging, deployed by **GitHub Actions to AWS ECR/ECS in under 8 minutes**.
</details>

<details>
<summary><b>🌶️ Chili's · global web &amp; mobile platform</b> — 29+ countries, 1.29M+ users, $16M in month one · <a href="https://www.chilis.com/">Web</a> · <a href="https://play.google.com/store/apps/details?id=com.brinker.chilis">Android</a> · <a href="https://apps.apple.com/us/app/chilis/id464383246">iOS</a></summary>

- **Cross-platform product** serving 29+ countries, 1.29M+ users and 2.09M+ sessions, with **$16M in revenue** inside the first month after the tech-stack migration.
- Built the **SEO location system** on Next.js SSR with custom XML sitemaps and Google Maps, lifting SERP rankings and organic traffic.
- Shipped a **secure multi-payment checkout** (cards, Google Pay, gift cards) with account management, driving a **17-minute average session**.
- Tuned state management, code splitting and caching; set up **Jest at 90%+ coverage** and Google Tag Manager for behavioural analytics.
</details>

<details>
<summary><b>☕ Starbucks · multi-locale marketing platform</b> — Next.js 15 SSG, en-US / en-CA / fr-CA · <a href="https://protein.starbucks.com/">US</a> · <a href="https://protein.starbucks.ca/">CA</a> · <a href="https://proteines.starbucks.ca/">CA-FR</a></summary>

- Architected a **Next.js 15 SSG app** with three locales, dynamic routing, automated sitemaps, canonical URLs, JSON-LD and a **headless JSON-driven content model** across 15+ TypeScript interfaces.
- Built **25+ reusable, accessible React components** with MUI theming, interactive quizzes, parallax and viewport-driven animation, documented and verified in Storybook.
- Added automated build validation, Jest unit tests, **CSP headers** and accessibility checks for consistently fast static exports at **90%+ coverage**.
</details>

<details>
<summary><b>🎸 Hard Rock · Unity mobile app</b> — contactless hospitality for 200+ locations in 75 countries · <a href="https://play.google.com/store/apps/details?id=com.shre.unitymobile.prod">Android</a> · <a href="https://apps.apple.com/us/app/unity-by-hard-rock/id1609454172">iOS</a></summary>

- Built the **contactless hospitality flow** (CLEAR identity verification, Virdee mobile keys) with location-aware venue features, Everi payments and a tiered loyalty programme.
- Improved performance with a **WebView architecture** and dynamic content from Sitecore/Firebase, plus A/B testing for data-driven UX decisions.
</details>

<details>
<summary><b>📊 Pella · business analytics dashboard</b> — RBAC, ECharts, Leaflet heat maps</summary>

- Built the **analytics dashboard** with role-based access control so administrators and branch managers track marketing ROI and performance.
- Implemented **data visualisation** with ECharts, Leaflet heat maps and filterable MUI tables, plus promotion management for multiple offer types.
- Designed the **RBAC infrastructure** with dynamic menus and a protected asset repository.
</details>

<details>
<summary><b>🎬 MilkPEP · video customiser</b> — real-time branded video previews, Vitest at 90%+</summary>

- Built a **responsive interactive UI** with dynamic form generation and a real-time video previewer for client-side template customisation (container types, sizes, colours, branded elements) alongside motion designers.
- Implemented an **optimised asset pipeline** that cut cloud-storage cost while keeping preview quality, with validated state management and **90%+ coverage via Vitest**.
</details>

<details>
<summary><b>🤖 AI-augmented engineering</b> — 2.5+ years embedding Copilot, Claude, ChatGPT and OpenCode into production workflows</summary>

- Use **GitHub Copilot, OpenCode, Claude and ChatGPT** daily for generation, debugging and test authoring while keeping full architectural ownership; the team ships faster with higher quality.
- Built a **production AI onboarding system**: `copilot-instructions.md`, four specialised Copilot agents (FE Agent, Docs Generator, Code Reviewer, OpenCode Agent) and a structured `ai_wiki`, adopted across projects to enforce standards and speed up onboarding.
- Configured **OpenCode MCP servers** for Jira, Figma and a Contentful sandbox, so AI-assisted development reads design specs, tickets and live content schemas without context switching.
</details>

## What teammates say

> **"Proactive, diligent, and flexible in his approach to every project. He consistently goes above and beyond expectations, adapting quickly to changing requirements while maintaining high standards of quality."**
> <sub>Bryan McKenzie · Director of Business Analysis &amp; Product Strategy, Gale Partners</sub>

> **"A breadth of skills that extend well beyond frontend development. He consistently completes tasks on time while maintaining clear and effective communication. He has the potential to be a great leader and mentor in any engineering team."**
> <sub>Riley Galante · Senior Software Engineer, Brinker International</sub>

> **"Quickly onboarded and delivered high-quality code at an impressive pace. His contributions were instrumental to the Chili's mobile app MVP, producing clean, well-structured code that set a strong foundation for the product."**
> <sub>Jobin Abraham · Senior Software Engineer, Brinker International</sub>

<p align="center"><a href="https://www.linkedin.com/in/sarang-chaudhary-401405178/details/recommendations/">Read all recommendations on LinkedIn →</a></p>

## Activity

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=sarang999&theme=dark&hide_border=true&background=0B0D12&stroke=232838&ring=FF6B35&fire=FF6B35&currStreakLabel=5CE1E6&sideLabels=F2F0EA&currStreakNum=F2F0EA&sideNums=F2F0EA&dates=8A8F9C" alt="GitHub streak" />
</p>

## Education

| | | |
|---|---|---|
| 🎯 | **Full-Stack Web Development** · Masai School, Bengaluru | Aug 2021 – Apr 2022 |
| 🎓 | **B.E., First Class with Distinction** · Savitribai Phule Pune University | Aug 2017 – Nov 2020 |

## Let's talk

<p align="center">
  <a href="https://www.linkedin.com/in/sarang-chaudhary-401405178/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:sarangchaudhary2014@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" /></a>
  <a href="https://twitter.com/sarangssc"><img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter" /></a>
  <a href="https://stackoverflow.com/users/22754685/sarang-chaudhary"><img src="https://img.shields.io/badge/Stack_Overflow-FE7A16?style=for-the-badge&logo=stack-overflow&logoColor=white" alt="Stack Overflow" /></a>
  <a href="https://sarangchaudhary.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-FF6B35?style=for-the-badge&logo=firefox&logoColor=white" alt="Portfolio" /></a>
</p>

<p align="center">
  🌐 <a href="https://sarangchaudhary.vercel.app/">Portfolio</a> ·
  📄 <a href="https://drive.google.com/file/d/10e7faVK4nKOi4UGJ8tb-E3sKYqGwnUBY/view">Resume</a> ·
  ⭐ <a href="https://www.linkedin.com/in/sarang-chaudhary-401405178/details/recommendations/">Testimonials</a> ·
  💼 <a href="https://www.linkedin.com/in/sarang-chaudhary-401405178/">LinkedIn</a>
</p>

<p align="center"><sub>Take a challenge. Conquer it. Repeat. Never settle.</sub></p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:5CE1E6,50:FF6B35,100:0B0D12&height=90&section=footer" alt="" width="100%" />
</div>

<!--
SEO: Senior Software Engineer, Frontend Engineer, Full-stack Engineer, React Developer, Next.js Developer,
TypeScript, React Native, JavaScript, Node.js, GraphQL, Contentful, Tailwind CSS, Redux, AWS CloudFront,
Docker, GitHub Actions, Valkey, Redis, Storybook, Jest, Vitest, Web Performance, SEO, Headless CMS,
Enterprise Platform, Monorepo, pnpm, AI Tooling, GitHub Copilot, Claude, MCP, Bengaluru, India,
North America clients, Remote, Open to work
-->
