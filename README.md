# Geolocation, Speedometer, and Compass

A page built to practice using geolocation data. Built for Wes Bos' [JavaScript 30](https://javascript30.com/) course.

![Screenshot of geolocation page](https://res.cloudinary.com/gerhynes/image/upload/v1517316746/Screenshot-2018-1-30_Document_ggdg79.png)

## Notes

Geolocation provides more than just latitude and longitude. Heading, for example, tells you how many degrees off north you are, as well as your speed.

You cannot access gelocation unless you are on a secure origin.

Xcode can simulate heading, whereas Chrome, Firefox etc. cannot, so this project doesn't have full functionality.

So in theory:

Select the compass arrow and the speed value.

Listen for the user's position using `navigator.geolocation.watchPosition`.

`getCurrentPosition` will give you your current position at time of asking. `watchPosition` will observe your position and update the geolocation data.

Update the speed value. `speed.textContent = data.coords.speed;`

Rotate the compass depending on the heading.

```js
arrow.style.transform = `rotate(${data.coords.heading}deg)`;
```

Add an error callback and alert the user if they haven't allowed acces to their location.
