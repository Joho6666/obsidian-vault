---
name: markitdown
description: Convert files and office documents to Markdown using Microsoft's MarkItDown. Use when you need to convert PDFs, Word documents, PowerPoint decks, Excel files, images, audio, HTML, CSV, JSON, XML, ZIP archives, EPUBs, or YouTube URLs into Markdown.
metadata:
  short-description: Convert many file types to Markdown with MarkItDown
---

# MarkItDown

Use Microsoft's MarkItDown when the user wants document content converted into Markdown for analysis, summarization, extraction, or downstream LLM use.

## When To Use

- Convert a local document to Markdown.
- Extract readable text from PDFs, Office files, images, audio, or web pages.
- Preserve structure such as headings, lists, tables, and links when converting.
- Produce Markdown output for later review or model input.

## Supported Formats

- PDF
- Word (`.docx`)
- PowerPoint (`.pptx`)
- Excel (`.xlsx`, `.xls`)
- Images with OCR and metadata
- Audio with transcription support
- HTML
- CSV, JSON, XML
- ZIP archives
- EPUB
- YouTube URLs

## Usage

Prefer `uvx` for one-off conversions. Pick the dependency group that matches the source type:

```bash
uvx 'markitdown[pdf]' input.pdf -o output.md
uvx 'markitdown[pptx]' slides.pptx -o slides.md
uvx 'markitdown[docx]' document.docx -o document.md
uvx 'markitdown[xlsx]' workbook.xlsx -o workbook.md
uvx 'markitdown[all]' input-file -o output.md
```

If the user wants a specific output file, use `-o`. If no output file is specified, write Markdown next to the source with a `.md` suffix.

## Notes

- Use the narrowest conversion option that fits the file type.
- Treat untrusted inputs carefully because MarkItDown can access local files and network resources.
- For very large or complex document workflows, consider breaking the input into smaller pieces before conversion.

## References

- Repository: https://github.com/microsoft/markitdown
- PyPI: https://pypi.org/project/markitdown/
