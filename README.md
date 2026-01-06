# Jerry Yang's Personal Blog

This is my personal blog, built with [Hugo](https://gohugo.io/) and the [Typo](https://github.com/tomfran/typo) theme. I use it to share my learning journey, side projects, and life experiences as a Taiwanese software engineer living in Finland.

## Prerequisites

To run this project locally, you need to have **Hugo** installed on your machine.

- **macOS (Homebrew)**: `brew install hugo`
- **Other Platforms**: See the [Hugo Installation Guide](https://gohugo.io/installation/).

## Local Development

### Start the Local Server
To preview the site locally with live reloading:

```bash
hugo server -D
```

- The `-D` flag includes content marked as `draft: true`.
- Once started, you can view the site at `http://localhost:1313/`.

### Create a New Post
To create a new blog post, run:

```bash
hugo new content/posts/your-post-title.md
```

This will create a new Markdown file with basic front matter (title, date, draft status). After creating it, you can edit the file in the `content/posts/` directory.

## Deployment

The blog is automatically deployed to GitHub Pages via GitHub Actions.

1. Commit your changes.
2. Push to the `main` branch.
3. The [GitHub Action workflow](.github/workflows/hugo.yaml) will trigger, build the site, and deploy it to `jerry871002.github.io`.
