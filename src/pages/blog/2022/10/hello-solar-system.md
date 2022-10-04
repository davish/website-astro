---
layout: "/src/layouts/BlogPost.astro"
title: "Hello, Solar System!"
date: 2022-10-03
draft: false 
tags: [meta, webdev, astro, javascript]
description: "Rewriting this website in the Astro web framework."
---

Hello World, [again](/blog/2020/02/my-first-post)! I've rewritten this website using the [Astro web framework](https://astro.build). Astro's *very* new, with its [1.0 release](https://astro.build/blog/astro-1/) just under two months ago. but there's a few things that got me excited about it enough to move.

1. **JSX**.  JSX is the templating syntax that powers React. While Astro *can* build and use [React](https://docs.astro.build/en/guides/integrations-guide/react/), [Vue](https://docs.astro.build/en/guides/integrations-guide/vue/),  [Svelte](https://docs.astro.build/en/guides/integrations-guide/svelte/), or any framework from [a growing list](https://docs.astro.build/en/core-concepts/framework-components/) , [`.astro` templates](https://docs.astro.build/en/core-concepts/astro-components/) are written with a mix of TypeScript and JSX and are rendered directly to vanilla HTML with no JavaScript at runtime. TypeScript is written in a [preamble section](https://docs.astro.build/en/core-concepts/astro-components/#the-component-script) that looks similar to Markdown frontmatter and sets up the scope for the rest of the template. I found Hugo's templating system that is built directly on [Go's templating library](https://pkg.go.dev/text/template) to be very limiting by contrast. At this point, I definitely believe the adage that "any powerful templating language eventually grows into an awkward programming language." Astro lets me write plain Typescript and JSX and get HTML pages out the other end.
2. **Scoped CSS**. CSS written in `.astro` templates are scoped to that template only. I'm not a fan of  [dogmatic separation of concerns in CSS](https://adamwathan.me/css-utility-classes-and-separation-of-concerns/). I also don't have much experience with Tailwind, and I enjoy writing SCSS. So scoped styles in all my templates is a happy medium where my styles live close to my templates while I can write in a familiar syntax.
3. **Lightweight**. With everything from archetypes to taxonomies, Hugo is really a static CMS more than a blog generator. It's a much more general system than I need. Astro is a bit "closer to the metal" in that respect. When I've had to write some helpers that I took for granted in Hugo, writing custom helpers is much easier since it can be accomplished in a few lines of Typescript.

<!--more-->

Astro is sponsorted by [Netlify](https://www.netlify.com/), and in many ways appears to be their answer to [Vercel](https://vercel.com/solutions/nextjs)'s extremely popular [NextJS](https://nextjs.org/) framework. Astro seems to be aiming more for the [server-first](https://docs.astro.build/en/concepts/why-astro/#server-first) niche. NextJS is frontend-first and dynamic by default, with the option to [export to static HTML](https://nextjs.org/docs/advanced-features/static-html-export) off to the side. For Astro, both [server-side rendering](https://docs.astro.build/en/guides/server-side-rendering/) and support for [reactive "Islands"](https://docs.astro.build/en/concepts/islands/) are opt-in, rather than opt-out. It's an approach that was very attractive for building a static site, and I'm interested to see how they plan to evolve the framework from here.

---

The transition from Hugo to Astro wasn't too bad. Most of my templates and partials had a 1-1 mapping with Astro components.  I'd like to give a special shoutout to [Bryce Wray](https://www.brycewray.com), whose [site repository](https://github.com/brycewray/astro-site) and blog posts on Astro were a great reference when building out my own site. The Astro docs are great, but they are also new, and there's a few things that I was able to find out about by snooping around Bryce's repo. 

Overall, I'm happy with the move, and think it'll help me make new additions to this site over time with less friction than before. We'll see how that goes!