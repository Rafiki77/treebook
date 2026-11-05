# Woodland Star Photo Library

A shared photo library and dashboard for Woodland Star staff. It runs as a claude.ai page, so there is no server to host.

**Live page:** https://claude.ai/artifact/JLuU7nXfGEx8Tgysv3CiWn

## What it does

- **Overview:** total photos, photos added this week, staff contributing, photos that still need tags, photos by category, uploads per week, recent photos, popular tags and top contributors.
- **Library:** search and filter by category, tag and uploader. Open a photo to see its details, download it, or open it full size.
- **Upload:** drag and drop several photos at once and give the batch a category, date, tags and notes. Each title can be edited before uploading. Large photos are resized to 2560px on the longest side, and a small thumbnail is made for the grid.
- **Categories:** editors can add, rename, recolour and delete categories from the Overview page.

## Who can do what

| Role (claude.ai Share menu) | Can view | Can upload, edit and delete own photos | Can manage categories and edit or delete anyone's photos |
|---|---|---|---|
| Viewer / Commenter | No | No | No |
| Contributor (staff) | Yes | Yes | No |
| Editor / Owner | Yes | Yes | Yes |

People sign in with their claude.ai account. If your school uses Google sign-in for claude.ai, that is their school Google account.

## Data

- `categories/<id>`: `{ name, color, createdAt }`. Only editors can write these.
- `photos/<id>`: `{ title, category, tags[], notes, takenOn, asset, thumb, width, height, sizeBytes, originalName, uploader, createdAt }`.
  `asset` and `thumb` are file ids, served at `/_blob/<id>`.

## Updating

`index.html` in this folder is the published page. Edit it, then republish it to the same artifact URL.
