# Alcohol Ranking Collection

WEB1 Second Project: a form for creating a community account.

The page uses HTML and CSS only. There are no frameworks, external fonts or JavaScript files.

## Open the project

Open `index.html` in a browser. Keep `style.css` and `complete.html` in the same folder.

## Files

- `index.html`: registration form, community rules and project description.
- `style.css`: colours, layout, focus states, error styling and mobile layout.
- `complete.html`: confirmation page for the form demo.
- `docs/wireframes.pdf`: desktop and mobile wireframes made before implementation.
- `docs/submission.pdf`: hand-in document with wireframes and evaluation.
- `docs/evaluation.md`: evaluation text and the checks performed.
- `GROUP_GUIDE_RU.md`: notes to help four group members understand the code.

## Form controls

The form contains text, email, password, telephone, date, number, range and file inputs, as well as dropdowns, a textarea, radio buttons and checkboxes.

The account, profile and preference sections use `fieldset` and `legend`. Every input has a label. Hints are connected using `aria-describedby` where useful.

## Validation

HTML attributes provide the checks:

- `required` prevents an incomplete submission.
- `type="email"` checks the email format.
- `pattern` checks the username and password rules.
- `min`, `max` and `step` limit the date and budget.
- `maxlength` limits the text fields.

CSS `:user-invalid` shows a border and an error message after interaction or submission. The browser also supplies its own validation messages. The form is usable with a keyboard, including arrow keys for the radio group and range slider.

## Demo behaviour

After valid input, the browser opens `complete.html`. No account is stored. The selected picture stays on the device.

Personal inputs intentionally have no `name` attribute, so their values are not sent in the demo's GET request. The radio buttons share `name="site-use"` to make them a single group; only this non-sensitive choice appears in the confirmation URL.

The form does not check username availability or email ownership. The `accept` attribute filters suggested image files; it does not verify file contents. There is no password confirmation field, because comparing two values requires logic beyond this HTML/CSS exercise.

The 18+ date cut-off is fixed to **29 October 2026** (`max="2008-10-29"`). Update the maximum date and the error wording before reusing the form on another date. The age limit is a community rule for this project.

## GitHub Pages

Target repository: https://github.com/hash1ro52/Second-Project

The website files belong in the repository root.

For GitHub Pages, go to **Settings > Pages > Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, and save. Use the actual URL shown by GitHub Pages in the PDF. Check that the URL works before hand-in.

The PDF has editable fields for the group members and the eventual website URL. Open it in a PDF reader, fill those fields, then save a copy before handing it in.

## References

- [HTML input reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input)
- [CSS :user-invalid](https://developer.mozilla.org/en-US/docs/Web/CSS/:user-invalid)
- [GitHub Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
