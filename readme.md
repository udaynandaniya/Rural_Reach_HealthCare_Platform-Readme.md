🧠 RuralReach: Mental & Physical Emergency Support System for Isolated Communities

Live Project: https://rural-reach-one.vercel.app/  
Demo Video: https://drive.google.com/drive/folders/13NxStr-AydBhhMLudmS8H92j5eg3wjOQ

------------------------------------------------------------------

Problem Statement

Mental health and early symptom awareness in rural and isolated communities are neglected and stigmatized. People silently suffer from:

- Anxiety, insomnia, and depression
- Physical symptoms like chronic pain, fatigue, etc.
- Delays in identifying harmful health conditions
- No access to private or nearby help
- Stigma around asking for help

This project addresses:

- Lack of awareness of early symptoms (mental + physical)
- Lack of digital, private self-help tools
- No clear emergency help channels for users in distress
- No structured communication channel with local hospitals/doctors

------------------------------------------------------------------

Solution Overview

A 4-role, multi-purpose platform that offers:

1. Users: Self-assessment, mood tracking, health tips, and emergency alert system
2. Hospitals: Real-time alert dashboard, post verified medical tips
3. Doctors: Post symptom explainers, early detection content
4. Admin: Platform moderation and role verification

------------------------------------------------------------------

User Roles

Role         | Features
-------------|--------------------------------------------------------------------
User         | Mood tracking, self-awareness, receive hospital tips, emergency SOS
Hospital     | Accept/reject emergencies, post tips, real-time availability toggle
Doctor       | Share expert explainers and early detection checklists
Admin        | Approve hospitals/doctors, monitor content

------------------------------------------------------------------

Tech Stack

Frontend: Next.js, Tailwind CSS, TypeScript  
Backend: Next.js API routes, MongoDB Atlas  
Authentication: NextAuth.js (role-based)  
Notifications: Socket.IO (real-time alerts)  
Emails: Nodemailer (weekly wellness tips)  
Charts: Chart.js / Recharts  
Deployment: Vercel

------------------------------------------------------------------

Key Features (By Role)

User
- Guided self-assessment tools (PHQ-9 style)
- Mood tracking with historical charts
- Weekly personalized tips via email
- Behavior-based mood estimation (screen time, calls missed, low steps)
- Emergency SOS Button:
  - Sends location & details to nearest hospitals
  - 3-min no-response popup warning
- Manual address fallback if GPS is denied

Hospital
- Emergency-ready signup option
- Real-time availability toggle
- Alerts only sent if:
  - Hospital can handle emergencies
  - Hospital is within 5–10 km range
- Accepts cases on first-come basis
- Post verified health tips

Doctor
- Role-based signup
- Post explainers & tips (tagged topics)
- Possible future: anonymous Q&A

Admin
- Approve/verify hospitals & doctors
- Moderate content
- View analytics and emergency logs

------------------------------------------------------------------

Emergency Alert Flow

1. User Clicks SOS → GPS prompt → Data saved in EmergencyAlerts
2. Hospital Dashboard → Filters only nearby & available hospitals
3. First Acceptance Wins → Others blocked from taking case
4. No Response in 3 Min → User gets “No hospital responded” message
