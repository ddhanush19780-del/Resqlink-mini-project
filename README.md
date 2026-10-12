You are an expert full-stack web developer, UI/UX designer, database architect, and security engineer.

Build a complete production-style full-stack web application called:

RESQLINK
"Emergency Assistance & Safety Platform for India"

The website must look professional, modern, attractive, responsive, and suitable for a college final-year project/demo.

IMPORTANT:
- Build the project completely, not just a UI mockup.
- Generate all required frontend, backend, database, authentication, API, admin, and configuration files.
- Make the application runnable locally.
- Do not leave placeholder buttons or fake functionality where real implementation is possible.
- Explain setup commands in README.md.
- Use environment variables for secrets.
- Never expose admin credentials, OTP secrets, database passwords, API keys, or JWT secrets in frontend code.
- Use secure password hashing.
- Validate all user input.
- Add proper error handling.
- Make the application responsive for mobile, tablet, and desktop.
- The website is intended ONLY for users in India.

==================================================
1. TECHNOLOGY STACK
==================================================

Use this stack:

FRONTEND:
- HTML5
- CSS3
- Vanilla JavaScript
- Responsive design
- Font Awesome or Lucide icons
- Google Fonts if appropriate

BACKEND:
- Node.js
- Express.js
- REST API
- JWT authentication
- bcrypt/bcryptjs for password hashing
- Nodemailer for email OTP
- Twilio or another SMS/OTP provider abstraction for mobile OTP
- dotenv
- express-validator
- cors
- helmet
- rate limiting

DATABASE:
- MongoDB
- Mongoose

MAP/LOCATION:
- Browser Geolocation API
- Google Maps integration
- Google Maps Places/Geocoding APIs where API keys are available
- Provide a clean fallback if Google Maps API key is not configured.
- Restrict location functionality to India.

==================================================
2. PROJECT STRUCTURE
==================================================

Create this structure:

RESQLINK/
│
├── frontend/
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── forgot-password.html
│   ├── dashboard.html
│   ├── emergency-contacts.html
│   ├── sos.html
│   ├── location.html
│   ├── nearby-help.html
│   ├── emergency-services.html
│   ├── notifications.html
│   ├── emergency-history.html
│   ├── profile.html
│   │
│   ├── css/
│   │   ├── style.css
│   │   ├── login.css
│   │   ├── register.css
│   │   ├── dashboard.css
│   │   ├── contacts.css
│   │   ├── sos.css
│   │   ├── location.css
│   │   ├── nearby-help.css
│   │   ├── services.css
│   │   ├── notifications.css
│   │   ├── profile.css
│   │   └── responsive.css
│   │
│   ├── js/
│   │   ├── main.js
│   │   ├── auth.js
│   │   ├── register.js
│   │   ├── login.js
│   │   ├── dashboard.js
│   │   ├── contacts.js
│   │   ├── sos.js
│   │   ├── location.js
│   │   ├── nearby-help.js
│   │   ├── emergency-services.js
│   │   ├── notifications.js
│   │   ├── history.js
│   │   └── profile.js
│   │
│   └── assets/
│       ├── images/
│       ├── icons/
│       └── logo/
│
├── backend/
│   ├── server.js
│   ├── package.json
│   ├── .env
│   ├── .env.example
│   │
│   ├── config/
│   │   ├── db.js
│   │   ├── mail.js
│   │   └── maps.js
│   │
│   ├── models/
│   │   ├── User.js
│   │   ├── EmergencyContact.js
│   │   ├── SOSAlert.js
│   │   ├── Location.js
│   │   ├── EmergencyHistory.js
│   │   ├── EmergencyService.js
│   │   └── Notification.js
│   │
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── userRoutes.js
│   │   ├── contactRoutes.js
│   │   ├── sosRoutes.js
│   │   ├── locationRoutes.js
│   │   ├── nearbyRoutes.js
│   │   ├── serviceRoutes.js
│   │   ├── notificationRoutes.js
│   │   └── adminRoutes.js
│   │
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── userController.js
│   │   ├── contactController.js
│   │   ├── sosController.js
│   │   ├── locationController.js
│   │   ├── nearbyController.js
│   │   ├── serviceController.js
│   │   ├── notificationController.js
│   │   └── adminController.js
│   │
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   ├── adminMiddleware.js
│   │   ├── errorMiddleware.js
│   │   └── rateLimitMiddleware.js
│   │
│   ├── services/
│   │   ├── otpService.js
│   │   ├── emailService.js
│   │   ├── smsService.js
│   │   ├── locationService.js
│   │   └── notificationService.js
│   │
│   └── utils/
│       ├── validators.js
│       ├── indiaLocation.js
│       └── generateOtp.js
│
├── admin/
│   ├── admin-login.html
│   ├── admin-dashboard.html
│   ├── users.html
│   ├── emergency-records.html
│   ├── locations.html
│   ├── services.html
│   ├── notifications.html
│   ├── admin.css
│   └── admin.js
│
├── README.md
└── .gitignore

==================================================
3. WEBSITE DESIGN
==================================================

Create a premium emergency-service visual design.

COLOR THEME:

Use the red Polish-flag-inspired palette described below:

- Dark scarlet red
- Deep red
- Dark pink/crimson accents
- Light gray background
- White cards
- Very dark text
- Subtle shadows
- Minimal gradients
- Professional emergency-service appearance

Suggested CSS variables:

--primary: #9E1B32;
--primary-dark: #720F24;
--accent: #C2185B;
--background: #F3F4F6;
--surface: #FFFFFF;
--text: #1F2937;
--muted: #6B7280;
--success: #16A34A;
--warning: #F59E0B;
--danger: #DC2626;

Do not overuse red.

Use:
- clean cards
- rounded corners
- subtle shadows
- modern navigation
- professional icons
- emergency warning sections
- responsive dashboard
- smooth hover effects
- loading indicators
- toast notifications
- confirmation dialogs

Use appropriate emergency-related images such as:
- ambulance
- hospital
- police
- fire rescue
- emergency phone
- location/map
- first aid
- safety

Do not use copyrighted images unnecessarily. Prefer royalty-free/publicly usable images or CSS/icon-based illustrations.

==================================================
4. HOME PAGE
==================================================

Create a professional landing page.

Header:

RESQLINK logo

Navigation:
- Home
- Emergency Services
- Nearby Help
- About
- Login
- Register

Hero section:

Title:
"Your Safety. One Click Away."

Subtitle:
"ResQLink connects you with emergency contacts, nearby help and essential emergency services across India."

Buttons:
- Get Started
- Emergency Services

Add emergency-themed hero visual.

Add feature cards:

1. SOS Alert
2. Live Location
3. Nearby Help
4. Emergency Contacts
5. Emergency Services
6. Instant Notifications

Add section:
"Emergency Support Across India"

Add footer with:
- ResQLink
- Emergency disclaimer
- India-only service notice
- Privacy Policy
- Terms
- Contact

==================================================
5. USER REGISTRATION
==================================================

Create register.html.

Required fields:

1. Email
2. Full Name
3. Mobile Number
4. Father Name
5. Mother Name
6. Address
7. Age
8. Emergency Contact Number / Parent Number
9. Password
10. Confirm Password
11. OTP verification

Registration requirements:

- Email must be valid.
- Mobile number must be an Indian mobile number.
- Emergency number must be valid.
- Password must satisfy strong-password rules.
- Password confirmation must match.
- Age must be valid.
- OTP must be verified before account creation.
- Store passwords only as hashes.
- Never store plain-text passwords.

OTP flow:

User enters mobile number.

Click:
"Send OTP"

Backend generates a secure 6-digit OTP.

OTP should:
- expire after a short time
- have limited attempts
- have resend cooldown
- be rate limited
- never be stored as plain text if possible

After successful OTP verification:
"Create Account"

Show registration success.

Redirect to login.

==================================================
6. USER LOGIN
==================================================

Create login.html.

Login options:

A. Password Login

Fields:
- Email or Mobile Number
- Password
- Login button

B. OTP Login

Fields:
- Registered email/mobile
- Send OTP
- OTP
- Verify & Login

Below password field:

"Forgot Password?"

"Don't have an account? Register"

If password is incorrect:

Display:
"Incorrect email/mobile or password."

Do not reveal whether an account exists.

==================================================
7. FORGOT PASSWORD
==================================================

Create forgot-password.html.

User enters registered mobile number.

Click:
"Send OTP"

Verify OTP.

Then show:

New Password
Confirm New Password

Reset password.

Use secure password hashing.

Invalidate old sessions/tokens after password reset.

==================================================
8. FIRST LOGIN EMERGENCY CONTACT
==================================================

After first successful login, if the user has not configured an emergency contact:

Show mandatory setup screen.

Title:
"Set Up Your Emergency Contact"

Required:

Name
Relationship
Address
Emergency Mobile Number

Explain:

"This contact will be used for emergency alerts and location sharing."

Do not allow SOS activation until the required emergency contact setup is completed.

After saving:
redirect to dashboard.

==================================================
9. USER DASHBOARD
==================================================

Create a professional dashboard.

Show:

Welcome, [User Name]

Quick action cards:

🚨 SOS
📍 Share Location
🏥 Nearby Hospitals
🚓 Police
🚑 Ambulance
🔥 Fire Service
👨‍👩‍👧 Emergency Contacts
🔔 Notifications
📋 Emergency History

Main central element:

Large RED SOS BUTTON

Text:
"HOLD TO SEND SOS"

Implement press-and-hold behavior rather than accidental one-click activation.

Before sending:
show confirmation:

"Send emergency alert now?"

Buttons:
Cancel
Send SOS

==================================================
10. SOS MODULE
==================================================

Create sos.html and backend SOS APIs.

When SOS is activated:

1. Get current GPS location.
2. Verify location is inside India.
3. Create SOS record in database.
4. Store:
   - user ID
   - timestamp
   - latitude
   - longitude
   - accuracy
   - status
5. Notify emergency contact.
6. Notify admin dashboard.
7. Create user notification.
8. Add event to emergency history.

Location link should be generated in a safe format that opens a map.

Example:

"Emergency alert from [Name].
Current location:
[Google Maps link]"

IMPORTANT:

Do not claim that SMS/WhatsApp/email was successfully delivered unless the configured provider confirms delivery.

If SMS/WhatsApp service is not configured:
show:
"Emergency alert created successfully, but external messaging service is not configured."

==================================================
11. LOCATION MODULE
==================================================

Use Browser Geolocation API.

Request permission clearly.

Show:

Current Location
Latitude
Longitude
Accuracy
Last Updated

Show map when API is configured.

Buttons:

"Get Current Location"
"Share Location"

Only permit location processing for locations within India.

If outside India:

"ResQLink currently supports locations inside India only."

Do not continuously track the user unless they explicitly enable a clearly explained tracking feature.

==================================================
12. NEARBY HELP
==================================================

Create nearby-help.html.

Categories:

🏥 Hospitals
🚓 Police Stations
🔥 Fire Stations
💊 Pharmacies
🚑 Ambulance
🩸 Blood Banks

Get user's current location.

Use Google Maps / Places API when configured.

Show nearby results as cards:

Name
Address
Distance
Phone Number
Open/closed status if available

Buttons:

"Call"
"Open in Google Maps"

Sort by nearest distance.

If Google Maps API is unavailable:
provide a fallback link/search approach and clearly display that live nearby data requires the Maps API.

==================================================
13. EMERGENCY SERVICES
==================================================

Create emergency-services.html.

India-focused services.

Include commonly recognized emergency numbers such as:

112 – Integrated Emergency Number
108 – Ambulance / emergency medical services where applicable
101 – Fire
100 – Police where applicable/legacy routing

IMPORTANT:
Emergency numbers can vary by service and location. Present them as informational and verify current availability through authoritative sources before production deployment.

Each service card:

Icon
Service name
Emergency number
Description
"Call Now"

Use:
tel:+91XXXXXXXXXX

Require double tap/click confirmation for emergency calls:

First click:
"Call Emergency Service?"

Second confirmation:
"Call Now"

Never auto-call without user confirmation.

==================================================
14. EMERGENCY CONTACTS
==================================================

Create emergency-contacts.html.

User can:

Add contact
Edit contact
Delete contact
View contact

Fields:

Name
Relationship
Phone
Address

Mark one contact as primary.

The primary contact is used for SOS notifications.

==================================================
15. NOTIFICATIONS
==================================================

Create notifications.html.

Show:

SOS sent successfully
Location shared
Emergency contact notified
Call initiated
Nearby service found
Failed operation
System alerts

Each notification:

Icon
Title
Message
Timestamp
Read/unread status

Add:
"Mark all as read"

==================================================
16. EMERGENCY HISTORY
==================================================

Create emergency-history.html.

Display:

Date
Time
Emergency type
Location
Status
Notification status

Examples:

SOS Alert
Location Share
Emergency Service Call
Nearby Help Request

Allow user to view their own history only.

==================================================
17. USER PROFILE
==================================================

Create profile.html.

Show:

Name
Email
Mobile
Father name
Mother name
Address
Age
Emergency contact

Allow safe editing.

Do not allow users to edit system-controlled fields improperly.

==================================================
18. ADMIN SYSTEM
==================================================

Create a completely separate admin interface.

Admin pages:

admin-login.html
admin-dashboard.html
users.html
emergency-records.html
locations.html
services.html
notifications.html

ADMIN MUST NEVER USE NORMAL USER LOGIN.

Admin authentication must be handled server-side.

The special admin credentials supplied by the project owner must NOT be hard-coded into frontend HTML/JavaScript.

Store them securely using environment variables and/or a protected Admin database record.

Use:

ADMIN_EMAIL=<configured admin email>
ADMIN_PASSWORD_HASH=<bcrypt hash>

The recovery phone should also be stored securely in an environment variable or protected admin configuration.

Admin password reset:

- OTP can ONLY be sent to the configured recovery number.
- Never allow the admin to choose another recovery number.
- Do not display the full recovery number in the frontend.
- Mask it, for example:
  ******1846

For the development/demo environment, document clearly how to configure the admin credentials in .env.

==================================================
19. ADMIN DASHBOARD
==================================================

Admin dashboard should display:

Total Users
Active Users
Total SOS Alerts
Today's SOS Alerts
Emergency Contacts
Location Events
Notifications

Dashboard charts:

- SOS alerts by day
- User registrations
- Emergency types
- Alert status

Recent SOS alerts table:

User
Emergency Type
Date
Time
Location
Status

Provide:

View
Update status

Do not expose passwords.

Never display password hashes.

==================================================
20. ADMIN USER MANAGEMENT
==================================================

Admin can:

View users
Search users
Filter users
View user details
Disable user account
Enable user account

Admin can view:

Name
Email
Mobile
Address
Age
Parent information
Emergency contact
Registration date
Account status

Do NOT display user passwords.

==================================================
21. ADMIN LOCATION MONITORING
==================================================

Admin can see emergency location events.

Show:

User
Latitude
Longitude
Timestamp
Accuracy
SOS status
Map link

Only store/share location data necessary for the emergency functionality.

Add proper access control.

==================================================
22. ADMIN EMERGENCY SERVICE MANAGEMENT
==================================================

Admin can:

Add service
Edit service
Delete service
Enable/disable service

Fields:

Service name
Category
Emergency number
Description
State/region
Status

Examples:

Police
Ambulance
Fire
Hospital
Blood Bank
Disaster Management

==================================================
23. DATABASE MODELS
==================================================

Create MongoDB/Mongoose models.

USER:

- name
- email
- mobile
- passwordHash
- fatherName
- motherName
- address
- age
- emergencyContact
- isVerified
- isActive
- hasCompletedEmergencySetup
- createdAt
- updatedAt

EMERGENCY CONTACT:

- userId
- name
- relationship
- phone
- address
- isPrimary
- createdAt

SOS ALERT:

- userId
- emergencyContactId
- latitude
- longitude
- accuracy
- timestamp
- status
- notificationStatus

LOCATION:

- userId
- latitude
- longitude
- accuracy
- source
- timestamp

EMERGENCY HISTORY:

- userId
- type
- location
- status
- message
- timestamp

EMERGENCY SERVICE:

- name
- category
- phone
- description
- region
- isActive

NOTIFICATION:

- userId
- type
- title
- message
- read
- createdAt

OTP:

- identifier
- purpose
- hashedOtp
- expiresAt
- attempts
- verified

==================================================
24. REST API
==================================================

Implement proper REST endpoints.

AUTH:

POST /api/auth/register
POST /api/auth/send-register-otp
POST /api/auth/verify-register-otp
POST /api/auth/login
POST /api/auth/send-login-otp
POST /api/auth/verify-login-otp
POST /api/auth/forgot-password
POST /api/auth/reset-password
POST /api/auth/logout

USER:

GET /api/users/me
PUT /api/users/me

CONTACTS:

GET /api/contacts
POST /api/contacts
PUT /api/contacts/:id
DELETE /api/contacts/:id

SOS:

POST /api/sos
GET /api/sos/history

LOCATION:

POST /api/location
GET /api/location/latest

NEARBY:

GET /api/nearby/hospitals
GET /api/nearby/police
GET /api/nearby/fire
GET /api/nearby/pharmacy

SERVICES:

GET /api/services

NOTIFICATIONS:

GET /api/notifications
PUT /api/notifications/:id/read

ADMIN:

POST /api/admin/login
POST /api/admin/send-reset-otp
POST /api/admin/reset-password
GET /api/admin/dashboard
GET /api/admin/users
GET /api/admin/sos
GET /api/admin/locations
GET /api/admin/services
POST /api/admin/services
PUT /api/admin/services/:id
DELETE /api/admin/services/:id

Protect every admin endpoint with admin authentication middleware.

==================================================
25. SECURITY
==================================================

Implement:

- bcrypt password hashing
- JWT authentication
- HTTP-only secure cookies where appropriate
- Helmet
- CORS configuration
- Rate limiting
- Input validation
- MongoDB query safety
- OTP expiry
- OTP attempt limits
- OTP resend cooldown
- Password strength validation
- Authentication middleware
- Admin middleware
- Error handling
- No passwords in logs
- No secrets in frontend
- No API keys in GitHub
- .env in .gitignore

Never store plain-text passwords.

Never return passwordHash in API responses.

==================================================
26. INDIA LOCATION VALIDATION
==================================================

ResQLink is only for India.

Create:

utils/indiaLocation.js

Implement a reasonable geographic valida
