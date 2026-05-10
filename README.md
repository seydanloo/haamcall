# HaamCall v3

HaamCall v3 is a lightweight browser-based meeting app for fast team collaboration.

## Architecture

HaamCall uses a **real-time SFU architecture** to keep meetings smooth as participants grow:

- Web app for meeting experience
- Backend service for room/session management
- LiveKit SFU for real-time audio/video/screen share transport

### Impact on Meeting Quality

- **SFU-based media routing (LiveKit)** improves quality for group calls by avoiding full mesh peer-to-peer overhead.
- **Adaptive video grid + active speaker highlighting** keeps focus clear in larger rooms.
- **Reconnection handling + connection banners** improves reliability under unstable networks.
- **TURN support** helps participants behind strict NAT/firewalls join more successfully.
- **State isolation with Zustand stores** keeps room UI responsive and predictable during rapid media events.

## Dark / Light Theme

The web app supports both themes:

- Persistent theme preference via `localStorage`.
- Root-level class switching (`dark` class on document root).
- Clean, high-contrast visual system designed for long meeting sessions.

## What Kind of Meetings You Can Have

- **1:1 quick calls** for instant check-ins.
- **Small team standups** with camera/mic and chat.
- **Larger collaboration rooms** with adaptive participant layout.
- **Presentation-style sessions** with screen sharing.
- **Async-friendly sessions** using file upload/download and in-room chat.

## Key Features

- Instant room creation + join by link
- No account required for regular meetings
- Pre-join camera/mic readiness check
- In-room controls: mic, camera, screen share, leave
- Real-time chat and participant list
- File sharing inside meeting rooms
- Responsive UI for desktop and mobile

## Security

- Server-side room and session management (no direct client trust)
- Admin panel protected with credential login and expiring sessions
- TURN support for secure/reliable connectivity across restrictive networks
- Token-based room access issued by the backend before joining media sessions
- Input validation and error boundaries for safer request/UI handling

## Tech Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS, Zustand
- **Backend:** NestJS, TypeScript
- **Real-time media:** LiveKit (SFU), WebRTC, TURN (coturn)
- **Infrastructure:** Docker, Docker Compose
