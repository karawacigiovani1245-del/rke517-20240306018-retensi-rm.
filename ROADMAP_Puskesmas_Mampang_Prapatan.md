# Roadmap

One slice per week. Each slice has a check you can run live in a 2-minute demo.
Change this file only through a pull request, and say why in the PR.

| Week | Tag | Slice (make it specific to your app) | Done when (Situation → Action → Result) | Feedback from |
|---|---|---|---|---|
| 8 | v0.1 | Launch: PRD, roadmap, and repository for retention status list at Puskesmas Mampang Prapatan | Files in place, buddy reviewed the launch PR | Buddy |
| 9 | v0.2 | The core form saves a fictional retention record. Fields: No. RM (fictional), Tanggal Kunjungan Terakhir, Tanggal Jatuh Tempo Retensi, Status Retensi | Enter one fictional record RM-0001, Save, reload -> record still there | Buddy |
| 10 | v0.3 | List, search, edit retention records. Search by: No. RM (fictional) or Status Retensi | Search "RM-0001" -> the record appears; edit status to Siap Retensi -> change saved | Week 10 demo: 3 comments become issues |
| 11 | v0.4 | Data quality rules: No. RM required, last visit not in future, due date not earlier than last visit, valid retention status | Due date earlier than last visit -> Save stopped with "Tanggal jatuh tempo tidak boleh lebih awal dari tanggal kunjungan terakhir" | Buddy |
| 12 | v0.5 | Report: monthly retention summary and list of due/ready retention records | 10 fictional test records -> open report -> numbers match my hand count | Lecturer: one change request |
| 13 | v0.6 | Usability test and fixes, fictional-data privacy check | A classmate (not my buddy) does 3 tasks; top 3 problems fixed | Classmate tester |
| 14 | v1.0 | Release: README, release notes, demo for retention status app | 5-minute demo runs end to end | Demo day |

## Change log
| Date | What changed in the plan | Why |
|---|---|---|
| 2026-11-20 | Set weekly slices for Daftar dan status retensi rekam medis at Puskesmas Mampang Prapatan using fictional data | Aligned weekly milestones with the selected Idea 2 scope and PRD |
