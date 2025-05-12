# AirBnB Clone Use Case Diagram Specification

## Actors

### Primary Actors
1. **Guest**
   - Unregistered User
   - Registered User

2. **Host**
   - Property Owner
   - Listing Manager

3. **Admin**
   - System Supervisor
   - Platform Manager

## Use Cases by Actor

### Guest Use Cases
#### Authentication
- Register for an account
- Log in / Log out
- Reset password
- OAuth login (Google, Facebook)

#### Property Interaction
- Search for properties
- Filter and sort properties
- View property details
- Check property availability

#### Booking Process
- Select booking dates
- Choose number of guests
- Make a booking
- View booking history
- Cancel a booking
- Modify a booking

#### Payment
- Process booking payment
- View payment history
- Handle payment methods
- Request refund

#### Review System
- Write property review
- View property reviews
- Rate property and host

#### Communication
- Send messages to host
- Receive booking confirmations
- Manage notification preferences

### Host Use Cases
#### Authentication
- Register as a host
- Log in / Log out
- Verify account

#### Property Management
- Create property listing
- Edit property details
- Set pricing
- Manage availability calendar
- Upload property images
- Define house rules
- Deactivate/Activate listing

#### Booking Management
- View booking requests
- Accept/Reject bookings
- Manage booking calendar
- Block specific dates

#### Financial Management
- View booking earnings
- Manage payout methods
- Track financial performance

#### Review Management
- Respond to guest reviews
- View guest ratings

#### Communication
- Respond to guest messages
- Manage communication preferences

### Admin Use Cases
#### User Management
- View all user accounts
- Suspend/Ban users
- Verify host accounts
- Manage user roles

#### Property Oversight
- Review property listings
- Remove inappropriate listings
- Verify property details
- Handle property disputes

#### Booking Management
- Monitor booking activities
- Resolve booking conflicts
- Generate booking reports

#### Financial Monitoring
- View platform revenue
- Generate financial reports
- Manage payment disputes
- Track host payouts

#### System Management
- Configure platform settings
- Manage site-wide notifications
- Monitor system performance
- Handle security incidents

## Use Case Relationships

### Generalization Relationships
- Unregistered User → Registered User (inheritance)
- Registered User → Guest (inheritance)
- Registered User → Host (inheritance)

### Include Relationships
- Book Property
  - Include: Check Availability
  - Include: Process Payment
  - Include: Generate Booking Confirmation

- Create Property Listing
  - Include: Upload Images
  - Include: Set Pricing
  - Include: Define Availability

### Extend Relationships
- Search Properties
  - Extend: Filter Properties
  - Extend: Sort Properties

- Make Booking
  - Extend: Apply Discount
  - Extend: Add Special Requests

## Interaction Flows

### Registration Flow
1. User selects registration type (Guest/Host)
2. Enter personal information
3. Verify email/phone
4. Complete profile setup

### Booking Flow
1. Search and select property
2. Check availability
3. Select dates and guests
4. Review property details
5. Process payment
6. Receive booking confirmation

### Property Listing Flow
1. Host initiates listing creation
2. Enter property details
3. Upload property images
4. Set pricing and availability
5. Define house rules
6. Submit for review (if required)