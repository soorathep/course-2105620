# Annual course archive

Prepare a complete, versioned snapshot of course 2105620 at the end of each
academic year. The working repository is `soorathep/course-2105620`. The original
pages and media on `skhgroup.net` and existing Test releases remain compatibility
resources. Archiving does not authorize changing, redirecting, or removing them.

This document defines the preparation process. It does not schedule a job,
start an archive of the current term, or authorize Zenodo publication. No Zenodo
record was published by the course migration.

## 1. Define and freeze the annual edition

- Confirm the academic-year label, teaching cutoff, course title, and edition
  version with the course owner. Do not infer the academic year from the date.
- Record the dedicated repository URL, full source commit SHA, site URL, build
  workflow, and preparation date. Keep uncommitted work separate and preserved.
- Prepare an independent local package from the selected commit. Do not modify
  a published archive, another actor's checkout, or the live course to assemble it.
- Keep a private preparation record with the source inventory, missing items,
  review decisions, and any exclusions. Do not push an archive tag or create a
  release as a substitute for approval.

## 2. Assemble the complete teaching snapshot

Use an explicit course inventory rather than copying an entire working folder.
Include:

- The full year's student-facing pages and rendered slides, including their
  scripts, styles, fonts, images, and shared runtime modules.
- Editable course sources from `_teaching-src/2105620/`, the required parts of
  `_teaching-src/shared/`, figure-generation code, and synthetic teaching inputs.
- Student handouts, notebooks, permitted assessment materials, transcripts,
  printable PDFs, and every audio or video file required to use the edition.
- The course data and necessary site configuration, layouts, shared assets,
  link-repair tools, dependency versions, and build instructions. Inventory
  shared files by actual use; do not include unrelated lab records by default.
- An offline entry point, instructions for any required local web server, and a
  mapping from original URLs to packaged paths. Test navigation and media with
  internet access disabled. Offline adjustments belong inside the prepared
  package and must not change live URLs or feedback backends.

### Known editable-source supplement

The 2026 migration includes the rendered review, but its editable review source
is still in the owner's ResCom working folder. The annual inventory must include
`quarto/review90.qmd`, `quarto/files/review90/narration.json`, its timeline,
the supporting theme/player files, figure code and synthetic inputs, and the
figure/audio/reader build scripts. Review private instructor notes before any
public inclusion. Preserve the working originals and record their source hashes.
A repository ZIP without this supplement is not a complete regenerable review.

Download required external media into the package as actual files. A list of
links, a GitHub source ZIP, or a Git LFS pointer is not a complete snapshot.
Record each external file's original URL, retrieval date, local path, byte count,
and SHA-256. Check that it is the intended version and that it may be included.

The known 2026 review audio is an external dedicated-Release dependency:

- URL: `https://github.com/soorathep/course-2105620/releases/download/2105620-review90-20261111-r2/review90_narration.m4a`
- Size: 42,994,270 bytes.
- SHA-256: `cc4295018d0564b10e76dbb7c45aaa6f5042586fa23562a0df176c6f259dccf6`.

Re-inventory the actual media used by the selected annual edition. Do not assume
that this baseline remains the current recording in later years. Both 2026
recordings are preserved in the dedicated repository's Releases. The owner
authorized retiring their Test-hosted copies after checksum verification on
2026-11-15; use the dedicated URLs in current material and annual inventories.

If a required file is missing, inaccessible, or not cleared for redistribution,
mark the package **incomplete** and report the gap. State which dependencies are
not bundled and whether this limits offline use or regeneration. Never describe
an incomplete collection as a complete annual snapshot.

## 3. Review personal data and reuse rights

Create a private, file-by-file review report before requesting publication:

- Check visible content and file metadata for student names, IDs, email
  addresses, identifiable feedback, grades, submissions, recordings, and other
  personal information. Public author credits are a separate, explicit decision.
- Exclude secrets, access tokens, private configuration, live databases, student
  responses, grades, and unpublished assessment answers from the public package.
- Preserve excluded originals in their authorized private location. Keep a
  private inventory and hashes where appropriate; do not expose identifying
  filenames or sensitive review findings in the public manifest. Preparation is
  not permission to delete or silently overwrite an original.
- Review third-party papers, figures, fonts, media, code, synthetic voices, and
  other contributions. Record the source, creator, license or permission,
  required credit, and the owner's inclusion decision. Do not assume that public
  availability grants redistribution rights or assign one license to everything.
- Preserve feedback-form functionality on the live site. Archive only a cleared
  blank form, schema, or instructions explaining its purpose and backend
  dependency. Do not export response data or claim an offline form submits to
  the original service.

Keep unresolved personal-data or rights decisions as publication blockers. Any
replacement, redaction, or restricted-access component needs a documented owner
decision, with the package's completeness limits stated accurately.

## 4. Prepare metadata, credits, and checksums

Prepare the archive's title, academic year, edition version, description, course
code, creators and contributors, affiliations, supplied public identifiers,
keywords, language, licenses, credits, related links, source commit, and file list.
Do not invent identifiers, permissions, licenses, or a DOI. Include a clear
description of the teaching scope and known limitations.

Include `README`, `CREDITS`, the required license and permission notices, an
asset manifest, build/offline instructions, and `SHA256SUMS` for the packaged
payload. Generate checksums from the final bytes and verify them after extracting
the package; do not include `SHA256SUMS` in its own entries. Keep the archive-file
SHA-256 and the final metadata SHA-256 outside
the archive as part of the private review receipt. Rebuild the checksums and
receipt whenever any approved file changes.

## 5. Obtain approval and publish the exact edition

Present the complete package, metadata, credits, checksums, offline/link test
results, private-data review outcome, rights decisions, and unresolved issues to
the course owner. Obtain explicit approval for the exact archive and metadata
hashes before publishing. Keep the unapproved package and review information
private. Do not publish automatically through an API, a GitHub release
trigger, or a GitHub-Zenodo integration.

Proceed only within that approval. A changed payload or metadata requires a new
review and approval for its new hashes. Archiving or publication never authorizes
removing current-year pages, legacy media, private originals, or older editions.

## 6. Verify the published version and add its DOI link

After an approved publication, verify the public Zenodo record's title, academic
year, creators, version, licenses, and file list. Download the published package,
compare its SHA-256 with the approved archive, extract it, and verify
`SHA256SUMS`. Retain the publication and download-verification receipt.

Only then add an annual archive entry to the course site with the verified
**version-specific DOI**, academic year, version, and relevant credits/license
information. A draft, a reserved identifier, or a concept DOI alone does not
satisfy this requirement. Keep the current course and existing links available,
and test the DOI and downloads after the site deployment.
