# Course 2105620 publishing rules

These rules add to the account lab standards.

## Repository and ownership

- This repository, `soorathep/course-2105620`, is the publication destination for
  Research Communication Skills for Chemical Engineers. Do not publish new
  course changes or media releases to `soorathep/Test`.
- Inspect status, remotes, publishing workflow and uncommitted work first. Use
  an isolated actor/task branch or checkout and record machine, task and base
  commit. Do not overwrite or discard another actor's changes.
- Never change an existing remote without first understanding its purpose.
  In particular, the shared Test repository still serves the research website
  and other courses. It is not an interchangeable course checkout.
- `COURSE_PUBLISHING.json` records the verified destination and media.

## Preserve student materials

- Preserve `teaching/2105620/`, editable `_teaching-src/2105620/`, shared runtime
  assets, videos, downloads, feedback links and their current functionality.
- On 2026-11-15 the owner explicitly authorized moving and deleting only course
  2105620 from Test after SHA-256 destination verification, including both audio
  Releases. Old skhgroup.net course links use a narrow main-site 404 browser
  redirect. Dedicated URLs are required for automated downloads and media.
  Preserve the main site, other courses, shared releases and local originals.
  Do not restore retired Test media links or rewrite shared Git history.
- Feedback forms may depend on their original authorized origin. Do not change
  a backend, origin, form action or authentication policy merely to change a URL.
  Test form loading without submitting entries or reading student responses.
- Preserve the project-site prefix `/course-2105620` and the current Pages
  workflow. Do not add the research website's CNAME to this repository.
- Do not replace the full course with a partial local Quarto source tree. Render
  Quarto with the public profile, strip private speaker notes, and review scoped
  outputs before copying them into the published tree.
- Keep secrets, grades, student submissions, private feedback and unpublished
  assessment keys out of public Git and website assets.

## Verify publication

- Test changed pages, navigation, media, downloads and feedback entry points.
  Distinguish confirmed broken links from authenticated or untested services.
- Wait for a successful GitHub Pages deployment and check the published site.
  Report changes, repository, commit, published URL and unresolved issues.
- Do not enable automatic Zenodo publication on GitHub releases. Use
  `ARCHIVING.md` for annual preparation, rights/personal-data review, exact-file
  approval, checksum verification and version-specific DOI linking.
- Do not publish an annual archive or remove old materials without the user's
  explicit approval. A prepared archive is not a published or verified DOI.
