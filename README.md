# CODSOFT
Intership Projects for Codsoft
<!DOCTYPE html>
<html lang=""en>
<head>
 <meta charset="UTF-8">
 <meta name="viewport content="width=device-width, initial-scale="1.0">
 <title>calculator</title>
  <style>
 body {
    display: flex;
    justify-content: center;
    align-items: center;
    height:100vh;
    margin: 0;
    background-color: #f0f0f0;
    font-family: 'Courier New', Courier, monospace;
 }
  .container {
    height: auto;
    width: 300px;
    border: 5px soild red;
    border-radius: 10px;
    padding: 10px;
    background-color: white;
  }
  #text { width: 100%;
    height: 50px;
    font-size: 24px;
    text-align: right;
    padding: 10px;
    box-sizing: border-box;
    border: 2px solid #ccc;
    border-radius: 5px;

  }
    .button {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 10px;}
    .button button {
        padding: 20px;
        font-size: 18px;
        border: none;
        border-radius: 5px;
        background-color: #007bff;
        color: white;
        cursor: pointer;
    }
    .button button:hover {
        background-color: #0056b3;
    }
    .equal {
        grid-column: span 2;
        background-color: #50cd6d;
        color: white;
    }

  </style>


</head>
<body>
<div class="container">
 <input type="text" id="text" disabled>
 <div class="button">
    <button onclick="cc()">CE</button>
    <button onclick="displayadd('+')">+</button>
    <button onclick="ex">X</button>
    <button onclick="displayadd('%')">%</button>

    <button onclick="displayadd('9')">9</button>
     <button onclick="displayadd('8')">8</button>
      <button onclick="displayadd('7')">7</button>
       <button onclick="displayadd('/')">/</button>

        <button onclick="displayadd('6')">6</button>
         <button onclick="displayadd('5')">5</button>
          <button onclick="displayadd('4')">4</button>
           <button onclick="displayadd('*')">*</button>

            <button onclick="displayadd('3')">3</button>
             <button onclick="displayadd('2')">2</button>
              <button onclick="displayadd('1')">1</button>
               <button onclick="displayadd('-')">-</button>

                <button onclick="displayadd('0')">0</button>
                 <button onclick="displayadd('.')">.</button>
                  <button class="equal" onclick="calculate()">=</button>

 </div>   
</div>

</body>
<script>
function displayadd(input)
{ var dis=document.getElementById("text");
    dis.value += input;
}
function calculate() {
    var dis = document.getElementById("text");
    dis.value = eval(dis.value);
}
function cc() {
     document.getElementById("text").value = "";
} 
</script>
</html>
