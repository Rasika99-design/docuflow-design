# DocuFlow Component System

## Component Sets (14 total)

| Component | Variants | Variant Properties |
|-----------|----------|-------------------|
| **Button** | 16 | Type (Primary/Secondary/Ghost/Danger) × State (Default/Hover/Disabled/Loading) |
| **Input** | 6 | State (Default/Focus/Filled/Error/Success/Disabled) |
| **Badge** | 6 | Status (Approved/Pending/Under Review/Rejected/Revision Requested/Draft) |
| **Avatar** | 3 | Size (SM/MD/LG) |
| **Nav Item** | 3 | State (Default/Active/Hover) |
| **Tab** | 3 | State (Active/Inactive/Hover) |
| **Toggle** | 3 | State (On/Off/Disabled) |
| **Stat Card** | 4 | Metric (Total Documents/Pending Review/Approved Today/Rejected) |
| **Dropdown** | 2 | State (Closed/Open) |
| **Table Row** | 3 | State (Default/Hover/Selected) |
| **Modal Header** | 4 | Type (Approve/Reject/Info/Warning) |
| **Toast** | 4 | Type (Success/Error/Warning/Info) |
| **File Card** | 4 | Status (Approved/Under Review/Rejected/Revision Requested) |
| **Notification Item** | 4 | Read (Unread/Read) × Category (Approval/Rejection/Submission/System) |

## Identification Convention
- All **Component Sets** have a 2px purple (#7C3AED) outer border
- All **Component Instances** placed in screens have a 1px purple outer border
- This allows instant visual identification of component-driven elements vs. one-off frames

## Auto Layout Applied
- All components use Auto Layout with explicit padding tokens
- Horizontal/Vertical layout modes set per component type
- `primaryAxisSizingMode: AUTO` for content-hugging components
- `primaryAxisSizingMode: FIXED` for table rows, nav items, cards

## Naming Convention
`ComponentName / VariantProperty=Value, VariantProperty=Value`

Examples:
- `Button / Type=Primary, State=Default`
- `Badge / Status=Approved`
- `Input / State=Focus`
- `Toggle / State=On`
