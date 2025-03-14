# Healthcare Management System

A robust healthcare platform that streamlines patient registration, appointment scheduling, and medical record management using Next.js, Appwrite, TypeScript, and TailwindCSS. This project is designed to efficiently manage healthcare services with a focus on user experience, secure data handling, and responsive design.

---

## ✨ Features

- **Patient Registration:** Create and manage secure patient profiles. 
- **Appointment Booking:** Schedule and track appointments with ease. 
- **Admin Management:** Comprehensive tools for administrators to confirm, reschedule, or cancel appointments.
- **SMS Notifications:** Automated alerts via Twilio for appointment confirmations and updates.
- **Responsive Design:** Optimized for seamless use on desktops, tablets, and mobile devices.
- **Secure File Uploads:** Integrated with Appwrite Storage to handle sensitive files.
- **Performance Monitoring:** Uses Sentry for real-time error tracking and performance insights.

---

## 🛠️ Technical Architecture

- **Frontend:** Next.js for a modern, server-rendered React application.
- **Backend:** Appwrite for data storage, authentication, and file management.  
- **Language:** TypeScript for enhanced code quality and maintainability.
- **Styling:** TailwindCSS for rapid, responsive UI development.
- **SMS Service:** Twilio for instant SMS notifications.
- **Monitoring:** Sentry for real-time error tracking and performance insights.

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/LankeSathwik7/healthcare-management-system.git
cd healthcare-management-system
```

Install project dependencies:

```bash
npm install
```

Set up environment variables:

1. Create a `.env.local` file in the project root.
2. Add your Appwrite credentials:

```env
# APPWRITE
NEXT_PUBLIC_ENDPOINT=https://cloud.appwrite.io/v1
PROJECT_ID=your_project_id
API_KEY=your_api_key
DATABASE_ID=your_database_id
PATIENT_COLLECTION_ID=your_patient_collection_id
APPOINTMENT_COLLECTION_ID=your_appointment_collection_id
NEXT_PUBLIC_BUCKET_ID=your_bucket_id

NEXT_PUBLIC_ADMIN_PASSKEY=111111
```

Replace the placeholders with your actual credentials.

---

## 🚀 Usage

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to access the application. Use the intuitive interface to:

- Register new patients. 
- Schedule and manage appointments.
- Receive SMS notifications for appointment updates.

---

## ⚙️ Configuration Options

| **Category**        | **Available Options**                  |
|---------------------|----------------------------------------|
| User Roles          | Patient, Administrator                 |
| Notification Method | SMS (Twilio)                           |
| File Uploads        | Appwrite Storage                       |
| UI Framework        | Next.js, TailwindCSS                   |

---

## 🗂️ Project Structure

```plaintext
.
├── README.md
├── app
│   ├── admin
│   │   └── page.tsx
│   ├── api
│   │   └── sentry-example-api
│   │       └── route.ts
│   ├── favicon.ico
│   ├── global-error.tsx
│   ├── globals.css
│   ├── layout.tsx
│   ├── loading.tsx
│   ├── page.tsx
│   ├── patients
│   │   └── [userId]
│   │       ├── new-appointment
│   │       │   ├── page.tsx
│   │       │   └── success
│   │       │       └── page.tsx
│   │       └── register
│   │           └── page.tsx
│   └── sentry-example-page
│       └── page.tsx
├── components
│   ├── AppointmentModal.tsx
│   ├── CustomFormField.tsx
│   ├── FileUploader.tsx
│   ├── PasskeyModal.tsx
│   ├── StatCard.tsx
│   ├── StatusBadge.tsx
│   ├── SubmitButton.tsx
│   ├── ThemeProvider.tsx
│   ├── forms
│   │   ├── AppointmentForm.tsx
│   │   ├── PatientForm.tsx
│   │   └── RegisterForm.tsx
│   ├── table
│   │   ├── DataTable.tsx
│   │   └── columns.tsx
│   └── ui
│       ├── alert-dialog.tsx
│       ├── button.tsx
│       ├── checkbox.tsx
│       ├── command.tsx
│       ├── dialog.tsx
│       ├── form.tsx
│       ├── input-otp.tsx
│       ├── input.tsx
│       ├── label.tsx
│       ├── popover.tsx
│       ├── radio-group.tsx
│       ├── select.tsx
│       ├── separator.tsx
│       ├── table.tsx
│       └── textarea.tsx
├── components.json
├── constants
│   └── index.ts
├── instrumentation.ts
├── lib
│   ├── actions
│   │   ├── appointment.actions.ts
│   │   └── patient.actions.ts
│   ├── appwrite.config.ts
│   ├── utils.ts
│   └── validation.ts
├── next-env.d.ts
├── next.config.mjs
├── package-lock.json
├── package.json
├── postcss.config.mjs
├── public
│   ├── assets
│   │   ├── gifs
│   │   │   └── success.gif
│   │   ├── icons
│   │   │   ├── appointments.svg
│   │   │   ├── arrow.svg
│   │   │   ├── calendar.svg
│   │   │   ├── cancelled.svg
│   │   │   ├── check-circle.svg
│   │   │   ├── check.svg
│   │   │   ├── close.svg
│   │   │   ├── email.svg
│   │   │   ├── loader.svg
│   │   │   ├── logo-full.svg
│   │   │   ├── logo-icon.svg
│   │   │   ├── pending.svg
│   │   │   ├── upload.svg
│   │   │   └── user.svg
│   │   └── images
│   │       ├── admin.png
│   │       ├── appointment-img.png
│   │       ├── appointments-bg.png
│   │       ├── cancelled-bg.png
│   │       ├── dr-cameron.png
│   │       ├── dr-cruz.png
│   │       ├── dr-green.png
│   │       ├── dr-lee.png
│   │       ├── dr-livingston.png
│   │       ├── dr-peter.png
│   │       ├── dr-powell.png
│   │       ├── dr-remirez.png
│   │       ├── dr-sharma.png
│   │       ├── onboarding-img.png
│   │       ├── pending-bg.png
│   │       └── register-img.png
│   ├── favicon.ico
│   ├── next.svg
│   └── vercel.svg
├── sentry.client.config.ts
├── sentry.edge.config.ts
├── sentry.server.config.ts
├── tailwind.config.ts
├── tsconfig.json
└── types
    ├── appwrite.types.ts
    └── index.d.ts
```

---

## 🤝 Contributing

1. Fork the repository  
2. Create your feature branch:
   ```bash
   git checkout -b feature/new-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add new feature'
   ```
4. Push the branch:
   ```bash
   git push origin feature/new-feature
   ```
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](./LICENSE) file for details.

---

## 🙏 Acknowledgements

- **JavaScript Mastery:** For inspiring this project through their detailed tutorial.
- **Next.js, Appwrite, TypeScript, TailwindCSS:** For the robust technologies powering this system. 
- **Twilio & Sentry:** For enabling SMS notifications and performance monitoring.
- Thanks to the open-source community for the invaluable tools and libraries that make projects like these possible.

---

## 📝 Note

This Healthcare Management System is designed to streamline patient and appointment management using modern web development practices. Please review and adapt the system to meet your specific healthcare service requirements.