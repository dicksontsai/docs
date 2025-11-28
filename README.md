# Dickson Tsai's Blog - Mintlify Migration

Personal blog migrated to [Mintlify](https://mintlify.com) documentation platform.

## Site Structure

```
docs/
├── docs.json              # Site configuration and navigation
├── index.mdx              # Homepage with bio and featured topics
├── blog/
│   ├── all-posts.mdx      # Chronological list of all posts (newest first)
│   ├── claude-code/       # AI coding assistant posts
│   ├── software-development/  # Engineering posts
│   ├── learning-and-teaching/ # Education and tutoring posts
│   └── fun/               # Board games and hobbies
├── images/                # Images for posts and site
└── logo/                  # Site logos (light/dark modes)
```

## Navigation

The site uses three main tabs:

1. **Home** - Landing page with bio, featured topics, and social links
2. **Blog** - Topic-based navigation with four categories:
   - Claude Code
   - Software Development
   - Learning and Teaching
   - Fun
3. **All Posts** - Reverse chronological list of all posts (blog-style)

## Adding New Posts

### Step 1: Create the post file

Create a new `.mdx` file in the appropriate topic folder:

```mdx
---
title: "Your Post Title"
description: "A brief description for SEO and previews"
---

Your content here using MDX format...

## Headings create table of contents

Use standard markdown with MDX components.
```

### Step 2: Add to navigation

Update `docs.json` to include the new post in the appropriate group:

```json
{
  "group": "Claude Code",
  "icon": "robot",
  "pages": [
    "blog/claude-code/existing-post",
    "blog/claude-code/your-new-post"
  ]
}
```

### Step 3: Add to All Posts

Add an `<Update>` entry in `blog/all-posts.mdx` (newest posts at top):

```mdx
<Update label="November 2024">
## Your Post Title

Brief description of the post.

[Read more →](/blog/claude-code/your-new-post)
</Update>
```

## Content Migration Checklist

Posts to migrate from the existing blog:

- [ ] SAT Reading Series Lessons (September 2021) → `learning-and-teaching/`
- [ ] (Add other posts here as they're identified)

### Migration Steps for Each Post

1. Create `.mdx` file with proper frontmatter
2. Convert HTML content to MDX/Markdown
3. Move images to `/images/` folder and update paths
4. Add to `docs.json` navigation
5. Add entry to `all-posts.mdx`
6. Test locally with `mint dev`

## Customization TODO

- [ ] Update logo files in `/logo/` with personal branding
- [ ] Add profile image to `/images/`
- [ ] Update social links in `docs.json` and `index.mdx`
- [ ] Configure favicon
- [ ] Set up custom domain (if desired)

## Development

### Prerequisites

- Node.js v20.17.0 or higher (LTS recommended)

### Install CLI

```bash
npm i -g mint
```

### Local Preview

```bash
mint dev
```

View at `http://localhost:3000`

### Update CLI

```bash
mint update
```

## Deployment

Install the [Mintlify GitHub App](https://dashboard.mintlify.com/settings/organization/github-app) to enable automatic deployments when pushing to the main branch.

## Resources

- [Mintlify Documentation](https://mintlify.com/docs)
- [MDX Guide](https://mintlify.com/docs/content/page)
- [Navigation Configuration](https://mintlify.com/docs/organize/navigation)
- [Changelog/Updates Component](https://mintlify.com/docs/create/changelogs)
