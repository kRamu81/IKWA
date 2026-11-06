Here are the errors you hit, with the cause and the fix for each.

| # | Error / problem | Cause | Fix |
|---|---|---|---|
| 1 | App created in **Global** | Wrong type chosen when creating the app | Deleted it and recreated as a **scoped** app (`x_ikwa_campus_at_0`) |
| 2 | "Roles on widgets?" confusion | Roles belong on **pages**, not widgets | Set roles on the pages; added role checks in the script include |
| 3 | `addActiveQuery is not allowed in scope` | Blocked in scoped apps | Use `addQuery('active', true)` |
| 4 | Landing page too big, white gap at the bottom | Oversized CSS, and the CSS classes didn't match the new HTML | Rewrote the CSS with `clamp()` and `vh` for the new HTML |
| 5 | Kiosk: **"This kiosk is not configured"** | Opened the URL without `&kiosk=` | Add `&kiosk=<sys_id>` or set the widget option |
| 6 | Kiosk: **"Unknown or inactive kiosk"** | URL still contained `PASTE_SYS_ID_HERE` | Use the real sys_id |
| 7 | Kiosk: **"Unknown kiosk"** | Used my example sys_id (`a1b2c3...`) | Copied the real sys_id (`b7ab299a...`) |
| 8 | "Do I change the sys_id for each student?" | Mixed up kiosk sys_id and student | One kiosk sys_id serves all students; faces identify students |
| 10 | Kiosk: **"This kiosk is not configured."** again | `AttendanceMatcher` was the old version with no `checkKiosk()` | Replaced the whole script include |
