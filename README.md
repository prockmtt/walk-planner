# Plan My Walk
Living in Ann Arbor the past few years has taught me 2 things: 1) walking is a convenient hobby to have when you live in a walkable city, but 2) Midwestern weather is not to be relied upon. So I built a tool that makes it even easier to determine when the best time is to go on my daily walk.  
![Image](https://github.com/user-attachments/assets/1bf89506-f364-4298-bbe7-7c0363259429)
Enter your city of choice to learn the best times to take a walk based on today's weather forecast and see a visualizer of the temperature shifts throughout the day. 

https://github.com/user-attachments/assets/399b2346-828a-4809-baa8-394f50d23fb0

## How does it work?
When the user enters a city I call [Weather API](https://www.weatherapi.com/) to find today's hourly forecasts. While the "best" walking weather is subjective, a solid baseline is a sunny, 65-70 degree day. The forecast for rain, snow, cloud cover, temperature, and the time of day/night, are used to calculate a "score" between 0 (best) and 10 (worst) for every hour. A 0 might be 68 degrees with no clouds, and a 10 might be torrential downpour at 3AM. The hour with the best score from the current to to the end of the day is shared, but if the best score was an hour earlier in the day which has already passed, that "peak" walking hour data is displayed as well.
Additionally, the temperature data is also used to create the temperature graph, built using [Chart.js](https://www.chartjs.org/).  

Invalid city values and other API errors are handled and shared clearly with the user.

https://github.com/user-attachments/assets/85b7441f-775f-4868-985e-8025f49972b4

If you have any questions or want to learn more about the code, [feel free to reach out](https://matthewprock.org).
