# User Story Template

**Title:**
_As a [user role], I want [feature/goal], so that [reason]._

**Acceptance Criteria:**
1. [Criteria 1]
2. [Criteria 2]
3. [Criteria 3]

**Priority:** [High/Medium/Low]  
**Story Points:** [Estimated Effort in Points]  
**Notes:**
- [Additional information or edge cases]

---

# Admin User Stories

**Title:**
_As an admin, I want to log into the portal with my username and password, so that I can manage the platform securely._

**Acceptance Criteria:**
1. Login page is accessible
2. Valid credentials log the admin in
3. Invalid credentials show an error message

**Priority:** High  
**Story Points:** 2  
**Notes:**
- Use encrypted passwords for login

---

**Title:**
_As an admin, I want to log out of the portal, so that I can protect system access._

**Acceptance Criteria:**
1. Logout button is visible on dashboard
2. Clicking logout redirects to login page
3. Session is properly terminated

**Priority:** High  
**Story Points:** 1  
**Notes:**
- Session should expire after logout

---

**Title:**
_As an admin, I want to add doctors to the portal, so that they can start managing appointments._

**Acceptance Criteria:**
1. Admin can fill doctor details in a form
2. Submit button adds doctor to the database
3. Confirmation is shown after addition

**Priority:** High  
**Story Points:** 3  
**Notes:**
- Doctor’s email must be unique

---

**Title:**
_As an admin, I want to delete a doctor's profile, so that I can remove inactive users._

**Acceptance Criteria:**
1. Admin can select a doctor to delete
2. Confirmation dialog appears before deletion
3. Doctor is removed from system and appointment list

**Priority:** Medium  
**Story Points:** 2  
**Notes:**
- Ensure deleted profiles are not recoverable

---

**Title:**
_As an admin, I want to run a stored procedure in MySQL CLI to get the number of appointments per month, so that I can track usage statistics._

**Acceptance Criteria:**
1. Admin has access to CLI
2. Stored procedure runs successfully
3. Monthly stats are displayed or exported

**Priority:** Medium  
**Story Points:** 3  
**Notes:**
- Ensure data reflects most recent appointments

---

# Patient User Stories

**Title:**
_As a patient, I want to view a list of doctors without logging in, so that I can explore options before registering._

**Acceptance Criteria:**
1. Doctor list is accessible publicly
2. Shows name, specialization, and ratings
3. Search and filter options are available

**Priority:** High  
**Story Points:** 2  
**Notes:**
- Filter by specialization and availability

---

**Title:**
_As a patient, I want to sign up using my email and password, so that I can book appointments._

**Acceptance Criteria:**
1. Signup form captures email and password
2. Email verification is sent after registration
3. Invalid or duplicate emails are rejected

**Priority:** High  
**Story Points:** 2  
**Notes:**
- Password must meet strength criteria

---

**Title:**
_As a patient, I want to log into the portal, so that I can manage my bookings._

**Acceptance Criteria:**
1. Login page is accessible
2. Correct credentials log user in
3. Shows patient dashboard after login

**Priority:** High  
**Story Points:** 2  
**Notes:**
- Login should use secure session tokens

---

**Title:**
_As a patient, I want to log out of the portal, so that I can secure my account._

**Acceptance Criteria:**
1. Logout button logs out user
2. Session is invalidated
3. User is redirected to homepage

**Priority:** Medium  
**Story Points:** 1  
**Notes:**
- Auto-logout on inactivity after 10 minutes

---

**Title:**
_As a patient, I want to book an hour-long appointment, so that I can consult with a doctor._

**Acceptance Criteria:**
1. Select doctor and available time slot
2. Booking is confirmed and visible in dashboard
3. Prevent double-booking

**Priority:** High  
**Story Points:** 3  
**Notes:**
- Time slots should be real-time updated

---

**Title:**
_As a patient, I want to view my upcoming appointments, so that I can prepare accordingly._

**Acceptance Criteria:**
1. Upcoming appointments are shown in dashboard
2. Appointments show doctor details and time
3. Option to cancel if needed

**Priority:** Medium  
**Story Points:** 2  
**Notes:**
- Sort appointments by date

---

# Doctor User Stories

**Title:**
_As a doctor, I want to log into the portal, so that I can manage my appointments._

**Acceptance Criteria:**
1. Secure login screen is available
2. Valid credentials redirect to doctor dashboard
3. Invalid login shows an error message

**Priority:** High  
**Story Points:** 2  
**Notes:**
- MFA may be added for enhanced security

---

**Title:**
_As a doctor, I want to log out of the portal, so that I can protect my data._

**Acceptance Criteria:**
1. Logout option on dashboard
2. Ends current session
3. Redirects to login page

**Priority:** Medium  
**Story Points:** 1  
**Notes:**
- Ensure session is cleared completely

---

**Title:**
_As a doctor, I want to view my appointment calendar, so that I can stay organized._

**Acceptance Criteria:**
1. Calendar view of all upcoming appointments
2. Click to see appointment details
3. Filter by day or week

**Priority:** High  
**Story Points:** 3  
**Notes:**
- Use color codes for appointment status

---

**Title:**
_As a doctor, I want to mark my unavailability, so that patients see only available slots._

**Acceptance Criteria:**
1. Doctor selects unavailable dates/times
2. Unavailable slots are blocked from booking
3. Confirmation after submission

**Priority:** High  
**Story Points:** 3  
**Notes:**
- Allow recurring unavailability (e.g. every Sunday)

---

**Title:**
_As a doctor, I want to update my profile, so that patients have up-to-date information._

**Acceptance Criteria:**
1. Edit profile form is accessible
2. Update name, specialization, contact info
3. Save changes reflects immediately

**Priority:** Medium  
**Story Points:** 2  
**Notes:**
- Add profile picture upload option

---

**Title:**
_As a doctor, I want to view patient details for upcoming appointments, so that I can be prepared._

**Acceptance Criteria:**
1. Each appointment links to patient details
2. View basic info and reason for visit
3. Only future appointments show full details

**Priority:** High  
**Story Points:** 2  
**Notes:**
- Sensitive data should be protected

