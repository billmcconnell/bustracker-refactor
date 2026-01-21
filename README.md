# bustracker

### Tracks the progress of the MBTA 1 Bus route through Cambridge, MA, from the MIT Campus to Harvard

Select the button **Show stops between MIT and Harvard** to move the map marker along the stops. Once the marker stops, refresh the page to start again. 

<a href="https://billmcconnell.github.io/bustracker/">Go to the bustracker project</a>

This project uses the following:

1. html
2. css
3. javascript
4. data from the MBTA API
5. A license from Mapbox, embedded in the javascript code
6. An MIT license

Several improvements may be made to this project, including:

- Automated page refresh
- Banners with the name for each stop
- A marker for each bus on the route
- information about each bus, including capacity information
# bustracker-refactor

  ## Summary of Changes                      
  
  File Modified: mapanimation js:89-103
  
  What was Added:           
  - When the animation completes (all bus stops visited), the page now automatically refreshes after 3 seconds
  - The 3-second delay allows users to see the final marker position at Harvard before the page resets
  - This enables continuous looping of the animation

  Implementation:                            
  - Added a check in the move() function that detects when counter >= busStops length
  - Schedules location.reload() with a 3-second delay using nested setTimeout() 
  - Minimal change (4 new lines) that doesn't modify any existing animation logic

  The animation now flows continuously: user clicks the button → marker animates through all stops → page refreshes after 3 seconds → user can click the button again to restart.
  