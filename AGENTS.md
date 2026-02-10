# AGENTS.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

R-Syntax-Workshop-2026 is an interactive R programming tutorial series designed for teaching R syntax fundamentals through modular, self-contained Shiny applications. The project consists of seven R Markdown documents that compile into interactive learnr tutorials with embedded code exercises and quizzes.

### Architecture

The project uses a **modular tutorial architecture** where:
- Each part (P1 through P7) is an independent R Markdown document using the `learnr` framework
- R Markdown files compile to HTML documents via `knitr` and the `learnr` runtime engine
- The RStudio project file (`R-Tutorial-Intro-To-R-Syntax.Rproj`) configures editor settings and project metadata
- Interactive code blocks are fully functional R sessions that can maintain state between chunks via `learnr` references
- All dependencies are built into the tutorial format (zero external setup required for participants)

### Content Structure

The seven-part series covers:
- **P1**: Operators, Variables, and Built-in Functions
- **P2**: Vectors in R (fundamental data structure)
- **P3**: Matrices and Arrays
- **P4**: Lists
- **P5**: DataFrames
- **P6**: User Functions and Programming (control flow basics)
- **P7**: Base R Graphics

The tutorials emphasize the "dollar sign" R syntax (as opposed to formula syntax or tidyverse syntax) for consistency and focus on understanding core language patterns rather than recipe-based learning.

## Working with Tutorial Content

### Rendering Tutorials

To compile an `.Rmd` file into an interactive HTML tutorial:

1. **From RStudio**: Open the `.Rmd` file and click the "Run Document" button (top right of editor)
2. **From command line**: Use `rmarkdown::render("P1_OperatorsVarsBuiltIns.Rmd")` in R
3. Output: HTML files are generated in the same directory (e.g., `P1_OperatorsVarsBuiltIns.html`)

### Rendering All Tutorials

To batch render all tutorials in sequence (creates all HTML output files):
```r
tutorials <- list.files(pattern = "^P[0-9]+.*\\.Rmd$")
for (file in tutorials) {
  rmarkdown::render(file)
}
```

## Key Dependencies and Structure

- **Framework**: `learnr` (interactive tutorials with exercises)
- **Document format**: R Markdown (`.Rmd` files)
- **Rendering engine**: `rmarkdown` + `knitr`
- **Bibliography**: `bib.bib` (shared across tutorials via YAML frontmatter `bibliography: bib.bib`)
- **Image assets**: `images/` directory (referenced in tutorials)
- **Runtime context**: `shiny_prerendered` (R code chunks are pre-executed, making tutorials deployable)

## YAML Configuration Notes

Each `.Rmd` file contains a YAML header that configures:
- `learnr::tutorial` output format with theme (`spacelab`), editor theme (`dawn`), and syntax highlighting (`pygments`)
- `progressive: true` (sections are revealed as user progresses)
- `allow_skip: true` (users can skip exercises)
- `toc: true` with depth for automatic table of contents generation
- `runtime: shiny_prerendered` (for Shiny server deployment compatibility)

## Code Block Types

- **Demonstrative blocks** (`{r setup, include=FALSE}`): Hidden setup code (libraries, chunk options)
- **Display blocks** (`{r example, echo=TRUE}`): Show results without interactivity
- **Exercise blocks** (`{r exercise-name, exercise=TRUE}`): Interactive code editors for users to modify and run
- **Quiz blocks** (`{r quiz-name, exercise=TRUE, exercise.lines=1}`): Single-line exercises or validation checks

## Important Development Notes

- **Exercise state preservation**: `learnr` persists user progress and code across browser sessions; participants can return to tutorials in the same state they left them
- **Comments in code**: Use `#` for inline documentation within code blocks
- **Bibliography references**: Inline citations using `[@key]` syntax reference entries in `bib.bib`
- **Emphasis on patterns**: Focus content on "why R works this way" rather than reference documentation
- **Two-session structure**: Workshop is typically delivered as Part 1-3 in one session, Part 5+ in a follow-up session

## Editing and Maintenance

When modifying tutorial content:
1. Edit the `.Rmd` source file directly
2. Test individual code blocks by rendering a quick preview
3. Render the full document to generate updated HTML
4. Commit both `.Rmd` and `.html` files (the HTML is generated output and versioned for accessibility)

The emphasis should remain on clarity of R syntax concepts and interactive learning without requiring complex setup from workshop participants.
