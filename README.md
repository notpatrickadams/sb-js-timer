# Timers Exercise

## **countdown**

Write a function called countdown that accepts a number as a parameter and every 1000 milliseconds decrements the value and console.logs it. Once the value is 0 it should log “DONE!” and stop.

```jsx
countDown(4);
// 3
// 2
// 1
// "DONE!"
```

```js
function countDown(time) {
  let timer = setInterval(() => {
    time--;
    if (time <= 0) {
      clearInterval(timer);
      console.log("DONE!");
    } else {
      console.log(time);
    }
  }, 1000);
}
```

## **randomGame**

Write a function called randomGame that selects a random number between 0 and 1 every 1000 milliseconds and each time that a random number is picked, add 1 to a counter. If the number is greater than .75, stop the timer and console.log the number of tries it took before we found a number greater than .75.

```js
function randomGame() {
  let num;
  let tries = 0;
  let timer = setInterval(() => {
    num = Math.random();
    tries++;
    if (num > 0.75) {
      clearInterval(timer);
      console.log(`It took ${tries} ${tries == 1 ? "try" : "tries"}.`);
    }
  }, 1000);
}
```
