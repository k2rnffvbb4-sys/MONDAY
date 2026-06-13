MONDAY — Design Principles & Visual Specification

1. Design Philosophy
Decision-first density. Every surface exists to surface signal, not decoration. Information is the aesthetic.

Dark-native. The application is built for extended professional use. Light is reserved for emphasis, not background.

Teal leads, purple supports. A two-accent system where teal (#00C8C8) drives action and status, purple (#9B6FE8) marks knowledge and reflection. They never compete — they annotate different layers of meaning.

Controlled motion. Transitions confirm state changes. Nothing animates without a reason.

2. Color System
Base Palette
Token	Hex	Role
--background	#13141A	Application canvas
--surface-01	#1C1D24	Primary card / panel surface
--surface-02	#22232C	Elevated card, modal, drawer
--surface-03	#2A2B35	Hover state, subtle highlight
--border	#2E2F3A	All structural dividers
--border-subtle	#232430	De-emphasised separators
Foreground
Token	Hex	Role
--text-primary	#F0F0F5	Headings, primary labels
--text-secondary	#9899A6	Supporting copy, metadata
--text-muted	#5A5B68	Disabled, placeholder, ghost
Accent — Teal (Action layer)
Token	Hex	Role
--teal	#00C8C8	Primary CTA, active state, live indicator
--teal-dim	#00C8C820	Teal background wash (badges, highlights)
--teal-border	#00C8C840	Teal-tinted border
Teal signals: action, status, connection, live data, open state.

Accent — Purple (Knowledge layer)
Token	Hex	Role
--purple	#9B6FE8	Principles, knowledge, AI, review
--purple-dim	#9B6FE820	Purple background wash
--purple-border	#9B6FE840	Purple-tinted border
Purple signals: learning, reflection, AI-derived content, knowledge objects.

Semantic Status Colors
Token	Hex	Role
--positive	#22C55E	Positive outcome, healthy state
--negative	#EF4444	Negative outcome, error
--warning	#F59E0B	Mixed, stalled, caution
--neutral	#6B7280	Unknown, inactive
Decision Lifecycle Colors
Status	Color	Hex
OPEN	Teal	#00C8C8
DECIDED	Blue	#3B82F6
REVIEWING	Purple	#9B6FE8
CLOSED	Green	#22C55E
3. Typography
Typefaces
Role	Family	Weights
Headings	Nunito	600, 700
Body / UI	DM Sans	400, 500
Monospace / IDs	System mono	400
Scale
Token	Size	Line Height	Weight	Usage
text-xs	11px	1.4	400	Timestamps, metadata, badges
text-sm	13px	1.5	400/500	Secondary labels, table cells
text-base	14px	1.6	400	Body copy, form inputs
text-md	15px	1.5	500	Card titles, widget headers
text-lg	18px	1.4	600	Section headings
text-xl	22px	1.3	700	Page titles
text-2xl	28px	1.2	700	Dashboard stat numbers
Rules
Headings use Nunito. All other text uses DM Sans.
Stat numbers (widget counts, metrics) use Nunito 700 at large scale.
Monospace only for IDs, timestamps in data tables, and code.
Letter-spacing: -0.01em on headings, 0 on body.
4. Spacing & Layout
Base Unit
4px grid. All spacing is a multiple of 4.

Common Tokens
Token	Value	Usage
space-1	4px	Tight internal padding
space-2	8px	Icon-to-label gap, badge padding
space-3	12px	Card internal padding (compact)
space-4	16px	Standard card padding
space-5	20px	Section internal padding
space-6	24px	Card-to-card gap
space-8	32px	Section gap
Grid
Dashboard grid: 24 columns, 48px row height, 10px gap
Content pages: Single column, max-width 960px, centered
Sidebar: Fixed 240px width
Drawer: 35–45% viewport width, full browser height, slides from right
Border Radius
Token	Value	Usage
radius-sm	4px	Badges, tags, small chips
radius-md	8px	Cards, inputs, buttons
radius-lg	12px	Modals, panels, drawers
radius-xl	16px	Large feature cards
5. Component Patterns
Cards
Background: --surface-01 Border: 1px solid --border Border-radius: radius-md (8px) Padding: 16px Hover: background → --surface-02, border → --border subtle teal tint Shadow: none (flat design — borders define depth)
Active / selected card adds border-color: --teal-border and a 2px left accent bar in --teal.

Buttons
Variant	Background	Text	Border
Primary	--teal	#13141A	none
Secondary	--surface-02	--text-primary	--border
Ghost	transparent	--text-secondary	none
Destructive	#EF444420	#EF4444	#EF444440
Purple (AI/knowledge)	--purple-dim	--purple	--purple-border
Button height: 32px (compact), 36px (standard). Border-radius: 6px. Font: DM Sans 500 13–14px.

Badges / Status Pills
Height: 20px Padding: 2px 8px Border-radius: 4px (radius-sm) Font: DM Sans 500 11px uppercase tracking-wide
Each status has a paired dim background and full-opacity text color from the semantic palette.

Inputs
Background: --surface-02 Border: 1px solid --border Border-radius: 6px Height: 36px Padding: 0 12px Font: DM Sans 400 14px --text-primary Placeholder: --text-muted Focus: border-color → --teal, box-shadow → 0 0 0 2px --teal-dim
Modals / Dialogs
Background: --surface-02 Border: 1px solid --border Border-radius: radius-lg (12px) Max-width: 560px Overlay: rgba(0,0,0,0.6) backdrop-blur(4px)
Drawers (side panels)
Background: --surface-01 Border-left: 1px solid --border Width: 35–45% viewport Height: 100vh Position: fixed right-0 top-0 Transition: transform 200ms ease-out
Data Tables
Header row: --surface-02, text --text-secondary, font DM Sans 500 11px uppercase Body rows: --surface-01, border-bottom 1px --border-subtle Row hover: --surface-02 Cell padding: 10px 16px
6. Iconography
Library: Lucide React exclusively
Size: 14px (inline/badge), 16px (standard UI), 20px (section headers), 24px (empty states)
Color: inherits from parent text color — never independently colored except for status icons
Status icons use their semantic color directly (--teal, --positive, --negative, etc.)
7. Motion
Principles
Purposeful only. No decorative animation.
Fast. UI transitions: 150–200ms. Content entrance: 250–350ms.
Ease-out default. Things arrive quickly and settle. Nothing lingers.
Standard Transitions
Interaction	Duration	Easing	Property
Button hover	150ms	ease-out	background, border-color
Card hover	150ms	ease-out	background, border-color
Modal open	200ms	ease-out	opacity, scale (0.97→1)
Drawer slide	200ms	ease-out	transform (translateX)
Tab switch	150ms	ease-out	opacity
Widget drag	0ms	—	transform (no transition while dragging)
Widget drop	200ms	ease-out	transform settle
Status badge change	200ms	ease-in-out	background, color
Entrance Animations (content load)
Initial: opacity 0, translateY 8px Animate: opacity 1, translateY 0 Duration: 300ms Easing: ease-out Stagger: 40ms between list items
8. Information Hierarchy
Layering Model
Layer 0 — Canvas: #13141A (background) Layer 1 — Base surface: #1C1D24 (cards, panels) Layer 2 — Elevated: #22232C (modals, drawers, dropdowns) Layer 3 — Overlay: #2A2B35 (hover, active, tooltip) Layer 4 — Accent: teal / purple (interactive, semantic)
Depth is communicated through surface color progression, not shadow. No box-shadow on structural elements.

Visual Weight Rules
Teal draws the eye first — use it only for the most important interactive element per surface.
Purple is secondary — use it for AI-derived, knowledge, or reflective content.
White text (--text-primary) is reserved for labels that require immediate reading.
--text-secondary is the default for all supporting information.
--text-muted is for metadata, timestamps, and disabled states only.
9. Density Modes
MONDAY operates at compact density throughout.

Element	Compact value
Card padding	16px
Table row height	40px
Button height	32–36px
Input height	36px
Line height	1.4–1.6
Widget minimum height	2 grid rows (96px + gap)
There is no "comfortable" or "spacious" mode. The application is built for information workers who want maximum signal per viewport.

10. Transferability Notes
When applying this system to another application:

The color tokens are the system. Adopt the full token set — do not cherry-pick teal and purple without the surface stack. The accents only read correctly against #13141A.
Teal/purple semantic split must be preserved. If you use teal for knowledge content and purple for actions, the system inverts and loses meaning.
Flat depth model is non-negotiable. Adding shadows breaks the layering logic. Depth lives in surface color, not elevation.
Typography pairing is load-bearing. Nunito headings + DM Sans body creates the professional-but-approachable register. Swapping either changes the character significantly.
Compact density is intentional. Do not add padding to "breathe." The density is the product.
Completed




