# Exit ticket and feedback for 2105620

The course form is published at
<https://soorathep.github.io/course-2105620/teaching/2105620/exit.html>.
Use `?s=N` for a specific teaching week, with sessions 1–14 matching the course
schedule. The form also lets students choose their week and study mode.

## Editable material

- `_teaching-src/2105620/exit.html`: the form.
- `_teaching-src/2105620/exit-prompts.json`: the shared question source.
- `_teaching-src/2105620/figures/make_exit_qr.py`: regenerates fourteen QR PNGs
  and the closing includes for Weeks 1–6 and 8–10.
- `_teaching-src/2105620/_exit-wNN.qmd`: generated closing slides.
- `_teaching-src/2105620/assets/exit-ticket/`: generated QR images, graphite
  from the lab palette on white, with a four-module border and 600 dpi metadata.

Sessions 7 and 11–14 currently use a clearly worded fallback to the instructor's
question because their teaching decks are not present in this repository.
The substantive Week 8 and Week 9 exit-ticket activity slides remain in place.
Week 4 asks students to select **On my own** for the recorded session.

Regenerate after changing the question JSON:

```bash
cd _teaching-src/2105620
"$HOME/.venvs/research/bin/python" figures/make_exit_qr.py
```

Build a public Quarto output with instructor notes stripped. Keep `exit.html`
and `exit-prompts.json` in resources; QR images are covered by `assets/**`.
Stage only reviewed course files into the published directory. Preserve all
existing slide fragment IDs, shared runtimes, videos, downloads and review audio.

## Shared relay and private storage

The form posts to the existing Cloudflare `course-feedback-relay`. The shared
relay must allow course `2105620` with fourteen sessions. It stores answers in
the private `soorathep/course-feedback` repository under
`responses/2105620/sNN/`. The canonical relay source belongs with that private
feedback system. Do not maintain a second Worker implementation in this public
course repository.

Keep the existing relay, allowed origins and other course registrations.
Never place a GitHub token, Cloudflare credential or response data in public
HTML, JavaScript or Git. Changes to a shared choice value require matching form
and relay validation.

## Verification before teaching

Check all fourteen QR targets against the matching `?s=N` URL. Open the form
from the relevant slide and confirm the week, prompt, study-mode control,
validation, optional fields and successful-response message. Check mobile
layout, keyboard operation and failure recovery. Verify the GitHub Pages build
and deployed files.

Routine checks load the form without submitting it or reading student
responses. An explicitly authorized submission test should use identifiable
synthetic test wording, and any private receipt should expose only the exact
test submission. Report whether an end-to-end submission was actually tested.

## Privacy and compatibility

The form does not ask for names, student IDs or email addresses. Students should
leave personal details out of free text. Review actual relay behavior and
provider logging before making broader anonymity claims.

Student responses and their summaries stay in the private feedback system and
are excluded from course and Zenodo archives. The public archive may include
the blank form, question schema, source and instructions.

The previous Notion form and `assets/qr_feedback.png` remain compatibility
resources. The new form links to the previous form. Preserve those assets and
the old skhgroup.net pages unless the instructor explicitly approves a scoped
change after an impact check.
