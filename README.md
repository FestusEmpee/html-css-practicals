<!DOCTYPE html>
<html>
    <head>
      <title>
        Rock Paper Scissors
      </title>
      <h1>
        Rock Paper Scissors
      </h1>
      <style>
        .Rock{
            cursor: pointer;
            margin-top: 10px;
            margin-bottom: 10px;
            margin-right: 10px;
            margin-bottom: 10px;
            color: rgb(14, 218, 35);
            border-width: 10px;
            border-radius: 10px;
        }
        .Paper{
            cursor: pointer;
            margin-top: 10px;
            margin-bottom: 10px;
            margin-right: 10px;
            margin-bottom: 10px;
            color: rgb(14, 218, 35);
            border-width: 10px;
            border-radius: 10px;
        }
        .Scissors{
            cursor: pointer;
            margin-top: 10px;
            margin-bottom: 10px;
            margin-right: 10px;
            margin-bottom: 10px;
            color: rgb(14, 218, 35);
            border-width: 10px;
            border-radius: 10px;
        }
        .body{
            background-color: rgb(122, 173, 75);
        }
      </style>
    </head>
    <body class="body">
       <br><br>
         <!-- 🧮 Score Display -->
    <p id="score">Wins: 0 | Losses: 0 | Ties: 0</p>

       <button class="Rock" onclick="
       const randomNumber=Math.random();
        let ComputerMove=''
        if ( randomNumber >= 0 && randomNumber < 1/3) {ComputerMove = 'Rock';}
        else if (randomNumber >= 1/3 && randomNumber < 2/3) {ComputerMove = 'Paper';}
        else if (randomNumber >= 2/3 && randomNumber < 1) {ComputerMove = 'Scissors';}

        let result = '';
        if (ComputerMove === 'Rock') {result = 'Tie';}
        else if (ComputerMove === 'Paper') {result = 'You lose';}
        else if (ComputerMove === 'Scissors') {result = 'You win!';}

        alert(`You picked Rock. Computer chose ${ComputerMove}. ${result}`)

              if (result === 'You win!') wins++;
            else if (result === 'You lose') losses++;
           else ties++;
           updateScore();

        ">Rock</button>

       <button class="Paper" onclick="
       const randomNumber=Math.random();
       let ComputerMovae=''
       if (randomNumber >=0 && randomNumber<=1/3) {ComputerMove = 'Rock';}
       else if (randomNumber >=1/3 && randomNumber <=2/3){ComputerMove = 'Paper';}
       else if (randomNumber >=2/3 && randomNumber <=1){ComputerMove = 'Scissors';}

       let result=''
       if (ComputerMove === 'Paper') {result = 'Tie';}
       else if (ComputerMove === 'Rock') { result ='You win';}
       else if (ComputerMove === 'Scissors') { result = 'You lose';}

       alert(`You picked paper.Computer picked ${ComputerMove}.${result}`);

       if (result === 'You win') wins++;
      else if (result === 'You lose') losses++;
      else ties++;
      updateScore();
       ">Paper</button>

       <button class="Scissors" onclick="
       const randomNumber=Math.random();
       let ComputerMove=''
       if( randomNumber >=0 && randomNumber<=1/3){ComputerMove = 'Rock';}
       else if( randomNumber >=1/3 && randomNumber < 2/3){ComputerMove = 'Paper';}
       else if ( randomNumber >= 2/3 && randomNumber <=1){ComputerMove = 'Scissors';}

       let result=''
       if (ComputerMove === 'Scissors'){result='Tie';}
       else if (ComputerMove == 'Paper'){result = 'You win';}
       else if (ComputerMove === 'Rock'){result = 'You lose';}

       alert(`You picked Scissors.Computer picked ${ComputerMove}.${result}`);

       if (result === 'You win') wins++;
      else if (result === 'You lose') losses++;
      else ties++;
      updateScore();
     ">Scissors</button> 

      <!-- 🧠 Score Logic -->
    <script>
      let wins = 0;
      let losses = 0;
      let ties = 0;

      function updateScore() {
        document.getElementById('score').innerText = `Wins: ${wins} | Losses: ${losses} | Ties: ${ties}`;
      }
    </script>
    </body>
</html>
