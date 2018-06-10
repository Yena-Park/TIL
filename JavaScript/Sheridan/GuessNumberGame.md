```javaScript
<!DOCTYPE html>
<html>

<head>
  <title> Guess number 2 </title>
  <meta charset="utf-8">
</head>

<body>
  <h1> Example </h1>
  <main>
    <!-- Prompt the user to guess a number between 1 and 10 -->
    <label> Guess a magic number between 1 and 10 </label>
    <!-- Capture and process user input on the click event -->
    <input type="number" id="guess" value="0" min="1" max="10">
    <p id="ans"></p>
  </main>
  <footer>
    <address> Web Programming </address>
  </footer>

  <script>
    //Generate a random number to be guessed
    var y = Math.floor((Math.random() * 10) + 1);
    console.log(y);
    var x = 0;

    //Prompt the user to guess a number between 1 and 10
    /*
      When the user chooses a number in the input element id=guess
      and clicks the element, the number is captured and processed.
      The response is displayed in the paragraph element id=ans.
      Need a handles for the Element objects (par of DOM).
    */
    var ans = document.getElementById("ans");
    var guess = document.getElementById("guess");

    guess.onclick = function () {
      x = parseInt(guess.value);
    }
    //Determine whether the guess is the same as the number
    //if yes, let the user know
    //if no, determin if
    //      guess is higher than number, let user know
    //      guess is lower than number, let user know
    if (x == y) {
      ans.innerText = "Yes, the number is " + y;
      //TODO: put in a delay to see the result.
      location.reload(); //reload page to start new game
    }
    else if (x < y) {
      ans.innerText = "Your guess is too low";
    }
    else {
      ans.innerText = "Your guess is too high";
    }
  </script>
</body>

</html>
```
