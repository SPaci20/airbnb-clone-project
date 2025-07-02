Requirements Document
This document outlines the key requirements for the system, derived from the provided database schema.

1. Functional Requirements
1.1 User Management
FR1.1.1 User Registration: The system shall allow new users to register by providing their first name, last name, email, and password.

FR1.1.2 User Authentication: The system shall allow registered users to log in using their email and password.

FR1.1.3 User Profiles: The system shall store and display user profiles including first name, last name, email, phone number (optional), and role.

FR1.1.4 Role Assignment: The system shall support three user roles: guest, host, and admin.

FR1.1.5 Unique Email: Each user's email address must be unique within the system.

1.2 Property Management
FR1.2.1 Property Listing: Hosts shall be able to list new properties, providing details such as name, description, location, and price per night.

FR1.2.2 Property Viewing: Users shall be able to view details of available properties.

FR1.2.3 Property Updates: Hosts shall be able to update their existing property listings.

FR1.2.4 Host Association: Each property must be associated with a host.

1.3 Booking Management
FR1.3.1 Property Booking: Users shall be able to book properties for specific date ranges.

FR1.3.2 Booking Status: Bookings shall have a status of pending, confirmed, or canceled.

FR1.3.3 Total Price Calculation: The system shall calculate the total price for a booking based on the property's price per night and the duration of the stay.

FR1.3.4 Booking History: Users shall be able to view their past and upcoming bookings.

FR1.3.5 Booking Confirmation/Cancellation: The system shall allow for the confirmation or cancellation of bookings.

1.4 Payment Processing
FR1.4.1 Payment Recording: The system shall record payments made for bookings, including the amount, payment date, and payment method.

FR1.4.2 Supported Payment Methods: The system shall support credit_card, paypal, and stripe as payment methods.

FR1.4.3 Payment-Booking Linkage: Each payment must be linked to a valid booking.

1.5 Review System
FR1.5.1 Review Submission: Users shall be able to submit reviews for properties they have booked, including a rating (1-5) and a comment.

FR1.5.2 Review Viewing: Users shall be able to view reviews for properties.

FR1.5.3 Review Association: Each review must be linked to a specific property and the user who wrote it.

1.6 Messaging System
FR1.6.1 User Messaging: Users shall be able to send messages to other users.

FR1.6.2 Message Content: Messages shall contain a body and a timestamp of when they were sent.

FR1.6.3 Sender/Recipient Tracking: Each message must clearly identify the sender and the recipient.

2. Non-Functional Requirements
2.1 Performance
NFR2.1.1 Response Time: Key operations (e.g., property search, booking creation) should complete within acceptable timeframes (e.g., under 2 seconds).

NFR2.1.2 Scalability: The system should be able to handle a growing number of users, properties, and bookings.

2.2 Security
NFR2.2.1 Data Protection: User passwords shall be stored as secure hashes.

NFR2.2.2 Access Control: User roles shall enforce appropriate access to system functionalities (e.g., only hosts can list properties, only admins can manage all data).

NFR2.2.3 Data Integrity: Data consistency and integrity shall be maintained through proper use of primary keys, foreign keys, and constraints.

2.3 Usability
NFR2.3.1 User Interface: The system should provide an intuitive and easy-to-use interface for all user roles.

NFR2.3.2 Error Handling: The system should provide clear and helpful error messages to users.

2.4 Data Integrity & Constraints
NFR2.4.1 Email Uniqueness: The system must enforce unique email addresses for users.

NFR2.4.2 Rating Validation: Review ratings must be between 1 and 5, inclusive.

NFR2.4.3 Enumerated Values: System fields like role, status, and payment_method must adhere to their predefined enumerated values.

2.5 Reliability
NFR2.5.1 Data Persistence: All data shall be persistently stored in the database.

NFR2.5.2 Data Backup: Regular backups of the database should be performed.

2.6 Maintainability
NFR2.6.1 Code Clarity: The codebase should be well-structured, documented, and easy to understand for future development and maintenance.

NFR2.6.2 Testability: The system components should be designed to be testable.

2.7 Indexing
NFR2.7.1 Optimized Queries: Key fields (user_id, email, property_id, booking_id) shall be indexed to optimize database query performance.