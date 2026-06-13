MONDAY — Dashboard Widget Inventory & Component Spec
Organizational Learning Area
Widget: Principles Captured
Property	Value
Icon	BookOpen (Lucide)
Icon size	16px
Icon color	--purple #9B6FE8
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Subtext	DM Sans 400 11px --text-muted
Accent bar	2px left border --purple
Background	--surface-01
Widget: Playbook Updates
Property	Value
Icon	BookMarked (Lucide)
Icon size	16px
Icon color	--teal #00C8C8
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Subtext	DM Sans 400 11px --text-muted
Accent bar	2px left border --teal
Background	--surface-01
Widget: Reviews Completed
Property	Value
Icon	ClipboardCheck (Lucide)
Icon size	16px
Icon color	--positive #22C55E
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Subtext	DM Sans 400 11px --text-muted
Accent bar	2px left border --positive
Background	--surface-01
Decision Pipeline Area
Widget: Active Decisions
Property	Value
Icon	GitBranch (Lucide)
Icon size	16px
Icon color	--teal #00C8C8
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Accent bar	2px left border --teal
Background	--surface-01
Widget: Awaiting Outcome
Property	Value
Icon	Clock (Lucide)
Icon size	16px
Icon color	--warning #F59E0B
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Accent bar	2px left border --warning
Background	--surface-01
Widget: Under Review
Property	Value
Icon	Search (Lucide)
Icon size	16px
Icon color	--purple #9B6FE8
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Accent bar	2px left border --purple
Background	--surface-01
Widget: Closed Decisions
Property	Value
Icon	CheckCircle2 (Lucide)
Icon size	16px
Icon color	--positive #22C55E
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Accent bar	2px left border --positive
Background	--surface-01
Activity & Feed Area
Widget: Recent Decisions Feed
Property	Value
Header icon	Activity (Lucide) 16px --teal
Row height	48px
Row border	1px bottom --border-subtle
Title	DM Sans 500 13px --text-primary
Meta line	DM Sans 400 11px --text-muted
Status badge	per lifecycle color table
Empty state icon	Inbox (Lucide) 24px --text-muted
Widget: Learning Loop Progress
Property	Value
Header icon	TrendingUp (Lucide) 16px --purple
Progress bar track	--surface-03
Progress bar fill	gradient --teal → --purple
Bar height	6px, border-radius 3px
Stage labels	DM Sans 400 11px --text-muted
Active stage label	DM Sans 500 11px --text-primary
Widget: Confidence Distribution
Property	Value
Header icon	BarChart2 (Lucide) 16px --text-secondary
HIGH bar	--positive #22C55E
MEDIUM bar	--warning #F59E0B
LOW bar	--negative #EF4444
Bar border-radius	3px
Label	DM Sans 400 11px --text-muted
Value	DM Sans 500 12px --text-primary
Capture & Intelligence Area
Widget: Pending Suggestions
Property	Value
Icon	Sparkles (Lucide) 16px --purple
Stat number	Nunito 700 28px --text-primary
Label	DM Sans 400 13px --text-secondary
Accent bar	2px left border --purple
Live indicator dot	6px circle --teal, pulsing opacity 1→0.4 2s infinite
Widget: Gmail Connection Status
Property	Value
Icon connected	Mail (Lucide) 16px --teal
Icon disconnected	MailX (Lucide) 16px --text-muted
Status text connected	DM Sans 500 12px --teal
Status text disconnected	DM Sans 400 12px --text-muted
Last sync	DM Sans 400 11px --text-muted
Connect button	Ghost variant, --teal text
Shared Stat Widget Anatomy
All single-metric stat widgets follow this structure:

┌─────────────────────────────────────┐ ← --surface-01, 1px --border │ ▌ [Icon 16px] Widget Title │ ← 2px accent bar + header row │ │ │ [Stat Number — Nunito 700 28px] │ ← primary metric │ [Label — DM Sans 400 13px] │ ← metric name │ [Subtext — DM Sans 400 11px muted]│ ← context / delta / last updated └─────────────────────────────────────┘ padding: 16px border-radius: 8px min-height: 96px
The 2px left accent bar color is the same as the widget's icon color. This is the only rule — icon color and accent bar color are always identical.

Icon–Color Assignment Rules (transferable)
Semantic meaning	Icon color token
Action / live / open	--teal
Knowledge / AI / reflection	--purple
Healthy / complete / closed	--positive
Stalled / waiting / caution	--warning
Error / negative	--negative
Neutral / metadata	--text-secondary
This mapping is the rule. When applying to another application, assign icon colors by semantic meaning — not by widget position or personal preference.

Completed




Continue building
(5/5)

