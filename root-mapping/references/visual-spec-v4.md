# Root Map Visual Spec v4.0

Quick-reference for the visual rules in `root-map-template-v4.html`. **The template CSS is the single source of truth** — this file exists so you can check rules without parsing minified CSS. If anything here conflicts with the template, the template wins.

## Color System

### Node types
| Element | Background | Border | Text | Dark mode adjusts all via `prefers-color-scheme` |
|---------|-----------|--------|------|--------------------------------------------------|
| Outcome (blue) | `--b50` #E6F1FB | `--b400` #378ADD (2px solid) | `--b800` #0C447C | Yes |
| Root outcome | Same as outcome | 3px solid | Same | Yes |
| Need (coral) | `--r50` #FAECE7 | `--r200` #F0997B (1px solid) | `--r800` #652710 | Yes |
| Business (amber) | `--a50` #FAEEDA | `--a200` #EF9F27 (1px solid) | `--a800` #573F08 | Yes |
| Solution (teal) | `--t50` #E1F5EE | `--t200` #5DCAA5 (1px solid) | `--t800` #07473A | Yes |
| Expansion (purple) | `--e50` #EEEDFE | `--e400` #7F77DD (2px dashed) | `--e800` #3C3489 | Yes |
| Non-EVS | Same as outcome | `--b200` #85B7EB (2px dashed) | Same, 78% opacity | Yes |

### Indicators
| Indicator | Color | CSS var |
|-----------|-------|---------|
| High confidence / strong effectiveness | Green | `--hi` #18865F |
| Medium / adequate | Amber | `--mi` #B07E0B |
| Low / unproven | Red | `--lo` #B33434 |
| Neutral (minor severity) | Gray | `--neu` #8A8983 |

### Severity dots
3 dots per need card. Lit dots use indicator colors above. Unlit dots: `--r200` at 20% opacity.
- 3 dots lit (severe) → `--lo` red
- 2 dots lit (moderate) → `--mi` amber  
- 1 dot lit (minor) → `--neu` gray

### Competitive differentiation tags
| Tag | Class | Background | Text |
|-----|-------|-----------|------|
| Differentiated | `.dd` | #E1F5EE | #0A5C43 |
| Table stakes | `.dts` | `--g50` | `--tm` |
| Battleground | `.dbg` | #FFF3DB | #6B4E00 |
| Uncontested | `.du` | #EDE9FE | #4E3D9E |
| Behind | `.dbh` | #FEE9E9 | #7A1D1D |

## Typography

- **Primary font**: `-apple-system, 'SF Pro Text', 'Helvetica Neue', sans-serif` (`--fn`)
- **Display font**: `-apple-system, 'SF Pro Display', 'Helvetica Neue', sans-serif` (`--fnd`)
- **Toolbar h1**: 15px, weight 600, letter-spacing -.02em (display font)
- **Outcome label**: 12px, weight 600, letter-spacing -.01em (display font)
- **Root outcome label**: 15px (same style, bigger)
- **Need card text**: 8px, line-height 1.35
- **Severity label**: 7px, weight 600
- **Solution/business card**: 8px
- **Solution name**: 9px, weight 600
- **Solution tech note**: 7px, 55% opacity
- **EVS badge**: 6px, weight 700, 4px tracking
- **Diff tag**: 7px, weight 600

## Layout Engine

- **Node width** (`NW`): 230px
- **Node gap** (`NG`): 35px
- **Row Y positions** (`RY`): [50, 620, 1040] — root, categories, features
- **Zone width**: `max(NW+12, childCount*(NW+NG)-NG+12)`
- **Zone gap**: NG + 15px between categories
- **Root positioning**: auto-centered above midpoint of all categories, 280px wide
- **Canvas padding**: 40px left margin for zones

## Node Container (`.ng`)
- Background: `--cbg` (rgba black 2%)
- Border: 1px solid `--cbd` (rgba black 6.5%)
- Border-radius: 12px
- Padding: 6px
- Hover: translateY(-2px), box-shadow 0 8px 28px rgba(0,0,0,.07)
- Selected: white background, `--bd` border, elevated shadow
- Expansion container: 14px radius, `--e50` at 40% mix, 2px dashed `--e400` border

## Card Stacking Order (within each node container)
1. **Need card** (coral) — top, above outcome
2. **Outcome card** (blue) — middle, the primary element
3. **Business outcome cards** (amber) — below outcome
4. **Solution cards** (teal) — bottom, below business

Cards are stacked vertically with 4px margin-bottom between them (2px for solution/biz).

## Arrows
- Connect node groups upward only (child → parent)
- EVS: `--arr` #B8B7B2, 1.8px stroke width
- Non-EVS: `--arrd` #CDCCC8, 1.2px, dash pattern `8 5`
- Expansion: `--e400`, 2px, dash pattern `10 6`
- Arrowhead: chevron marker, 6×6px
- Path: cubic bezier, midpoint Y control points

## Detail Panel
- Width: 400px, slides from right
- Background: white (`#fff`), dark mode: `#1E1E1C`
- Border-left: 1px solid `--bd`
- Transition: 0.3s cubic-bezier(.4,0,.2,1)
- Header: 22px display font, weight 600, -.025em tracking
- Sections: 9px uppercase label, 13px body text
- Sources box: `--g50` background, 8px radius
- Notes box: `--a50` background, 3px `--a200` left border (amber)
- Expansion notes: `--e50` background, 3px `--e400` left border (purple)

## Zoom & Pan
- Initial: fit-to-viewport (calculates scale from content bounding box)
- Scroll zoom: ±2% per tick, zoom-to-cursor
- Button zoom: ±8%
- Min scale: 0.05, max: 2.0
- Reset: re-fits to viewport

## v4 Additions

### Star Badge
- `.star-badge`: 8px gold `★` character, `#C8940A` light / `#E8B84A` dark
- Positioned after outcome label text with `margin-left:3px`

### Indicators (Detail Panel)
- `.ind-list` / `.ind-item`: 12px text, 5px dot bullet via `::before`, `--bd` color
- Shown in detail panel for `indicators[]` and `bizIndicators[]` fields

### Add/Remove (Detail Panel)
- `.dp-add`: 11px link-style button, `--b600` color, underline on hover
- `.dp-rm`: 9px `✕` button, `--tl` at 40% opacity, red on hover (`--lo` + `--r50` background)
- `.dp-act-bar`: action section with "Add child outcome" button, top border separator

### Sub-Feature Support
- Layout engine detects features whose `parent` is another feature (not in `catCh`)
- Adds a 4th row at `RY[2]+420` for sub-features
- Sub-features positioned centered below their parent feature

### Responsive
- Detail panel: full-width on viewports ≤600px
- `prefers-reduced-motion`: disables node hover transitions and panel slide animations

### Accessibility
- Zoom and close buttons have `aria-label` attributes
- Node containers have `role="button"`, `tabindex="0"`, `aria-label`
- Enter key opens detail panel on focused node; Escape closes it
- Focus rings use `outline:2px solid var(--b400)` instead of `outline:none`
- Minimum text sizes: need cards 10px, severity 9px, EVS badge 8px, diff tags 9px, biz/sol cards 10px
