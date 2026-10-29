# Evaluation

## Reflection (985 characters, including spaces)

The form was evaluated with a heuristic review and browser checks, rather than a participant study. The review focused on clear wording, error prevention and consistency. Required fields are marked, while optional details can be skipped. Each control has a label, related choices use fieldsets, and hints explain the rules before submission. Keyboard checks covered the skip link, Tab order, radio buttons, the slider and visible focus. Native validation rejected empty required fields, an invalid email, a weak password, an out-of-range birth date and an invalid budget. The layout was checked at 320, 390 and 768 pixels, with no horizontal overflow. Text contrast was also calculated. The review led to clearer field hints and a fix to the agreement error message. A remaining limitation is that HTML checks cannot verify email ownership or username availability. The form therefore ends with a demo confirmation. A useful next step would be testing it with people outside the group.

## Method and scope

A heuristic review, browser interaction checks, source inspection and contrast calculations were performed. This was not a participant usability study, a screen reader test, an axe audit or a Lighthouse audit. Responsive checks used browser frames at the stated widths, not physical mobile devices. Browser checks were performed in Chrome on 29 October 2026.

## Recorded results

| Check | Observation |
| --- | --- |
| Submit an empty form | Submission blocked; focus moved to the username; inline errors appeared. |
| Username `a!` | Rejected by the username pattern. |
| Email `wrong-email` | Rejected by the email input. |
| Password `weak` | Rejected by the password pattern. |
| Birth date `2010-01-01` | Rejected by the date maximum. |
| Budget `5001` | Rejected by the maximum and step restrictions. |
| Budget `55` | Rejected by the step restriction. |
| Correct required values, optional fields blank | Form validity passed. |
| Correct submission | Opened `complete.html?site-use=both`; no personal input values in the URL. |
| Username followed by Tab | Focus moved to email; visible outline measured 3 CSS pixels. |
| Space on Beer | Checkbox toggled. |
| ArrowRight on Browse ratings | Selection moved to Write reviews. |
| ArrowRight on the slider | Value changed from 3 to 4. |
| Skip to content | Moved focus to the main element. |
| 320 / 390 / 768 px containers | Document width matched its available width; no horizontal overflow. |
| Labels | All 22 controls had a visible label. |
| Source | No script elements, JavaScript event attributes, external libraries or JavaScript files. |

The preview environment may inject its own support script. This is not part of the project files or the archive.

## Contrast calculations

| Pair | Contrast ratio |
| --- | --- |
| Main text `#2c2526` on white | 15.00:1 |
| Hint text `#62595b` on white | 6.78:1 |
| Hint text `#62595b` on `#f4f1ee` | 6.02:1 |
| White on the burgundy button `#6c2737` | 10.59:1 |
| Error text `#a11c2f` on white | 7.71:1 |
| Input border `#8a8284` on white | 3.75:1 |

These calculated colour pairs do not establish full accessibility compliance.

## Iterations

- Kept error styling off untouched fields and used `:user-invalid` for feedback after interaction or submission.
- Used permanent hints for field requirements; hidden error text is not referenced as a hint on untouched fields.
- Fixed the agreement layout so its error text responds to the checkbox validity state.
- Made the main element focusable as the target of the skip link.
- Embedded fonts in the wireframe PDFs after inspecting the first render.

## Limitations and next checks

The form is a static prototype. It cannot create accounts, verify email ownership, check unique usernames or upload files. File `accept` values are picker hints rather than content validation. The date maximum is fixed to the preparation date. `:user-invalid` behaviour and native error wording can vary across browsers.

Before hand-in, the group should repeat the checks, try a second browser and test on an actual phone. A useful usability task is: create a sample account, select two categories and correct an invalid budget. Record real observations if this is done; do not invent participants or results.
