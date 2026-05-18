# DocuFlow — Enterprise Document Management Platform
## Design Manifest

**Figma File:** `O8Ub8UtjjfykaMXBSJY7AI`  
**File Name:** Doc-Approval-Platform  
**Target Resolution:** 1440 × 900 px (Desktop Web)

---

## Pages

| # | Page | Screens | Description |
|---|------|---------|-------------|
| 0 | 🎨 Foundations | — | Color tokens, typography scale, spacing, radius, shadow variables |
| 1 | 🧩 Components | 28 components | Button variants, badges, inputs, stat cards, file cards, sidebar |
| 2 | 🔐 Authentication | 5 screens | Login, OTP/MFA, Forgot Password, Reset Password, Reset Success |
| 3 | 📊 Dashboard | 2 screens | Main dashboard, Analytics & Reporting |
| 4 | 📁 Projects | 2 screens | Projects List, Project Detail |
| 5 | 📄 Documents | 4 screens | Documents List, Upload Modal, Upload Success, Document Detail |
| 6 | ✅ Review & Approval | 4 screens | Review Queue, Reject Modal, Approve Modal, Post-Approval Queue |
| 7 | 🔔 Notifications | 1 screen | Notifications centre |
| 8 | ⚙️ Admin Panel | 2 screens | Admin Panel, Branding & Customization |
| 9 | 🛡️ System Admin | 2 screens | System Admin overview, System Settings |
| 10 | 🔄 Prototype Flow | Flow map | All screens as scaled thumbnails with clickable prototype connections |

---

## Screen Inventory

### 🔐 Authentication (5 screens)
- **Screen / Login** — Email + password form, branded split-panel layout
- **Screen / OTP Verification** — 6-digit OTP input with countdown timer
- **Screen / Forgot Password** — Email entry with security note
- **Screen / Reset Password** — New password with strength meter + requirements checklist
- **Screen / Password Reset Success** — Confirmation with security tip + CTA

### 📊 Dashboard (2 screens)
- **Screen / Dashboard** — KPI stat cards, activity feed, pending reviews table
- **Screen / Analytics & Reporting** — Bar chart (submissions vs approvals), donut chart (categories), project performance table, activity feed

### 📁 Projects (2 screens)
- **Screen / Projects List** — Filterable project grid with status badges
- **Screen / Project Detail** — Documents tab, team members, project timeline

### 📄 Documents (4 screens)
- **Screen / Documents** — Searchable document table with filters + status badges
- **Screen / Upload Document Modal** — Drag-and-drop upload zone, file preview, metadata fields
- **Screen / Upload Success** — Confirmation with progress indicators
- **Screen / Document Detail** — PDF viewer simulation, version history (2 versions), approval timeline

### ✅ Review & Approval (4 screens)
- **Screen / Review Queue** — Priority-sorted document list with approve/reject actions
- **Screen / Reject Modal** — Rejection reason selection + comment field
- **Screen / Approve Modal** — Document info panel, optional comment field, standardized Cancel (212×48px) + Approve Document (212×48px) buttons with 10px radius and consistent 20px/12px padding
- **Screen / Review Queue (Post-Approval)** — Success toast + updated document status

### 🔔 Notifications (1 screen)
- **Screen / Notifications** — Grouped notification feed with read/unread states

### ⚙️ Admin Panel (2 screens)
- **Screen / Admin Panel** — User management, permission matrix toggles
- **Screen / Branding & Customization** — Logo upload, 6-color palette editor, font selector, live preview panel

### 🛡️ System Admin (2 screens)
- **Screen / System Admin** — Platform overview, system health indicators
- **Screen / System Settings** — Tabbed settings (General, Security, Integrations, Notifications, Audit Log) with 4-card grid layout: General Settings, Security & Access, Workflow & Approvals, System Status

---

## Design System

### Color Tokens (Figma Variables)
```
color/primary/600      #4F46E5  — Brand primary (Indigo)
color/primary/500      #6366F1  — Hover state
color/primary/50       #EEF2FF  — Light backgrounds
color/success/600      #16A34A  — Approved / positive
color/error/600        #DC2626  — Rejected / danger
color/warning/500      #F59E0B  — Pending / caution
color/neutral/900      #111827  — Primary text
color/neutral/600      #4B5563  — Secondary text
color/neutral/400      #9CA3AF  — Placeholder
color/neutral/100      #F3F4F6  — Dividers / subtle bg
```

### Typography Scale
```
Display  — Inter Bold 32px / 40px
H1       — Inter Bold 28px / 36px
H2       — Inter Semi Bold 22px / 30px
H3       — Inter Semi Bold 18px / 26px
Body L   — Inter Regular 16px / 24px
Body M   — Inter Regular 14px / 22px
Body S   — Inter Regular 13px / 20px
Caption  — Inter Regular 12px / 18px
Label    — Inter Semi Bold 12px / 16px
```

### Spacing Tokens (8px grid system)
```
spacing/1   4px   — Icon gap, tight inline
spacing/2   8px   — Input/badge internal gap
spacing/3   12px  — Button padding vertical, chip padding
spacing/4   16px  — Card internal row gap
spacing/5   20px  — Button padding horizontal
spacing/6   24px  — Card padding, section gap
spacing/8   32px  — Modal padding, content area padding
spacing/10  40px  — Section vertical gap
spacing/12  48px  — Button height (large), top bar height base
spacing/16  64px  — Top bar height, sidebar header
```

### Layout Grid
```
Sidebar width:       240px
Top bar height:       64px
Content start X:     272px (240 + 32 margin)
Content padding:      32px (left/right)
Card internal pad:    20–24px
Section gap:          16–24px
Card corner radius:   12px
Modal corner radius:  16px
Button height:        44px (standard) / 48px (large)
Button padding H:     20px
Input height:         44px
Input padding H:      14px
Input corner radius:   8px
Badge padding H:       8px
Badge corner radius:   6px
Form row height:      52–56px
Table row height:     52–56px
Stat card:         272×88px
```

### Component Library (28 components)
- **Buttons:** Primary, Secondary, Ghost, Danger, Success (3 sizes each)
- **Badges:** Draft, Under Review, Approved, Rejected, Revision Requested, Pending
- **Inputs:** Default, Focus, Filled, Error states
- **Cards:** Stat card (4 variants), File card (4 status variants)
- **Navigation:** Sidebar with active/inactive states

---

## User Roles

| Role | Primary Screens | Key Actions |
|------|----------------|-------------|
| **Vendor / Consultant** | Login → Dashboard → Upload → Track status | Upload docs, view feedback, resubmit |
| **Project Manager** | Dashboard → Review Queue → Approve/Reject | Review docs, approve/reject, view analytics |
| **Admin** | Admin Panel → Branding → User Management | Manage users, permissions, branding |
| **System Admin** | System Admin → System Settings | Configure platform, security, integrations |

---

## Prototype Flow

### Auth Flow
```
Login → OTP Verification → Dashboard
Login → Forgot Password → Reset Password → Reset Success → Login
```

### Vendor Flow
```
Dashboard → Documents → Upload Modal → Upload Success
```

### PM / Review Flow
```
Dashboard → Review Queue → Approve Modal → Post-Approval Queue (with toast)
Dashboard → Review Queue → Reject Modal → Review Queue
Documents → Document Detail (version history + approval timeline)
```

### Admin Flow
```
Admin Panel → Branding & Customization
```

### System Admin Flow
```
System Admin → System Settings
```

---

## Design Principles Applied

- **Neutral palette** with deep indigo (#4F46E5) as brand anchor
- **Auto Layout** on all frames — no fixed-position elements
- **8px grid** — all spacing multiples of 4px
- **Status-first UX** — every document state has a distinct visual language
- **Progressive disclosure** — modals for destructive/confirmation actions
- **Accessibility** — 4.5:1+ contrast ratios, clear focus states
- **Developer-ready** — semantic layer naming, Figma Variables throughout

---

*Built with Claude Code via Figma Plugin API — May 2024*
