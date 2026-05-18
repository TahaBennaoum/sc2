# Iqraa School - Test Credentials Guide

This document provides the test email addresses and credentials for different user roles in the Iqraa School management system.

## Overview

The application supports the following user roles:
- **ADMIN** - Full system access, user management, reporting
- **DIRECTOR** - School management, staff oversight
- **TEACHER** - Class management, grade entry, attendance
- **STUDENT** - View grades, attendance, courses
- **PARENT** - Monitor child's progress, notifications

---

## Test Credentials by Role

### 1. ADMIN Account
**Email:** `admin@ecole.dz`  
**Password:** `Admin@123456`  
**Role:** ADMIN  
**Status:** APPROVED

**Dashboard Access:**
- User management and validation
- System settings
- Reports and analytics
- Full access to all modules

---

### 2. DIRECTOR Account
**Email:** `director@ecole.dz`  
**Password:** `Director@123456`  
**Role:** DIRECTOR  
**Status:** APPROVED

**Dashboard Access:**
- School administration
- Staff management
- Budget and payments oversight
- Teacher and student records

---

### 3. TEACHER Account
**Email:** `ahmed.benali@ecole.dz`  
**Password:** `Teacher@123456`  
**Role:** TEACHER  
**Status:** APPROVED

**Dashboard Access:**
- Attendance management (mark attendance)
- Grade entry and management
- Student records and analytics
- Class schedule and courses
- Student communication

---

### 4. STUDENT Account
**Email:** `fatima.hadj@ecole.dz`  
**Password:** `Student@123456`  
**Role:** STUDENT  
**Status:** APPROVED  
**Matricule:** `MAT-2024-001`

**Dashboard Access:**
- View personal grades and statistics
- View attendance records
- Course enrollment and schedule
- Access to learning materials
- Notifications

---

### 5. PARENT Account
**Email:** `parent@ecole.dz`  
**Password:** `Parent@123456`  
**Role:** PARENT  
**Status:** APPROVED

**Dashboard Access:**
- Monitor child's grades
- View attendance records
- Receive school notifications
- Payment history and statements
- Child's course information

---

## Additional Test Users for Load Testing

### Additional Teachers
- **Email:** `karim.mansour@ecole.dz`
- **Email:** `sara.khelifi@ecole.dz`

### Additional Students
- **Email:** `ahmed.ahmed@ecole.dz`
- **Email:** `amina.benali@ecole.dz`
- **Email:** `youcef.mansour@ecole.dz`

---

## Setup Instructions

### 1. Create Test Users in Supabase

1. Go to your Supabase dashboard
2. Navigate to **Authentication** → **Users**
3. Click **Add user** for each test account
4. Enter the email and password from above
5. Confirm email verification if needed

### 2. Set User Roles and Status

After creating users in Supabase:

1. Navigate to the **Users** management page in Iqraa School admin panel
2. For each pending user, click the **Validate/Approve** button
3. Assign the appropriate role to each user

### 3. Quick Login Path

1. Navigate to `http://localhost:3000/login` (or your app URL)
2. Enter the email and password from the table above
3. Click **Login**
4. You'll be redirected to the appropriate dashboard based on your role

---

## Features by Role

### Admin Dashboard
- ✓ User validation and management
- ✓ Role assignment
- ✓ System configuration
- ✓ Audit logs
- ✓ Advanced reporting

### Director Dashboard
- ✓ School overview
- ✓ Staff management
- ✓ Student enrollment
- ✓ Financial reports
- ✓ Academic calendar

### Teacher Dashboard
- ✓ Mark attendance (Mark Today tab)
- ✓ View attendance records
- ✓ Enter student grades
- ✓ View grade analytics
- ✓ Manage classes and schedules
- ✓ Access student information

### Student Dashboard
- ✓ View grades and statistics
- ✓ View attendance records
- ✓ Course enrollment
- ✓ Schedule view
- ✓ Download/print records

### Parent Dashboard
- ✓ Monitor child's grades
- ✓ View child's attendance
- ✓ Receive notifications
- ✓ Payment information
- ✓ Academic progress reports

---

## Troubleshooting

### Login Failed
- Ensure user exists in Supabase
- Verify user status is APPROVED (not PENDING)
- Check that password is correct
- Clear browser cache and try again

### Wrong Dashboard Displayed
- Verify the user's role in the Users admin panel
- Try logging out and logging back in
- Check browser developer console for errors

### Can't Access Specific Features
- Verify user has the correct role
- Check permission settings in admin panel
- Ensure feature is not behind a feature flag

---

## Security Notes

⚠️ **Important:** These are test credentials for development only.

- Do NOT use these passwords in production
- Change all credentials before deploying to production
- Implement strong password policies
- Enable two-factor authentication for admin accounts
- Regularly audit user access logs

---

## Environment Setup

Make sure your `.env.local` file is configured with:

```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_key
```

---

## Questions or Issues?

For issues with test credentials or login:
1. Check the browser console for error messages
2. Verify user exists in Supabase Authentication
3. Ensure user is in APPROVED status in the Users panel
4. Review the Authentication Fix Report: `AUTH_FIX_REPORT.md`
