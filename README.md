# Mentor Connect System


Mentor Connect is a Django-based web application designed to streamline the process of connecting students with teachers for mentorship and scheduling meetings. This system features student registration with OTP verification, a robust teacher appointment dashboard, dynamic timetable views, and more.

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Features

### 1. Student Registration
- **Details Captured:** Name, SAP ID, Date of Birth (DOB), Email, Mobile Number, Password.
- **Email Validation:** Only allows emails ending with `@stu.upes.ac.in`.
- **OTP Verification:** After submitting the form, an OTP is sent to the registered email. Once the OTP is verified, the account is created.

*![Registration Page Screenshot](Images\StudentRegistration.jpg)*


### 2. Email Verification via OTP
- **OTP Process:** Ensures that the student's email is verified through an OTP sent during registration.

*![OTP Verification Screenshot](Images\Verification1.jpg)*
*![OTP Verification Screenshot](Images\Verification2.jpg)*



### 3. Login Page
- **Simple Form:** Includes fields for Email and Password.
- **Forgot Password Option:** Allows users to recover their accounts if needed.

*![Login Page Screenshot](Images\LoginImg.jpg)*


### 4. Dashboard
- **Search Bar:** Allows students to search for professors.
- **Recommendation System:** Suggests relevant teacher names as the student types.
- **Feedback:** Displays a "No results found" message if there is no match.

*![Dashboard Screenshot](Images\TDashboard1.jpg)*
*![Dashboard Screenshot](Images\TDashboard2.jpg)*


### 5. Teacher Timetable View
- **Dynamic Display:** Shows the teacher’s full timetable after selecting a teacher.
- **Real-time Updates:** Reflects the current meeting status, showing occupied slots when a meeting is scheduled.

*![Teacher Timetable Screenshot](Images\Timetable.jpg)*


### 6. Meeting Request
- **Slot Selection:** Students can view available time slots on the teacher’s timetable.
- **Mode Selection:** Option to request a meeting by choosing either online or offline mode.
- **Time Frame:** Students can specify their preferred meeting time.

*![Meeting Request Screenshot](Images\MeetingRequest.jpg)*


### 7. Teacher Approval
- **Email Notifications:** Teachers receive an email for every meeting request.
- **Direct Response:** Teachers can approve or decline meeting requests directly via email.
- **Decline Reason:** Option for teachers to provide a reason if declining a request.
  

### 8. Confirmation Notifications
- **For Approved Meetings:** Both teacher and student receive confirmation emails.
- **For Declined Meetings:** Emails include the reason for cancellation.


### 9. Online Meeting Link and Calendar Reminder
- **Google Meet Integration:** For online meetings, a Google Meet link is generated.
- **Calendar Reminder:** The generated link is sent along with an option to add a calendar reminder.


### 10. Database Setup
- **Student Database:** Stores registration details.
- **Teacher Database:** Contains teacher information (sample data for now).
- **Timetable Database:** Maintains schedule data (sample data for now).
- **Meeting Details Database:** Logs meeting requests and statuses.



### 11. Dynamic Timetable Updates
- **Real-time Sync:** The timetable automatically updates to reflect current meeting requests and scheduled events.



## Tech Stack
- **Backend:** Django
- **Frontend:** HTML, CSS, JavaScript, Bootstrap
- **Database:** MySQL

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/mentor-connect.git
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd mentor-connect
   ```

3. **Create and Activate a Virtual Environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

4. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Configure MySQL Database:**
   - Update your Django settings with the MySQL database credentials.

6. **Run Migrations:**
   ```bash
   python manage.py migrate
   ```

7. **Start the Development Server:**
   ```bash
   python manage.py runserver
   ```

## Usage
- **Student Registration:** Create a new account by filling out the registration form and verifying your email via OTP.
- **Login:** Use your registered credentials to access your account.
- **Dashboard:** Search for professors and view dynamic timetable updates.
- **Meeting Request:** Request meetings by selecting available slots and choosing the preferred meeting mode.
- **Teacher Approval:** Teachers receive email notifications to approve or decline meeting requests.
- **Confirmation & Notifications:** Both parties receive emails based on the meeting request status.

## Project Structure
```
mentor_connect/
├── manage.py
├── mentor_connect/         # Django project configuration files
├── app/                    # Main application folder
│   ├── templates/          # HTML templates for the UI
│   ├── static/             # Static assets: CSS, JavaScript, Images
│   ├── models.py           # Database models
│   ├── views.py            # Application views
│   └── urls.py             # URL routing configuration
└── requirements.txt        # List of Python dependencies
```

## Contributing
Contributions are welcome! Feel free to fork the repository and submit pull requests with enhancements or fixes.

