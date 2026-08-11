# Talli Sandbox Log
Target production version: v3.0.9
Last updated: 2026-08-11
Current sandbox version string: v3.0.9 SANDBOX

---

## Status
IN PROGRESS — do not promote to production until all items below are ticked

---

## Outstanding before production push

- [ ] Fix `&amp;` rendering as escaped HTML in the header (should read "Pick & Pack")
- [ ] Collections screen UX — make it obvious to Rab that invoice upload is step one
- [ ] Rename "Counter Orders" to "Collections" throughout the list screen
- [ ] Badge counts — red circles on home tiles with combined totals
- [ ] Badge counts — totals split per entry card inside Pick & Pack home
- [ ] Universal sign-off component

---

## Changes made in sandbox

### 2026-08-11 — Session 1 (Neil + Claude)
- Pick & Pack home screen added as unified entry point for tile 02
- Three entry cards: Packing Slip, Collections, Remedial Pick
- Job number search fallback added below the three cards
- Pick button added to stock check shell header — loads current session directly into pick completion without exiting to search
- Green Pick Completion shortcut card removed from M1 upload screen
- Back navigation from Collections and Remedial Pick returns to Pick & Pack home
- Tab bar removed from Goods In — tile 01 is now Goods In only, no outbound reference
- Collections list removed from Goods In — lives exclusively under Pick & Pack
- List screen card title set to "Counter Orders" — to be renamed "Collections" next session
- SANDBOX label added to all three version string locations

---

## How to use this file

- Upload this file alongside index.html at the start of every sandbox session
- Claude reads it first to understand current state before touching any code
- Add a new dated entry under "Changes made in sandbox" at the end of every session
- Tick off items in "Outstanding before production push" as they are completed
- When all items are ticked: strip SANDBOX from version string, push index.html to production via GQ, paste the changelog entry into GQ, then delete or archive this file from the sandbox repo

---

## Production changelog entry (paste into GQ at production push)

```
v3.0.9 — [date of production push]
- Pick & Pack home screen added as unified entry point for tile 02
- Three entry paths: packing slip, collections, remedial pick
- Job number search fallback on Pick & Pack home
- Pick button added to stock check shell — loads session directly into pick completion
- Green Pick Completion shortcut card removed from M1 upload screen
- Back navigation from collections and remedial returns to Pick & Pack home
- Tab bar removed from Goods In — tile 01 is now Goods In only, no outbound reference
- Collections removed from Goods In — lives exclusively under Pick & Pack
```

## GQ commit message (use at production push)
```
Pick & Pack home — unified entry, Goods In and counter order separation
```
