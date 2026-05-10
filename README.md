# HaamCall v3

**Language / زبان:** [English](#english) | [فارسی](#فارسی)

---

## English

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

---

## فارسی

هم‌کال v3 یک برنامه سبک مبتنی بر مرورگر برای برگزاری جلسات آنلاین و همکاری سریع بین اعضای تیم است.

## معماری

در HaamCall از **معماری real-time SFU** استفاده شده است تا با افزایش تعداد شرکت‌کنندگان، کیفیت جلسه پایدار و روان باقی بماند.

- یک **Web app** برای تجربه جلسه در مرورگر
- یک **Backend service** برای مدیریت room و session
- استفاده از **LiveKit SFU** برای انتقال real-time صدا، تصویر و screen share

### تأثیر بر کیفیت جلسه

- استفاده از **SFU-based media routing (LiveKit)** باعث بهبود کیفیت تماس‌های گروهی می‌شود، زیرا سربار معماری full mesh peer-to-peer حذف می‌شود.
- استفاده از **Adaptive video grid + active speaker highlighting** کمک می‌کند در اتاق‌های بزرگ تمرکز روی فردی که در حال صحبت است حفظ شود.
- وجود **Reconnection handling + connection banners** باعث می‌شود در شبکه‌های ناپایدار اتصال کاربران پایدارتر مدیریت شود.
- پشتیبانی از **TURN** کمک می‌کند کاربرانی که پشت NAT یا firewallهای سخت‌گیرانه هستند راحت‌تر به جلسه متصل شوند.
- استفاده از **State isolation با Zustand stores** باعث می‌شود رابط کاربری اتاق هنگام رخ دادن رویدادهای سریع رسانه‌ای همچنان responsive و قابل پیش‌بینی باقی بماند.

## نوع جلساتی که می‌توانید داشته باشید

- برگزاری **تماس‌های سریع 1:1** برای هماهنگی‌های فوری
- برگزاری **جلسات standup تیم‌های کوچک** با camera، mic و chat
- ایجاد **اتاق‌های همکاری بزرگ‌تر** با layout تطبیقی شرکت‌کنندگان
- برگزاری **جلسات ارائه** با استفاده از screen sharing
- ایجاد **جلسات async-friendly** با امکان file upload/download و chat داخل اتاق

## قابلیت‌های اصلی

- ایجاد فوری room و امکان پیوستن از طریق لینک
- عدم نیاز به account برای شرکت در جلسات معمولی
- بررسی آماده بودن camera و mic قبل از ورود به جلسه
- وجود کنترل‌های داخل جلسه شامل mic، camera، screen share و leave
- امکان chat لحظه‌ای و مشاهده لیست شرکت‌کنندگان
- قابلیت اشتراک فایل داخل اتاق جلسه
- رابط کاربری responsive برای desktop و mobile

## امنیت

- مدیریت room و session در سمت server بدون اعتماد مستقیم به client
- محافظت از Admin panel با credential login و sessionهای دارای زمان انقضا
- پشتیبانی از TURN برای ایجاد اتصال امن و پایدار در شبکه‌های محدود
- صدور token دسترسی به room توسط backend پیش از ورود به session رسانه‌ای
- انجام input validation و استفاده از error boundaries برای مدیریت امن‌تر درخواست‌ها و رابط کاربری

## Tech Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS, Zustand
- **Backend:** NestJS, TypeScript
- **Real-time media:** LiveKit (SFU), WebRTC, TURN (coturn)
- **Infrastructure:** Docker, Docker Compose
