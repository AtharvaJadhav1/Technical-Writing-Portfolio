# Markdown Documentation Checker

> **AI-assistance disclosure:** This utility and this project README were created with AI assistance. They demonstrate a small documentation-tooling project; they are not an unaided writing sample for an application that prohibits AI assistance.

## What it checks

The command-line tool scans Markdown files and reports:

- Broken relative file links and local heading anchors.
- Empty sections.
- Placeholder markers such as `TODO`, `TBD`, and `FIXME`.
- Required headings, when supplied by the user.
- A text report or machine-readable JSON output.

It uses the Python standard library and does not make network requests.

## Requirements

- Python 3.10 or later.

No third-party Python packages are required.

## Run the checker

From the root of this repository:

```bash
python automation/check_docs.py .
```

Check for a required heading in every Markdown file:

```bash
python automation/check_docs.py . --required-heading "Overview"
```

Print a JSON report:

```bash
python automation/check_docs.py . --format json
```

The command exits with:
- `0` when no issues are found.
- `1` when one or more documentation issues are found.
- `2` when the supplied path cannot be read.

## Run the tests

```bash
python -m unittest discover -s automation/tests -v
```

The test suite covers valid local links and anchors, broken links, empty sections, missing required headings, placeholders, and links inside fenced code blocks.

## Scope and limitations

- Only Markdown files are scanned.
- Relative inline links and local heading anchors are checked; reference-style Markdown links are not currently parsed.
- External URLs are not requested or checked.
- The heading-anchor algorithm is intentionally lightweight and may differ from some Markdown renderers in edge cases.
- A passing report checks document structure and local references. It does not establish that technical statements are correct or that instructions work. Human review and product testing are still required.

## Project files

- `check_docs.py` — command-line validator.
- `tests/test_check_docs.py` — standard-library unit tests.

## Verification

The included tests were run with Python's `unittest` runner. Re-run the test command above after changing the checker.
