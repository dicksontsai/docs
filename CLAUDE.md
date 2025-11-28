# New Blog Post

When you create a new blog post:

1. Create a new .mdx file in the appropriate topic folder (e.g.,
   blog/claude-code/my-post.mdx)
2. Add the file to the navigation in docs.json under the appropriate group
3. Add an Update entry in `blog/all-posts/all-posts.mdx` and the appropriate
   `blog/all-posts/yyyy-qN.mdx` (e.g. 2025-q2.mdx) with the post date and link

Posts should be ordered newest first (reverse chronological).

```
  <Update label="September 2021">
  ## {blog title}

  {blog description}

  [Read more →](/blog/learning-and-teaching/sat-reading-series-lessons)
  </Update>
```
