# Layout & ATS Review Reference

## Layout Rubric

Evaluate these separately from ATS parsing. Use them during focused layout reviews and whenever a broader review includes a PDF or image.

- **First-Glance Scanability**: Can a recruiter find the current title, company, and tenure in under 3 seconds?
- **Density & Whitespace**: Is the page too dense to read? Are margins adequate (usually 0.5" - 1")?
- **Bullet Size**: Are bullets strictly 1-2 lines? Any 3+ line bullet is a wall of text that will likely be skipped.
- **Section Ordering**: Is the most relevant section at the top (Education for New Grads, Experience for everyone else)?
- **Alignment**: Do dates align cleanly on the right margin?
- **Header Density**: Are headers distinct and recognizable?
- **Overflow & One-Page Fit**: Does it fit on one page without awkward widows/orphans or tiny font sizes (minimum 10pt)?
- **Link Presentation**: Are GitHub/LinkedIn links cleanly formatted without ugly tracking parameters?
- **Font Choice & Size**: Is the font a standard sans-serif (e.g., Arial, Calibri, Helvetica) at 10pt minimum? Decorative or uncommon fonts can cause parsing failures and hurt readability.

## ATS Compatibility Checklist

Apply these checks to ensure the resume parses correctly through applicant tracking systems:

- **No tables, columns, or text boxes** for critical content. Single-column layout is safest.
- **Standard section headings**: `Experience`, `Education`, `Skills`, `Projects`. Avoid creative alternatives like `Where I've Made Impact`.
- **No images, icons, graphs, or non-standard characters** (rating bars, stars, progress circles).
- **No headers or footers** for contact information — many parsers skip these regions.
- **File format**: PDF generated from a text source (Word, Google Docs, LaTeX). Not an image-based or scanned PDF.
- **Consistent date formats**: `Mon YYYY – Mon YYYY` or `YYYY – YYYY`. Avoid ambiguous formats.
- **No invisible text or white-on-white keyword stuffing** — modern ATS systems detect and penalize this.
- **Hyperlinks**: Include full URLs or keep them as plain text. Shortened or tracked URLs can break or look suspicious.
- **Keyword forms**: Include both acronyms and full terms (e.g., "AWS" and "Amazon Web Services") since some parsers only recognize one form.
- **Plain-text test**: Copy resume content into a plain text file — if information is missing or garbled, ATS will likely have trouble too.
