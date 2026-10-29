# DeskHub Project Rules

## Project Overview
DeskHub is a co-working space booking website for a school project.

## Core Rules
- Build ONLY the features listed below.
- Add new features ONLY after the core works.
- Never put secret keys in the code.
- Keep secret keys in a file called .env.local and never commit it to GitHub.

## Core Features
1. **Desk and room map** - Show desks and rooms with color indicators:
   - Green = Available
   - Red = Occupied
   - Yellow = Needs cleaning
2. **Booking by hour or day** - Allow members to book by hour or by day
3. **Paystack test payment** - Integrate Paystack test payment for bookings
4. **My bookings for members** - Members can view their own bookings
5. **Admin occupancy view** - Admins can view overall occupancy
6. **Day passes and monthly plans** - Support day passes and monthly plans
7. **Booking confirmation email** - Send booking confirmation emails

## Roles
- **Members** - Regular users who can book spaces
- **Admin** - Can view occupancy and manage the space

## Database Tables
- **members** - Member/user information
- **spaces** - Desks and rooms available for booking
- **bookings** (with start and end time) - Booking records with start and end times
- **payments** (with booking_id and paystack reference) - Payment records linked to bookings via booking_id with Paystack reference
