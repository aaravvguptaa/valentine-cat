<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f9f9f9;
        }

        #catImage {
            width: 300px;
            height: auto;
            margin-bottom: 20px;
        }

        #buttonsContainer {
            display: flex;
        }

        .button {
            margin: 0 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        #yesButton {
            background-color: green;
            color: white;
        }

        #noButton {
            background-color: red;
            color: white;
        }
    </style>
</head>
<body>
    <img id="catImage" src="https://placekitten.com/300/200" alt="Cute Cat">
    <div id="buttonsContainer">
        <button id="noButton" class="button" onclick="noButtonClick()">No</button>
        <button id="yesButton" class="button" onclick="yesButtonClick()">Yes</button>
    </div>

    <script>
        let yesButton = document.getElementById('yesButton');
        let noButton = document.getElementById('noButton');

        function noButtonClick() {
            // Increase the size of the yesButton
            yesButton.style.padding = `${parseInt(yesButton.style.padding) + 5}px`;

            // Check if the yesButton has become too big
            if (parseInt(yesButton.style.padding) >= 60) {
                // Display "yay" when yesButton is clicked after becoming too big
                alert("Yay! 🎉 You said yes!");
            }
        }

        function yesButtonClick() {
            // Display "yay" when yesButton is clicked
            alert("Yay! 🎉 You said yes!");
        }
    </script>
</body>
</html>
