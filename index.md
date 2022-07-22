<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Weather</title>
    <style>
      h1 {
        text-align: center;
        color: #1a64d6;
        font-size: 34px;
        line-height: 48px;
        margin: 0;
        font-family: Helvetica, Arial, sans-serif;
      }
      h2 {
        text-align: center;
        margin: 0;
        font-size: 34px;
        line-height: 48px;
        font-weight: normal;
        font-family: Helvetica, Arial, sans-serif;
      }
      h3 {
        font-family: Helvetica, Arial, sans-serif;
      }
      ul {
        text-align: center;
        list-style: none;
        padding: 0;
      }
      li {
        padding: 10px 0;
        border-radius: 10px;
        max-width: 400px;
        margin: 0 auto;
      }
      li:hover {
        border-radius: 10px;
        max-width: 400px;
        margin: 0 auto;
        background: rgb(252, 252, 239);
      }
      button {
        display: block;
        margin: 20px auto;
        border: 1px solid #1a64d6;
        background: #1a64d6;
        color: #fff;
        font-size: 16px;
        line-height: 22px;
        padding: 16px 24px;
        border-radius: 30px;
      }
      button:hover {
        transition: all 200ms ease-in-out;
        box-shadow: rgba(37, 39, 89, 0.08);
        cursor: pointer;
        background: #fff;
        color: #1a64d6;
      }
      p {
        text-align: center;
        font-size: 18px;
        opacity: 0.7;
        font-family: monospace;
      }
    </style>
  </head>
  <body cz-shortcut-listen="true">
    <h1>☀ <br />Currently 52° in Seattle</h1>
    <h2>
      13º /
      <strong> 23º </strong>
    </h2>
    <ul>
      <li>
        <h3>🌧 Tomorrow</h3>
        <p>
          10º /
          <strong>22º</strong>
        </p>
      </li>
      <li>
        <h3>🌤 Saturday</h3>
        <p>15º / <strong>17º</strong></p>
      </li>
      <li>
        <h3>☀ Sunday</h3>
        <p>25º / <strong>28º</strong></p>
      </li>
    </ul>
    <button>Change City</button>
    <p>Coded by Chloe Redstone</p>

    <script>
      function changeCity() {
        let city = prompt("What city do you live in?");
        let temp = prompt("What temperature is it?");

        let h1 = document.querySelector("h1");
        if (temp >= 0) {
          h1.innerHTML = "☀ <br />" + "Currently " + temp + "° in " + city;
        } else {
          h1.innerHTML = "❄ <br />" + "Currently " + temp + "° in " + city;
        }
      }

      let cityChange = document.querySelector("button");

      cityChange.addEventListener("click", changeCity);
    </script>
  </body>
</html>
