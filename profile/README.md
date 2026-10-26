<p align="center">
  <a href="https://slovenscinakzk.com" target="_blank">
    <img src="https://raw.githubusercontent.com/Slovenscina-Korak-za-Korakom/.github/main/assets/slo-logo.svg" width="400" alt="Slovenščina Korak za Korakom logo">
  </a>
</p>

<p align="center">
  <a href="https://slovenscinakzk.com"><img src="https://img.shields.io/badge/Platform-Live-brightgreen" alt="Platform status"></a>
  <img src="https://img.shields.io/badge/Students-350%2B-blue" alt="Students">
  <img src="https://img.shields.io/badge/Lessons-5%2C000%2B%20hours-orange" alt="Lesson hours">
  <img src="https://img.shields.io/badge/Staff-10-purple" alt="Staff">
  <img src="https://img.shields.io/badge/Languages-4-lightgrey" alt="Languages">
</p>

## About

**Slovenščina Korak za Korakom** (Slovene Step by Step) is a Slovenian language school that teaches online and in person. Learners are matched with a tutor after a placement test and take one-on-one, pair, or group lessons, plus language-club events and a self-paced video course.

Until 2026 the school ran on Excel, Google Calendar, and Telegram. Today it runs on its own platform, which handles booking, scheduling, payments, courses, and staff management in one place, in Slovenian, English, Italian, and Russian.

## The platform

| Repository | What it is |
|---|---|
| [`student-platform`](https://github.com/slovenscina-korak-za-korakom/student-platform) | The learner-facing web app: booking, payments, progress tracking, and encrypted course streaming |
| [`admin-platform`](https://github.com/slovenscina-korak-za-korakom/admin-platform) | The staff tool: scheduling, team hours and budgets, language-club events, and course management |
| [`student-app`](https://github.com/slovenscina-korak-za-korakom/student-app) | Mobile companion app for learners: booking, session reminders, and progress *(in development)* |

### Engineering at a glance

- **350+ registered learners and 10 staff** on the platform, with **80–100 lesson-hours scheduled every week**
- **Time-zone-aware scheduling** for learners and tutors in different countries, built around IANA time zones after a real production bug ([the story](https://github.com/slovenscina-korak-za-korakom/admin-platform))
- **Encrypted course streaming:** AES-128 HLS, enrollment-gated keys, and short-lived presigned S3 URLs, so paid video never exposes a source URL ([details](https://github.com/slovenscina-korak-za-korakom/student-platform))
- **Automated video pipeline:** uploads from the admin panel are packaged into encrypted HLS by an S3-triggered AWS Lambda running ffmpeg
- **Near-zero hosting cost** on Vercel and pay-per-use AWS

Designed, built, and operated by a single engineer, [Sebastjan Bas](https://github.com/sebastjanbas).

**Stack:** Next.js · TypeScript · PostgreSQL (Drizzle ORM) · Clerk · Stripe · AWS S3 and Lambda · Vercel

## Community

- **[Telegram](https://t.me/slovenscina_korak_za_korakom)**: 2,100+ members practising Slovenian together
- **[Instagram](https://www.instagram.com/slovenscina_korakzakorakom/)**: daily tips and cultural insights
- **[TikTok](https://www.tiktok.com/@slovenina.korak.z5)**: short language lessons
- **[Website](https://slovenscinakzk.com)**: book a free trial lesson

## Security

Found a vulnerability? Email [sebastjan.bas1@gmail.com](mailto:sebastjan.bas1@gmail.com). Reports are handled promptly.

## License

Proprietary. All rights reserved.
