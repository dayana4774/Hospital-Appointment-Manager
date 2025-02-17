# Hospital Appointments Plugin

A WordPress plugin for managing hospital appointments and doctor schedules.

## Description

The Hospital Appointments plugin allows hospitals and medical practices to manage doctor appointments through their WordPress website. Patients can book appointments online, and administrators can manage doctors and appointments through the WordPress dashboard.

## Features

### Frontend
- Appointment booking form for patients
- Doctor availability check
- Time slot selection
- Automatic email notifications
- Mobile-responsive design

### Admin Panel
1. View Appointments
   - List all booked appointments
   - Patient details (name, email)
   - Doctor assigned
   - Appointment date and time
   - Status management (Pending, Confirmed, Completed, Cancelled)

2. Manage Doctors
   - Add/Edit/Delete doctors
   - Set doctor details:
     - Name
     - Specialty
     - Available days
     - Time slots

## Installation

1. Download the plugin zip file
2. Go to the WordPress admin panel
3. Navigate to Plugins → Add New
4. Click "Upload Plugin"
5. Choose the downloaded zip file
6. Click "Install Now"
7. Activate the plugin

## Usage

### Adding the Booking Form
Add the booking form to any page using the shortcode:
[hospital_appointment_form]

### Managing Doctors
1. Go to WordPress admin panel
2. Navigate to "Hospital Appointments" → "Manage Doctors"
3. Click "Add New Doctor"
4. Fill in the doctor's details:
   - Name
   - Specialty
   - Select available days
   - Enter time slots (one per line)
5. Click "Add Doctor"

### Managing Appointments
1. Go to WordPress admin panel
2. Navigate to "Hospital Appointments" → "View Appointments"
3. View all appointments
4. Change appointment status using the dropdown

## Requirements

- WordPress 5.0 or higher
- PHP 7.4 or higher
- MySQL 5.6 or higher

## Database Tables

The plugin creates two custom tables:

1. `{prefix}ha_doctors`
   - id (Primary Key)
   - name
   - specialty
   - available_days
   - time_slots

2. `{prefix}ha_appointments`
   - id (Primary Key)
   - patient_name
   - patient_email
   - doctor_id
   - appointment_date
   - appointment_time
   - status
   - created_at

## Shortcodes
Displays the appointment booking form.

[hospital_appointment_form]

## CSS Classes

Key CSS classes for styling:
- `.ha-appointment-form-wrapper`: Main form container
- `.ha-form-row`: Form row container
- `.ha-submit-btn`: Submit button
- `.ha-form-message`: Message container
- `.ha-message-content`: Message content

## Actions and Filters

### Actions
- `ha_after_appointment_booked`: Fires after an appointment is booked
- `ha_after_appointment_status_change`: Fires after appointment status changes

### Filters
- `ha_appointment_statuses`: Modify available appointment statuses
- `ha_validation_messages`: Modify form validation messages

## Customization

### Custom Styling
Add custom CSS to your theme's stylesheet:

CSS

/ Example customizations /
.ha-appointment-form {
max-width: 600px;
margin: 0 auto;
}
.ha-submit-btn {
background-color: #4CAF50;
color: white;
}


## Troubleshooting

Common issues and solutions:

1. Form not displaying
   - Check if the shortcode is properly inserted
   - Verify plugin is activated

2. Emails not sending
   - Check WordPress email settings
   - Verify email configuration in hosting

3. Time slots not showing
   - Ensure the doctor has time slots entered
   - Check the JavaScript console for errors

## Support

For support, please:
1. Check the documentation
2. Search existing issues
3. Create a new issue on the plugin's repository

## License

This plugin is licensed under the GPL v2 or later.

## Credits

Developed by Dayana babu

## Changelog

### 1.0.0
- Initial release
- Basic appointment booking functionality
- Doctor management
- Appointment management
- Email notifications

## Future Enhancements

Planned features for future releases:
1. Calendar view for appointments
2. SMS notifications
3. Payment integration
4. Custom fields for appointments
5. Export functionality
6. Multiple location support

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
