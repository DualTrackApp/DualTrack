# **Milestone 1 – DualTrack (Unit 7)**

***Table of Contents***

***Overview***

***Product Spec***

***User Features (Required & Optional)***

***Screen Archetypes***

***Navigation (Tabs + Flows)***

***Wireframes (next)***

---

# **Overview**

## *Description*  
DualTrack is a mobile-first app designed for student-athletes, coaches, and optionally parents, to manage academic, athletic, and wellness responsibilities in one secure and centralized platform.  
The app allows athletes to plan and track tasks, workouts, forms, injuries, eligibility status, and wellness habits — while giving coaches powerful tools to view progress, approve forms, and support athletes in real time.  

## *App Evaluation*  
**Category:** Health, Productivity, Education  
**Mobile:** Real-time data entry, push reminders, camera/file uploads, and instant sync with Firebase for shared data between athletes and coaches.  
**Story:** Student-athletes balance practice, academics, eligibility requirements, and wellness. DualTrack helps organize it all with one tool, increasing accountability and performance.  
**Market:** Primarily college and high school athletics, but easily scalable to clubs and travel programs.  
**Habit:** Athletes use the app daily for schedules, wellness logs, and reminders; coaches use it weekly for reviews, approvals, and dashboards.  
**Scope:** Semester 1 = Core app features (schedule, wellness, forms, injury tracking, sync). Semester 2 = Expansion with advanced tools (exports, messaging, wearable integration).

---

# **Product Spec**

## 1) User Features (Required & Optional)

### ✅ Required (MVP)

---

### **R1. Authentication & Role-Based Access**
* **User Stories**  
  - As an athlete, I can register/login and select my sport/team.  
  - As a coach, I can login and view only athletes on my roster.  
* **Acceptance Criteria**  
  - Login remembers session.  
  - Wrong credentials show inline error.  
  - Role determines accessible tabs and permissions.

---

### **R2. Home Dashboard**
* **Stories**  
  - View “Next Up” events, due forms, alerts (e.g., “At Risk”), and streak badges.  
* **Acceptance**  
  - Cards update in real-time when synced.  
  - Badges show new or pending actions.

---

### **R3. Tasks & Schedule Management**
* **Stories**  
  - Add, edit, delete, and filter tasks (Academic, Athletic, Events).  
  - Conflict detection when overlapping events occur.  
* **Acceptance**  
  - New tasks update instantly on schedule view.  
  - Task completion updates progress data.

---

### **R4. Forms (Travel, Absence, Participation)**
* **Stories**  
  - Submit forms with attachments and e-signature.  
  - Check approval status and coach notes.  
* **Acceptance**  
  - Submit → Pending state.  
  - Coach approval/rejection updates timeline and sends notification.

---

### **R5. Notifications & Reminders**
* **Stories**  
  - Receive reminders for tasks, deadlines, injury rehab check-ins.  
* **Acceptance**  
  - Tap notification → Deep link to relevant screen.  
  - Daily summary and snooze functions available.

---

### **R6. Injury & Recovery Tracker**
* **Stories**  
  - Log injuries (type/severity/date), create rehab checklist, receive rehab reminders.  
  - Coaches can monitor recovery status.  
* **Acceptance**  
  - Injury logs appear in schedule and progress screens.  
  - Completed rehab tasks update status automatically.

---

### **R7. Nutrition & Wellness Log**
* **Stories**  
  - Log daily hydration, meals, and sleep.  
  - Generate weekly wellness summaries.  
* **Acceptance**  
  - Wellness data contributes to streaks/achievements.  
  - Trends visible in Progress tab.

---

### **R8. Eligibility & Compliance Tracker**
* **Stories**  
  - Track GPA, credit hours, and attendance.  
  - Receive “At Risk” flags when thresholds not met.  
* **Acceptance**  
  - GPA thresholds highlight warnings.  
  - Coaches see alerts for early intervention.

---

### **R9. Calendar Sync & Family View**
* **Stories**  
  - Sync practice/game schedules to Google/Apple Calendar.  
  - Share read-only links with parents or guardians.  
* **Acceptance**  
  - Calendar events update automatically with changes.  
  - Family view is view-only and secure.

---

### **R10. Gamification System**
* **Stories**  
  - Earn streak badges for consistency (attendance, task completion, wellness).  
  - Coach-awarded badges for motivation.  
* **Acceptance**  
  - Badges show up on dashboard/profile.  
  - No public leaderboards for privacy.

---

### **R11. Cloud Sync (Firebase)**   
* **Stories**  
  - Store and sync data (tasks, forms, wellness logs, injuries) in real time between athlete and coach.  
* **Acceptance**  
  - Changes appear on coach dashboard without refresh.  
  - Offline actions queue and sync when online.

---

### **R12. Wellness Survey Module**
* **Stories**  
  - Weekly survey: stress, fatigue, mood.  
  - Generate team wellness trends for coach review.  
* **Acceptance**  
  - Surveys prompt weekly.  
  - Aggregated results visible on coach dashboard.

---

### **R13. Coach Dashboard**
* **Stories**  
  - View roster, pending forms, at-risk athletes, wellness trends, injury updates.  
  - Approve or reject forms, manage tasks, review team analytics.  
* **Acceptance**  
  - Dashboard updates in real time.  
  - Approval actions logged with timestamp and user ID.

---

### ✳️ Optional / Nice-to-Have (Future Phases)

- **O1. Document Vault** – Secure storage for medical clearance, insurance, transcripts.  
- **O2. Team Announcements & Messaging** – Coach → Team one-way posts with push notifications.  
- **O3. Export (CSV/PDF)** – Export schedules, logs, wellness trends, eligibility reports.  
- **O4. In-App Chat (Coach ↔ Athlete)** – Direct communication.  
- **O5. Wearable Integration** – Optional pulling of heart rate, sleep, or step data.

---

# **2) Screen Archetypes (with components & main actions)**

**A. Login / Register**  
* Components: email/password fields, role selector, “Forgot password”.  
* Actions: Login → Home; Register → Role & Team select → Home.

**B. Home Dashboard**  
* Components: Next Up, Pending Forms, At-Risk Alerts, Streak Badges, Quick Add.  
* Actions: Tap card → Detail; tab bar to navigate.

**C. Schedule**  
* Components: Weekly calendar, filters (Academic/Athletic/Events), “+ Add Task” button.  
* Actions: Tap task → Detail; Add → Task Form; Long-press to complete/delete.

**D. Task Form / Task Detail**  
* Components: Task title, type, date/time, reminder, recurrence.  
* Actions: Save, Update, Delete; conflict warnings.

**E. Forms**  
* Components: Status list (Pending/Approved/Rejected), + New Form, filters.  
* Actions: New Form → Editor; Tap form → Timeline & attachments.

**F. Progress & Wellness**  
* Components: Completion chart, wellness summaries, eligibility flags, injury overview.  
* Actions: Tap tile → Detail; Log wellness; “Log Injury” → Injury Form.

**G. Injury & Recovery**  
* Components: List view, injury timeline, rehab checklist, + Add Injury.  
* Actions: Log injury, resolve, add notes, set reminders.

**H. Eligibility Tracker**  
* Components: GPA, credit hours, attendance stats, “At Risk” flags.  
* Actions: Tap tile → Explanation; Add academic task directly.

**I. Coach Dashboard (role=coach)**  
* Components: Roster, Pending Forms Queue, Wellness Trends, At-Risk Flags.  
* Actions: Approve/reject, open athlete profiles, export analytics.

**J. Profile & Sync Settings**  
* Components: Avatar, name, role, team; calendar linking; notification settings; sync status.  
* Actions: Edit profile, sign out, manual sync.

---

# **3) Navigation**

## **Tabs (Tab → Screen)**

* 🏠 Home → Dashboard  
* 📅 Schedule → Calendar & Tasks  
* 🗂️ Forms → Form Management  
* 📈 Progress → Eligibility, Wellness, Injury  
* 👤 Profile → Profile & Sync Settings (Coach Dashboard accessible for coaches)

---

## **Key Flow Navigation (Screen → Screen)**

### **Flow F1: Onboarding & Role**
1. App launch → Login/Register.  
2. Register → Choose Athlete/Coach + team/sport → Home.  
3. Prompt notification permission on first login.

### **Flow F2: Create a Task**
1. Home → Schedule → “+ Add Task”.  
2. Fill out Task Form → Save.  
3. Conflict check → Success toast → Schedule updates instantly.

### **Flow F3: Submit a Form**
1. Forms → “+ New Form” → Choose type.  
2. Fill fields + attach file/e-sign → Submit.  
3. Status = Pending → Coach notified → Approve/Reject → Athlete notified.

### **Flow F4: Log Injury & Rehab**
1. Progress → Injury & Recovery → “+ Add Injury”.  
2. Add rehab checklist with reminders → Save.  
3. Rehab tasks appear in Schedule.  
4. Resolving injury archives the record.

### **Flow F5: Check Eligibility**
1. Progress → Tap Eligibility tile.  
2. View GPA/credits/attendance.  
3. If “At Risk,” view reasons and suggested actions → Prefilled Task Form.

### **Flow F6: Notifications & Deep Links**
* Task reminder → Task Detail.  
* Form decision → Form Detail.  
* Rehab reminder → Injury Detail.

### **Flow F7: Profile & Settings**
1. Profile → Edit Profile → Save.  
2. Calendar linking → Permission flow → Events synced.  
3. Toggle notifications → Immediate effect.

### **Flow F8: Coach Review**
1. Coach Dashboard → Roster → Athlete Profile.  
2. Approve/Reject forms, view injuries, eligibility, wellness trends.  
3. Actions are logged with audit trail.

### **Flow F9: Sync Handling**
1. Any screen → Action taken offline.  
2. UI shows “Syncing…” banner.  
3. Firebase sync completes in background once online.

---

**Back behavior (global):**  
- Up/back returns to previous screen.  
- Tabs preserve scroll & filters.  
- Unsaved edits prompt confirmation.

**Empty/Error States:**  
- No tasks → “Add your first task” CTA.  
- Offline → banner “Offline — actions will sync later”.  
- Missing permissions → inline explainer + “Enable” button.

---
# **Wireframes**
1 >
2 >
3 >
