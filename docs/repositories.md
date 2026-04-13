# Planned Repositories

## Overview
The startup portfolio is currently organized around a small set of focused repositories. Each one has a clear role and a scoped first version.

## 1. `main-ui`
**Purpose:** public-facing site for the startup

**Initial scope**
- Landing page
- Latest reviews
- Latest videos
- Donation page
- Upcoming projects page
- Legal information

**Recommended direction**
- Next.js
- React
- TypeScript
- Tailwind CSS
- `shadcn/ui`

## 2. `agents`
**Purpose:** shared prompt library for specialist startup assistants

**Initial scope**
- Shared base prompt
- UI expert
- RPG Maker RZ expert
- Unity expert
- Networking expert
- Finance and business planning expert

## 3. `desktop-chess-game`
**Purpose:** prove out an internet-connected two-player chess game

**Initial scope**
- Two desktop players over the internet
- Server-mediated networking model
- Two implementation tracks:
  - RPG Maker RZ proof of concept
  - Tauri desktop proof of concept

## 4. `infrastructure`
**Purpose:** Terraform-first infrastructure foundation

**Initial scope**
- AWS-first baseline
- Standard Terraform structure
- Environment scaffolding
- Remote state conventions
- CI validation and planning workflows

## 5. `desktop-launcher`
**Purpose:** Windows-first launcher for installing, updating, and launching apps and games

**Initial scope**
- Installed library view
- Install flow
- Update flow
- Launch management
- Settings and diagnostics foundation

**Recommended direction**
- Tauri
- React
- TypeScript
- Manifest-driven install and update model

## 6. `community-chat-platform`
**Purpose:** private community platform for gamers to chat, hang out, and coordinate shared social sessions

**Initial scope**
- Accounts and controlled access
- Browser-first text and voice chat
- Community/server structure
- Voice rooms
- Shared watch-together and listen-together sessions
- Moderation and admin basics

**Recommended direction**
- Browser-first web client
- Real-time backend with auth and persistent chat data
- WebRTC-based voice support
- Legal external-provider integration for shared media sessions rather than self-hosted streaming

## Supporting repository
### `team-mission-and-documentation`
**Purpose:** shared planning, mission, and operational documentation for the team

This repository anchors the rest of the portfolio by documenting direction, standards, roadmap, and support work.
