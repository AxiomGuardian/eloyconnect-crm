# Eloy Connect CRM

Staff dashboard for the City of Eloy's civic engagement platform. Built as a single-page web application that connects to Supabase for live data, enabling city staff to manage reports, publish content, and monitor community engagement.

## Features

### Core Operations
- **Dashboard** — Live overview with report counts, resident stats, and recent activity from Supabase
- **Reports Management** — View, triage, and update citizen-submitted reports with photos, GPS locations, and status tracking
- **Content Management** — Create, edit, and publish news articles, events, and emergency alerts
- **Residents Directory** — Browse registered residents with profile details and engagement history

### Specialized Modules
- **Code Enforcement** — Manage code enforcement notices and violations
- **Business Directory** — Review and approve business listings submitted through the app
- **City Leaders** — Manage elected official profiles and department head bios
- **AI Briefing** — Grok-powered analytics and insights across all city data
- **Notification Broadcaster** — Send push notifications to app users via Supabase Edge Functions
- **Settings** — Staff account management and system configuration

### Role-Based Access
- **City Manager** — Full access to all modules
- **Department Head** — Department-specific views and management
- **Staff** — Standard operational access
- **Chambers of Commerce** — Business directory and economic development tools

## Tech Stack

- **Single HTML file** — Self-contained dashboard (~7500+ lines) with inline CSS and JavaScript
- **Supabase JS SDK** — Real-time database queries, authentication, and storage
- **Grok API (xAI)** — AI-powered analytics and natural language briefings
- **Responsive Design** — Works on desktop and tablet browsers

## Setup

1. Clone this repo
2. Open `index.html` in a browser, or serve via any static file server
3. The Supabase client is configured with the project URL and anon key in the source
4. Log in with staff credentials configured in your Supabase auth system

## Supabase Tables

The CRM reads from and writes to the following Supabase tables:

| Table | Purpose |
|-------|---------|
| `profiles` | User profiles (display_name, avatar_url, email) |
| `reports` | Citizen-submitted issue reports |
| `news` | News articles and announcements |
| `events` | City events and meetings |
| `alerts` | Emergency and informational alerts |
| `notifications` | Push notification records |
| `code_enforcement_notices` | Code enforcement cases |
| `businesses` | Local business directory listings |

## Related

- **[EloyConnect](https://github.com/AxiomGuardian/EloyConnect)** — iOS app for residents (SwiftUI + Supabase)

## License

Private. All rights reserved.
