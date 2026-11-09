# Khaled Math Study Portal

Student and teacher portal prototype for G12A–G12D.

## Demo accounts
- Teacher: teacher / math123
- Student: student1 / study123 (G12A)
- Student: student2 / study123 (G12B)

## Features
- Student dashboard with pending assignments, next quiz, class materials and profile.
- Teacher dashboard with student account creation, material publishing, assignment creation, quiz scheduling and announcements.
- Class-specific resources and assignments.
- Students can mark assignments complete.
- Responsive mobile navigation and layout.

## Important: demo database limitation
GitHub Pages only hosts static files. This version stores data in the current browser's localStorage. Data is not shared between students or devices, and demo passwords are not secure. Do not enter real student information or real passwords.

## Production database (later)
Create a new, separate Firebase project for this portal. Connect Firebase Authentication and Cloud Firestore collections: users, materials, assignments, quizzes, announcements, and completions. Enforce teacher permissions with custom claims and Firestore Security Rules. Never store plaintext passwords in Firestore.

## Publish with GitHub Pages
In repository Settings > Pages, choose Deploy from a branch, select main and /(root), then save.

Website: https://beshoy1402.github.io/khaled-math-study-portal/
