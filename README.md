App introduction:
A ride share flutter application that enables users to book a ride with friends and colleagues. 

Use:
- passengers (colleagues, friends, or strangers either going to same place or being picked up from same place) are able to share a ride together.
Conditions:
- either the pick up location or arrival location must be the same.
- after booking, a chat is created for the ride and passengers within the ride group are able to chat with the driver and each other.

1. Booking steps:
- one user selects either same pick up, or same arrival
For example, user selects same pick up:
- enters the pick up location
- enters the date and time for pick up
- enters how many passengers are sharing this ride
- enters other passengers phone number and arrival location
- finish by clicking 'book now' button

2. After successfull booking, notification is sent to other passengers that a booking has been made. All passengers need to confirm.
- They confirm the booking on the ride page. 
- Status of the booking is 'pending' until all passengers confirm.

3. Ride page - we have a ride page that shows current status of that booking.
- if status is 'pending' - means that other other passengers haven't confirmed yet
- upon each passenger clicking 'confirm' button on this ride page, status is still 'pending', but the request becomes visible on the driver's side. And a driver can now accept this request. (ride page is now changed to 'looking for a driver...')
- when driver accepts the request, status changes to 'accepted', and notification is sent to all passengers. 
- ride page now changed (we've found a driver for you) - displaying the driver's information.
- all passengers must now check the driver's information and choose to confirm 
- upon confirmation from all passengers, the booking is now successfully reserved.


What needs to be implemented (tasks):

Before begining of ride; Ride page:
- top half screen map
- display location markers of all passengers in the booked ride
- display the routes (from pick up location upto the last destination)


* Starting from ride confirmed upto end of ride
1. all users confirm driver and ride is successfully booked
'Ride Page'
2. send notification to user 24 hours before the booked ride starting time
3. send a reminder notification to driver 10 minutes before the 'leave time' (leave time should be 'x' minutes before the pick up time - 'x' being the amount of time it takes to get to the first pick up location from the driver's current location)
4. when driver starts the ride, send notification to all passengers that the driver has started coming and notify them of the estimated arrival time at the first pick up location. eg: 'Driver ... is on the way to passenger ...'s location and will be there in ... minutes'
4+. change the 'ride page' -> the map will change to real time map - showing real time location of the driver while on the move. Should show the markers pointed at each of the passenger's location, and should display the routes in order. The driver's marker will be continuously changing as the driver moves to each of the assigned locations.
5. when driver arrives at each of the locations, should be able to click on 'arrival' button on the driver's ride page. At this time, specific user should receive a notification that the driver has arrived at their location (and static notification message should be sent in the ride group message [eg: driver has arrived at (passenger ...'s location)])
6. next step is for the specific user to enter the car, and click on the button 'entered the car' on their ride page. At the click of this button, button changes to 'confirm arrival' and the driver's position shown on the 'rider page' on all users will be changing again as the driver moves to the next passenger's location. Same happens for all locations.
7. if different arrival location, when each user arrives at their destination, they click on the button 'confirm arrival', but the whole ride becomes complete and closed only when the last passenger confirms their arrival.
8. upon the last arrival location, ride status changes to 'complete' and becomes available for each passenger to rate and leave feedback. Send notificaion to all passengers letting them know the ride has ended and they're able to leave a feedback or rating. The driver receives their payment which is added to their balance. Chat gets closed.
