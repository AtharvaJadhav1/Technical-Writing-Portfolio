# Documentation Automation — Project Brief

## Purpose

Documentation can become inconsistent as a software project changes. A lightweight validation script can catch basic maintenance problems before documentation is published.

This file describes a proposed portfolio project. It is a project brief, not a claim that the utility has already been implemented.

## Proposed capabilities

The first version should be deliberately small and should:

1. Find Markdown files under a chosen documentation directory.
2. Check for required headings in selected documents.
3. Detect empty or placeholder sections.
4. Validate relative links to files in the repository.
5. Print a readable summary showing passed checks and problems found.

## Suggested implementation

- **Language:** Python 3
- **Input:** A repository or documentation directory
- **Output:** A terminal validation report
- **Dependencies:** Prefer the Python standard library for the first version.

## Example usage (planned)

```bash
python check_docs.py .
```

The command above is an intended interface. It should be documented as usable only after the script is implemented and tested.

## Validation rules to define

| Check | Expected behaviour |
|---|---|
| Markdown discovery | Find relevant `.md` files recursively |
| Required headings | Report configured headings that are missing |
| Empty sections | Flag headings with no meaningful content before the next heading |
| Relative links | Report local targets that do not exist |
| Report summary | Show total files checked and issues by category |

## Testing plan

Before describing the utility as complete:

- Create a small fixture directory with valid and invalid Markdown files.
- Test nested relative links.
- Test links containing anchors.
- Test documents with missing and empty sections.
- Confirm the script exits with a non-zero status when validation fails.
- Record the Python version used for testing.

## Limitations to document

The initial version is not intended to validate external URLs, render Markdown, or determine whether technical statements are factually correct. Those checks require separate tools or human review.

## Implementation status

**Status: Planned.** Update this section only after the script exists, its behaviour has been tested, and the instructions above match the implementation.
