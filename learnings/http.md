## 1. Write code that executes asynchronously

In my scripts.js, I've implemented async functions to execute asynchronous operations. For instance:
```javaScript
async function getPostcodeCoordinates(postcode) {...}
```

## 2. Use callbacks to access values that aren’t available synchronously
I've utilized event listeners as callbacks in my code:
```javaScript
postcodeInput.addEventListener("keydown", function (event) {...});
```

## 3. Use promises to access values that aren’t available synchronously
In my getPostcodeCoordinates function, I've employed the fetch method, which inherently returns a promise:
```javaScript
const response = await fetch(url);
```

## 4. Use the fetch method to make HTTP requests and receive responses
I've made several HTTP requests using the fetch method in my code, such as:
```javaScript
const response = await fetch(url);
```

## 5. Configure the options argument of the fetch method to make GET and POST requests
Within the code I provided, I'm primarily making GET requests with fetch. An example is:
```javaScript
const boundaryResponse = await fetch(boundaryUrl);
```

## 6. Use the map array method to create a new array containing new values
I utilized the map method in the fetchAndDrawBoundaryCoordinates function to convert boundaryData into a format suitable for Leaflet:
```javaScript
const leafletCoords = boundaryData.map((coord) => [...]);
```

## 7. Use the filter array method to create a new array with certain values removed
Though I've employed methods like find in my code, I didn't directly incorporate the filter method in the examples I provided.

## 8. Access DOM nodes using a variety of selectors
I accessed several DOM nodes using methods like getElementById:
```javaScript
const mapElement = document.getElementById("map");
```

## 9. Add and remove DOM nodes to change the content on the page
While I didn't directly add or remove any DOM nodes, I modified the content of certain nodes in the code:
```javaScript
const neighbourhoodLabel = document.getElementById("neighbourhood");
neighbourhoodLabel.textContent = `Crime in: ` + neighbourhoodName;
```

## 10. Toggle the classes applied to DOM nodes to change their CSS properties
In my code, I toggled the spin class on the crosshair element to achieve specific visual effects:
```javaScript
crosshair.classList.add("spin");
crosshair.classList.remove("spin");
```

## 11. Use consistent layout and spacing
I've maintained a consistent layout and spacing throughout my code, ensuring it remains clean and readable.

## 12. Follow a spacing guideline to give our app a consistent feel
I've maintained a consistent layout and spacing throughout my code, ensuring it remains clean and readable.

## 13. Debug client side JS in our web browser
Though direct debugging isn't showcased in the code I provided, I've made use of console.log statements throughout my JavaScript as a debugging aid:
```javaScript
console.log("Success getting crimes");
```

## 14. Use console.log() to help us debug our code
To aid my debugging process, I frequently incorporated console.log in various places. Here's an example:
```javaScript
console.log("Postcode coordinates:", latitude, longitude);
```
