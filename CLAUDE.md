# New Blog Post

When you create a new blog post:

1. Create a new .mdx file in the appropriate topic folder (e.g.,
   `blog/software-development/my-post.mdx`)
2. Add an Update entry in the topic's `all-posts.mdx` (e.g.,
   `blog/software-development/all-posts.mdx`)
3. Add an Update entry in the quarterly file `blog/all-posts/yyyy-qN.mdx`
   (e.g., `2025-q2.mdx`)

Posts should be ordered newest first (reverse chronological) in both all-posts
files.

Update entry format:

```
<Update label="May 18, 2025">
**[Blog Title](/blog/topic-folder/post-slug)**

Blog description goes here.

</Update>
```

Note: Individual blog posts are NOT added to `docs.json`. The navigation uses
the quarterly and topic all-posts files which contain the Update entries.
