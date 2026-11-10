# Khaled Math Study Portal

Live site: https://beshoy1402.github.io/khaled-math-study-portal/

GitHub Pages hosts the frontend. Supabase Auth, PostgreSQL, private Storage, Row Level Security and a protected Edge Function power the portal.

## First teacher account — required one-time setup
No teacher login is pre-created. Do not expose a secret/service-role key or enable public signup.

1. Open https://supabase.com/dashboard/project/apzleaclwhfwqyqcynav
2. Authentication → Users → Add user → Create new user.
3. Create a confirmed user with email mrkhaled@khaledmath.portal.invalid and a strong password.
4. Copy that user's UUID.
5. In SQL Editor, run the following after replacing the placeholder UUID:

```sql
update public.profiles
set role = 'teacher', class_code = null, display_name = 'Mr Khaled', username = 'mrkhaled'
where id = 'PASTE-USER-UUID-HERE';
```

6. Sign in to the website with username mrkhaled and the password set above.

The teacher can create students from the Students section. Each student signs in with their own username and password.

## Features
- Individual student logins and private profiles.
- Teacher-only student account creation.
- Class-specific resources and private uploaded files.
- Homework with due dates and completion tracking.
- Quiz schedule and study topics.
- Class announcements.
- Responsive mobile navigation.

## Security
The frontend contains only the Supabase publishable key. RLS protects all portal tables. The service-role/secret key is never stored in GitHub. Uploaded files are in a private bucket and served using expiring signed URLs.

## Free tier
This project is intended to stay on Supabase Free. Free-tier quotas and inactivity pausing apply. Do not enable paid add-ons or upgrade billing.
