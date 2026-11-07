# latchkey

An authentication server built with NestJS, plus a small Flutter client that uses it.

> Work in progress. This project is built lesson by lesson, and this README grows with it.

## What it will do

- Email/password sign-up with email verification
- Login with short-lived access tokens (JWT, 15 min) and rotating refresh tokens
- Refresh token reuse detection (a reused token revokes every session)
- Logout on this device / on every device
- Forgot / reset password
- Sign in with Google and Sign in with Apple
- Account deletion (`DELETE /me`)

## Repository layout

```
latchkey/
├── server/          NestJS API (TypeScript, PostgreSQL, Prisma)
├── flutter_client/  Flutter demo app (Clean Architecture + BLoC)
└── README.md
```

## Getting started

### Server

```bash
cd server
npm install
npm run start:dev
```

The API runs on http://localhost:3000.

## Roadmap

- [x] 0. Project setup
- [ ] 1. Config module + env validation
- [ ] 2. Database: Prisma schema + first migration
- [ ] 3. Users module + password hashing
- [ ] 4. Register + email verification
- [ ] 5. Login, access tokens, JWT guard, `GET /me`
- [ ] 6. Refresh tokens: rotation, reuse detection, logout
- [ ] 7. Forgot / reset password
- [ ] 8. Google sign-in
- [ ] 9. Apple sign-in
- [ ] 10. Hardening: helmet, throttling, CORS, `DELETE /me`
- [ ] 11. Flutter client: setup + architecture
- [ ] 12. Flutter: auth repository, secure storage, refresh interceptor
- [ ] 13. Flutter: screens + Google/Apple buttons
- [ ] 14. Final README
