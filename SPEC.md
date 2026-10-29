




# DeskHub One-page spec

#Problem
Desks are overbooked, walk-in members cannot see which desk are free, so bookings get lost.

## Who uses it 
-Member:Books a desk or room, pays, view and cancles their own bookings.
-Admin: Views occupancy across the space and manages space 
-Walk-in guest: Views the desk map in read only guest mode without an account. to book they must sign up or login

##Pages
-Home(public): explains deskhub,links to the map, plans, and signup 
-Desk map (public, read only for guests):green=available, red=occupied, yellow=needs cleaning.
-Book (members):choose desk or room, hour or day, see total, pay. Day passes and monthly plans are shown here as a clear option.
-Plans(Public, dedicated sections):day passes and monthly plans, linked from home 
-My Bookings (members): list own bookings, cancel
-Admin Occupancy (Admin):how many desks are in use now and today 
-login and signup.

## User Flow: member books a desk
1. open the desk map and pick a free desk
2. Choose hourly or day booking, with start and end time.
3. Pay through paystack and test mode.
4. Booking shows as paid and a confirmation email is sent.
5. The booking appears under my bookings.

##Features(build order)
1. Desk and room map with colour status
2. Booking by hour or day, with overlap check.
3. paystack test payment
4. My bookings
5. Admin occupancy view
6. Day passes and monthy plans
7. Booking confirmation email

## Data to save 
- members: id, name, email, role, team_id
-Spaces: id, type, zone, status, capacity.
-bookinga: id, member_id, Space_id, start, end, status
-payments: id, member_id,  booking_id, amount, pass_type, paystack_reference, status 

##How The Business earns
day passes and monthly plans 

##How we will know it works 
- A member can book a free desk and the map turns red
- A booking that overaps an existing one is refused.
- A member sees ony their own bookings.
- An admin sees occupancy.
- a test payment marks the booking as paid.
- A guest can view the the map but cannot book.
