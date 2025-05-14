# How to target a button that is not always loaded into the DoM (may not be the best way)

```js
// checks all clicks then checks if the id of a click matches our target
//    prevents selecting un-loaded dynamic content
document.addEventListener("click", (event) => {

    if (event.target.classList.contains("targetBtnClass")) { // this has to be a class target, I don't know if this can be done with an id
        const targetBtnId = document.getElementById("targerBtnId"); // now we target the specific button value we want (using id)
        console.log(targetBtnId.value);
    }
});
```

There has to be a better way but this is the one I have found that works
