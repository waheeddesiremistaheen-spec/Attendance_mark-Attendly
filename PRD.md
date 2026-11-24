Attendly

Product Name: Attendly
Version: 1.0

Product Overview

Attendly is a mobile-first application that makes taking attendance for classes easier for both lecturers and students. It replaces the traditional paper register with a secure, real-time, time-bound digital solution that ensures only students physically present in the lecture room can mark attendance. The system serves students, lecturers, and academic administrators by providing transparency, accuracy, and accountability while reducing administrative burden.

It ensures that students are present before attendance is marked, replacing the traditional paper register, which can be misplaced. This application focuses mainly on attendance coordination and attendance accuracy. In short, students who are not present in class will not sign attendance, reducing the rate of false attendance.

Problem Statement

The current attendance system in many universities, including Bacock University, relies heavily on paper to take attendance. This creates multiple problems, such as the following:

1. Students can sign the attendance sheet from outside.
2. Students can mark attendance for absent friends.
3. Lecturers waste valuable time collecting and verifying attendance.
4. Paper records are easily lost, damaged, or altered.
5. There is no reliable audit trail or real-time visibility of attendance.
6. The use of ink on paper may fade, leading to loss of content.
7. Departmental and examination officers struggle to obtain accurate attendance data for decisions.
8. Lecturers find it hard to determine the accurate number of students who actually attended their class at a given time.

Goals and Objectives

Primary Objective:
To eliminate fraudulent attendance and improve the accuracy and efficiency of class tracking.

Specific Objectives:

1. To ensure only students physically present in the class sign or mark attendance.
2. To reduce the time lecturers spend checking the accuracy of attendance.
3. To provide real-time and historical attendance records accessible to authorized users.
4. To create a transparent, auditable system that supports academic decisions.
5. To ensure that the number of people present in the class is accurately calculated.

Target Users

Students, lecturers, and department admins or HODs.

- Students: To create a fast, fair, and simple way to mark attendance.
- Lecturers: For quick setup, live monitoring, and accurate records.
- Department Admins or HODs: For reliable reports and eligible data.

Stakeholders

- Students: Quick, fair, and simple attendance marking; ability to view attendance history.
- Lecturers: Fast session setup, real-time monitoring, and accurate, exportable records.
- Department Admins or HODs: Reliable attendance reports for academic and eligibility decisions.

User Personas

Persona 1: Tunde (Student)

A 200-level student at Bacock University studying Computer Science. He sometimes arrives late and hates the stress of fighting for attendance. He dislikes seeing people mark attendance for friends who are not present, as he feels this is not a fair judgment. He wants a system that is quick, fair, and just.

Persona 2: Dr. Adebayo (Lecturer)

He teaches a large number of students and spends 8–20 minutes on attendance alone, which is a long time. He wants a way to take attendance without making it stressful and with it being accurate and just.

Persona 3: Mrs. Okoro (Department Officer)

Responsible for the accuracy of attendance for eligible students to participate in examinations. She currently receives incomplete or questionable paper records, missing weeks, and missing reports. She needs clean, exportable data.

Solution Overview

Attendly allows a lecturer to generate a unique, time-limited attendance session for a class. Students mark attendance through their mobile app only when they are:

1. Within the allowed time window.
2. Authenticated with their student identity (matric number).
3. Able to provide proof of being in class, such as taking a live picture of the lecturer.

The system records attendance events with timestamp, location verification status, and device information for audit purposes and information preferences.

Functional Requirements

Core Features

For Lecturers

- Create a class session (select course, date, start time, duration, and location).
- Generate a unique session code or QR code.
- Check attendance count.
- View the list of students who have marked attendance.
- Close or extend a session.
- Export attendance report.

For Students

- View upcoming and active class sessions for enrolled courses.
- Mark attendance only when:
  - Within the defined space.
  - Within the time window.
  - Authenticated as a valid user.
- Receive confirmation of successful marking.
- View personal attendance history.

For Admin or Department

- View and export attendance reports by course, student, or date range.
- Perform basic user and course management.

Supporting Features

- Student authentication: university ID plus password or OTP.
- Geofencing: configurable radius around the classroom.
- Time-bound session: open for 15 minutes before class and close after a set duration.
- Audit log: who marked attendance, when, and verification status.
- Notification when a session opens.

Nice to Have

- Facial verification.
- Offline mode with later sync.
- Integration with the university student portal.
- Attendance percentage calculation and eligibility alerts.
- Multi-campus support.

Non-functional Requirements

- Attendance marking should complete in three seconds under normal conditions.
- The system should be available during lecture hours (at least 99% during peak use).
- All attendance data must be encrypted for safekeeping and security.
- New users should successfully mark attendance with minimal instruction.
- Support at least 200 students marking attendance in the same session.
- Mobile responsive.

Key User Stories

Student

- As a student, I want to mark my attendance quickly so that I do not disrupt the lecture.
- As a student, I want the system to prevent others from marking for me so that attendance remains fair.
- As a student, I want to see my attendance history so that I know my current standing.

Lecturer

- As a lecturer, I want to open an attendance session in under 30 seconds so that I can start teaching promptly.
- As a lecturer, I want to see who has marked attendance in real time so that I have visibility during class.
- As a lecturer, I want accurate, exportable records so that I do not spend time reconciling paper sheets.

Admin

- As a department officer, I want reliable attendance data so that exam eligibility decisions are based on truth.

Acceptance Criteria

AC-01: Student Authentication and Attendance Marking

- Student must be authenticated with a valid university ID and password or OTP.
- Student must be enrolled in the course linked to the session.
- Student can mark attendance only when the session is active.
- Student can mark attendance only within the configured time window.
- Student can mark attendance only within the configured geofence radius.
- Duplicate attendance for the same student and session must be blocked.
- Successful marking must show a confirmation message.

AC-02: Lecturer Creates Attendance Session

- Lecturer must be authenticated and assigned to the course.
- Lecturer must provide course, date, start time, duration, and location.
- System must generate a unique session code or QR code.
- Session must open and close according to the configured time rules.
- Lecturer must be able to see the session status: scheduled, active, closed, or extended.

AC-03: Prevent False Attendance

- A student cannot mark attendance for another student.
- One student account can record only one attendance entry per session.
- Attendance must be rejected if the student is outside the geofence.
- Attendance must be rejected if the time window has closed.
- If proof-of-presence is enabled, attendance must be rejected when proof is missing or invalid.
- Every attendance attempt, successful or failed, must be recorded in the audit log.

AC-04: Lecturer Real-time Attendance View

- Lecturer must see attendance count update in real time.
- Lecturer must see the list of students who have marked attendance.
- Lecturer must be able to refresh or view live status during the session.
- Data displayed must match the audit log.

AC-05: Close or Extend Session

- Lecturer can close an active session.
- Lecturer can extend a session only within allowed rules.
- Closing or extending a session must be recorded in the audit log with lecturer ID, timestamp, and reason where applicable.
- Students cannot mark attendance after the session is closed.

AC-06: Export Attendance Report

- Lecturer can export attendance for a selected session.
- Admin can export attendance by course, student, or date range.
- Export must include student identity, session, timestamp, verification status, and attendance status.
- Export must not include unauthorized private data.
- Export must be generated in a usable format such as CSV or PDF.

AC-07: Admin Report and Management

- Admin can view and export attendance reports by course, student, or date range.
- Admin can manage users, courses, and enrollments according to assigned permissions.
- Admin actions must be recorded in the audit log.

AC-08: Audit Log

- System must record who marked attendance, when, and verification status.
- System must record session creation, extension, closure, and manual overrides.
- Audit records must be tamper-resistant and accessible only to authorized roles.

AC-09: Notification

- Students must receive a notification when a session opens, if notifications are enabled.
- Notification failure must not prevent attendance marking.

AC-10: Proof-of-presence, if Enabled

- If live photo or other proof is enabled, the system must define what is captured, how it is verified, and how long it is retained.
- Proof data must be accessible only to authorized users.
- A failed proof check must reject attendance with a clear reason.

Student Metrics

- No false attendance.
- Less than 15 seconds per student to mark attendance.
- Reduction in time spent on attendance.
- Ensure accurate attendance.

Assumptions

- Students have smartphones with location services enabled.
- The classroom has a digital way to display the QR code.
- The university can provide or allow student identity verification (matric number, passwords, or OTP).
- Lecturers are willing to use a digital tool instead of paper.
- Internet connectivity is available in most lecture rooms.

High-Level Technical Considerations

- Frontend: Mobile app and a simple web dashboard for lecturers and admins.
- Backend: FastAPI.
- Database: PostgreSQL.
- Authentication: University ID.
- Hosting: Cloud (such as the university server or AWS).

Risks & Mitigations

- Low lecturer adoption.
- Network issues in lecture halls.

Proposed Timeline

- Research & Design: 1–2 weeks.
- Core Backend and Authentication: 6–9 weeks.
- Student & Lecturer Apps: 5–6 weeks.
- Testing: 5–7 days.
- Documentation and Demo: 1 week.