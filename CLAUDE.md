# InvestRand Project Instructions

## SVG to PDF Conversion (Critical)

When converting SVG presentations to PDF, there is a **scaling issue** that causes fonts to become unreadable.

### The Problem

| SVG Source | PDF Output | Scale Factor |
|------------|------------|--------------|
| 1920 × 1080 px (viewBox) | 960 × 540 points | **50%** |

The standard PowerPoint widescreen size is 960 × 540 points. When we scale SVG content from 1920×1080 to fit this size, everything shrinks by 50% — including fonts.

**Result:** A 16px font in the SVG becomes 8px in the PDF — unreadable.

### The Solution

Design SVGs with fonts **2x larger** than the target rendered size:

| Target Rendered Size | SVG Source Size |
|---------------------|-----------------|
| 36-40px (titles) | 72-80px |
| 18-20px (headers) | 36-40px |
| 14-16px (body) | 28-32px |
| 12-14px (captions) | 24-28px |

### Conversion Commands

```bash
# Convert each SVG to PDF (scales content to 960x540)
for f in *.svg; do
  rsvg-convert -f pdf --width 960 --height 540 -o "${f%.svg}.pdf" "$f"
done

# Combine into single PDF
gs -dBATCH -dNOPAUSE -q -sDEVICE=pdfwrite \
   -sOutputFile=OutputName.pdf \
   slide1.pdf slide2.pdf slide3.pdf [etc...]

# Clean up individual PDFs
rm -f *.pdf  # Be careful - exclude your combined PDF first
```

### Key Points

1. **Do NOT use `--page-width/--page-height`** — this only sets page size, doesn't scale content (causes cropping)
2. **Use `--width/--height`** — this actually scales the SVG content to fit
3. **Font sizes in SVG must be 2x target** — because of 50% scale to PowerPoint dimensions
4. **Dense slides need simplification** — if content doesn't fit with larger fonts, reduce content rather than shrinking fonts
