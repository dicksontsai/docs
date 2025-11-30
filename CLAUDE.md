# New Blog Post

## File Structure

When you create a new blog post:

1. Create a new .mdx file in the appropriate topic folder (e.g.,
   `blog/software-development/my-post.mdx`)
2. Add an Update entry in the topic's `all-posts.mdx` (e.g.,
   `blog/software-development/all-posts.mdx`)
3. Add an Update entry under the `all-posts` directory (e.g.,
   `blog/all-posts/2025.mdx`)

Posts should be ordered newest first (reverse chronological) in both all-posts
files.

## Post Frontmatter

```mdx
---
title: 'Your Post Title'
description: 'Published Month Day, Year'
---
```

## Update Entry Format

```mdx
<Update label="May 18, 2025">
**[Blog Title](/blog/topic-folder/post-slug)**

Blog description goes here (1-3 sentences summarizing the post).

</Update>
```

Note: Individual blog posts are NOT added to `docs.json`. The navigation uses
the date-based and topic all-posts files which contain the Update entries.

## Writing Style

**Voice and Tone:**

- Write in first person ("I", "my") - this is a personal blog
- Be conversational but informative
- Prefer succint over verbose
- NEVER write in a clickbaity style, especially for titles and headings 

**Structure:**

- Start with a hook or context that draws readers in
- Use clear section headers (##) to organize content chronologically or
  thematically
- Include personal anecdotes that connect to the main topic
- End with a fitting conclusion that includes main takeaways and/or suggestions for next steps

**Formatting:**

- Use horizontal rules (---) to separate the intro from the main content
- Use code blocks with language hints (```sql, ```python, ```bash, etc.)
- Ensure the code within the code blocks are formatted for human readability.
- Bold key phrases or takeaways for scannability
- Use pre-format for any file paths or code syntax (e.g. `CLAUDE.md`, `PATH`)
- Use `<Note>` (blue with round exclamation icon), `<Tip>` (green with light
  bulb icon), `<Warning>` (yellow with triangle caution exclamation icon) ,
  `<Info>` (gray with round i icon), or `<Callout>` (yellow with key icon)
  components where appropriate (not often, to really call something out)

**Content Guidelines:**

- Ground technical concepts in real experiences and iterations
- Don't be afraid to share failures alongside successes - document the journey
- For tutorials: provide step-by-step instructions with code snippets and
  expected outputs
- For reflective posts: extract principles or lessons learned
- Cross-reference other blog posts when relevant using relative links (e.g.,
  `/blog/learning-and-teaching/typing-z-a`)

## Process

- You do not need to write the first draft perfectly. Maybe even start with more and then iteratively cut down
- Launch subagents to evaluate certain dimensions of your work. For example, you can launch a Haiku agent to do a basic coherence check. You can launch an Opus agent to evaluate how informative, insightful, and creative the content is.
