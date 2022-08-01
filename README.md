# NetlifyCMS version

`~/public/admin/condig.yml`

example:

```
site_url: http://localhost:3000
# site_url: https://github.com/r4nd3l/Nuxt3
logo_url: https://raw.githubusercontent.com/r4nd3l/Nuxt3/feature/netlify/public/img/myLogo.png

publish_mode: editorial_workflow
backend:
  name: github
  repo: r4nd3l/Nuxt3
  branch: feature/netlify
  squash_merges: true

# used together with `npx netlify-cms-proxy-server`. https://www.netlifycms.org/docs/beta-features/#working-with-a-local-git-repository
local_backend: true

media_folder: "/assets/images"
public_folder: "/public/img"

# Docs: https://www.netlifycms.org/docs/configuration-options/#collections
collections:
  - name: "Main"
    label: "MainPage"
    folder: "content/00.main"
    create: true
    format: "frontmatter"
    slug: "{{fields.createdAt}}-{{slug}}"
    editor:
      preview: true
    fields:
      - {
          label: "Created Date",
          name: "createdAt",
          widget: "datetime",
          date_format: "YYYY-MM-DD",
          time_format: false,
        }
      - { label: "Title", name: "title", widget: "string", required: true }
      - {
          label: "Description",
          name: "description",
          widget: "string",
          required: false,
        }
      - { label: "Body", name: "body", widget: "markdown", required: false }
      - { label: "Button", name: "button", widget: "string", required: true }

  - name: "blog"
    label: "Blog"
    folder: "content/blog"
    create: true
    format: "frontmatter"
    slug: "{{fields.createdAt}}-{{slug}}"
    editor:
      preview: true
    fields:
      - {
          label: "Created Date",
          name: "createdAt",
          widget: "datetime",
          date_format: "YYYY-MM-DD",
          time_format: false,
        }
      - { label: "Title", name: "title", widget: "string", required: true }
      - {
          label: "Description",
          name: "description",
          widget: "string",
          required: false,
        }
      - { label: "Body", name: "body", widget: "markdown", required: false }

  - name: "projects"
    label: "Projects"
    label_singular: "Project"
    folder: "content/projects"
    create: true
    format: "frontmatter"
    slug: "{{slug}}"
    preview_path: "projects/{{slug}}"
    fields:
      - {
          label: "Project Category",
          name: "category",
          widget: "select",
          default: "animals",
          options:
            [
              { label: "Animals", value: "animals" },
              { label: "Food", value: "food" },
            ],
        }
      - { label: "Title", name: "title", widget: "string", required: true }
      - {
          label: "Description",
          name: "description",
          widget: "string",
          required: false,
        }
      - {
          label: "Cover Image",
          name: "cover",
          widget: "image",
          required: false,
          allow_multiple: false,
        }
      - { label: "Content", name: "body", widget: "markdown", required: false }
      - {
          label: "Gallery",
          name: "gallery",
          widget: "list",
          required: false,
          summary: "{{fields.image}}",
          field: { label: "Image", name: "image", widget: "image" },
        }
```
