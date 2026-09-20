# PROJECT-STATE.md

Current status of the Portfolio Engine build.
Update this file at the end of every working session.

---

## CURRENT PHASE

**Phase 01 — Foundation**
Status: ✅ COMPLETE
---

## WHAT'S DONE

- [x] Folder `D:\Projects\Portfolio\portfolio-engine\` created
- [x] `CLAUDE.md` created
- [x] `PROJECT-STATE.md` created (this file)
- [x] `package.json` created
- [x] Next.js + TypeScript + Tailwind installed
- [x] All config files created
- [x] Basic app folder structure created
- [x] Hello world page working at localhost:3000
- [x] Git repo initialized
- [x] Pushed to private GitHub repo
---

## WHAT'S NEXT

- [ ] `package.json` created
- [ ] Next.js + TypeScript + Tailwind installed
- [ ] `tsconfig.json`, `next.config.js`, `tailwind.config.ts` created
- [ ] shadcn/ui installed
- [ ] Firebase SDK installed
- [ ] Basic app folder structure created
- [ ] Empty routes: Home, Projects, Project Detail, About, Contact, Admin
- [ ] `npm run dev` works, shows a page
- [ ] Git repo initialized
- [ ] Pushed to GitHub
- [ ] "Hello world" deployed to Firebase App Hosting

---

## BUILD PHASES OVERVIEW

- Phase 01 — Foundation (current)
- Phase 02 — Public Site (Minimal skin)
- Phase 03 — Admin Panel
- Phase 04 — Polish + Demo
- Phase 05 — Editorial Skin
- Phase 06 — First Client

---

## LOCKED DECISIONS

- Platform: Firebase (Blaze plan, staying in free tier)
- Stack: Next.js + TypeScript + Tailwind + shadcn/ui
- Deployment: Firebase CLI local-source
- Public site: server-rendered
- Admin: client-side Firebase SDK
- Images: compressed to 200-400 KB on upload
- Soft-delete: 30-day trash for projects
- Client owns: Firebase, domain, data
- We own: Portfolio Engine source

---

## NOTES

- Firebase account: your own (dev/demo)
- Client Firebase: created at handover time (later phase)
- Domain: `.web.app` free tier first, custom domain optional
- Deploy method: portable Node.js + Firebase CLI on USB

---

## LAST UPDATED

Phase 01 — Step 2 completed