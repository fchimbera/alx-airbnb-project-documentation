# 🧾 Use Case Diagram

##👥 Actors
**Guest**: A user who searches and books properties.

**Host**: A user who lists properties for rent.

**Admin**: A system administrator responsible for user and listing moderation.

**Payment Gateway**: External service that handles financial transactions.

##🔍 Core Use Cases
###For Guests:
- **Register Accoun**t: Sign up and create an account.

- **Search Properties**: Look for available properties to book.

- **Book Property**: Reserve a selected property.

- - *Includes*: Make Payment

- **Leave Review**: Provide feedback after a stay.

###For Hosts:
- **Register Accoun**t: Sign up and create an account.

- **List Property**: Publish property details for renting.

- **Update Property**: Modify existing listings.

- **View Bookings**: Track which guests have booked the properties.

- **View Payments**: Monitor incoming transactions.

- **View/Respond to Messages**: Communicate with potential or current guests.

###For Admins:
- **Manage Users**: Add, remove, or edit user accounts.

- **Moderate Listings**: Approve or reject property listings.

###External System:
- **Payment Gateway**: Handles the Make Payment process triggered during bookings.

##✅ Notes
*The Make Payment use case is included in the Book Property process.*

*Each actor interacts with a distinct subset of the system’s functionalities.*

*The Payment Gateway is treated as an external actor responsible for transaction handling.*