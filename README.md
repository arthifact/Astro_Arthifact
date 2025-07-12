# Astro Arthifact Website

*(A fork and modification from Astro Cactus by Chris Williams)*

Welcome to the template for [Astro Arthifact](https://arthifact.com/) —  my site for interactive systems, visual constructs, and neural logs. 

## Features

- **Blog Posts**: Write and share articles with support for tags, topics, cover images, and more.
- **Notes**: Short-form content for quick ideas and thoughts.
- **Projects**: Showcase projects with cover images, descriptions, and publish dates.
- **Topics**: Posts are grouped by topic for easy browsing.
- **Tags**: Tag posts for discoverability; tag pages can have custom descriptions.
- **Dark & Light Mode**: Theme toggling with a dark mode default.
- **Responsive Design**: Looks great on all devices.
- **Search**: Fast, static search powered by Pagefind.
- **RSS Feeds**: Automatic RSS for posts and notes.
- **Open Graph Images**: Auto-generated or custom OG images for sharing.

## To Deploy to GitHub Pages:

This template includes a GitHub Actions workflow to deploy your site to GitHub Pages.
To publish your site at https://your-username.github.io:

1. Rename your repository to your-username.github.io

2. Make sure GitHub Pages is enabled in your repo settings and **Source** set to --> GitHub Actions

3. Set the correct site URL in `astro.config.ts`:

```js
 site: siteConfig.url,
	image: {
		domains: ["your-username.github.io"],
 },
```

The included .github/workflows/deploy.yml will automatically build and deploy your site to the gh-pages branch when you push to main.

## Local Getting Started

1. **Install dependencies:**
   ```sh
   pnpm install
   # or
   npm install
   ```
2. **Run the development server:**
   ```sh
   pnpm dev
   # or
   npm run dev
   ```
3. **Build for production:**
   ```sh
   pnpm build
   ```

## Content Structure

- `src/content/post/` — Blog posts (Markdown/MDX)
- `src/content/note/` — Notes (Markdown/MDX)
- `src/content/projects/` — Projects (Markdown/MDX)
- `src/content/tag/` — Tag metadata (optional, Markdown)

### Example Post Frontmatter
```yaml
---
title: "My Post Title"
description: "A short summary of the post."
topic: "Web Development"
publishDate: "25 Aug 2024"
updatedDate: "26 Aug 2024"
tags: ["astro", "web"]
coverImage:
  src: "./cover.png"
  alt: "Cover image alt text"
---
```

### Example Project Frontmatter
```yaml
---
title: "My Project"
description: "A description of the project."
topic: "" # Leave empty for projects
tags: [] # Leave empty for projects
publishDate: "01 Jan 2024"
coverImage:
  src: "./cover.png"
  alt: "Project cover"
---
```

### Example Tag Metadata
`src/content/tag/astro.md`:
```markdown
---
title: Astro
description: Posts about the Astro static site generator.
---
```

## Customization
- Edit site settings in `src/site.config.ts` (title, description, author, etc).
- Update styles in `src/styles/global.css` and Tailwind config.
- Add or edit navigation links in `src/site.config.ts`.

## License
MIT
