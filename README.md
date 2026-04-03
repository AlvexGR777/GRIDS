GRID CSS e HTML

CSS

* {
    margin: 0;
    padding: 0;
box-sizing: border-box;
font-family: Arial, Helvetica, sans-serif;
}

body {
 background: color #f0f0f0;; 
 padding: 20px;  
}

.container {
display: grid;
height: 90vh;/*espaço de tela que vai ocupar*/
gap:10px;/*espaço entre os blocos*/


grid-template-columns:  1fr 2fr 1fr;

grid-template-rows: 80px 1fr 1fr 80px;

grid-template-areas: 
"header header header"
"menu main ad1"
"ad2 main ad1"
"footer footer footer";

}
 header, nav, main, aside, footer  {
  background-color: #4a90e2;
  border: 4px solid #e74c3c;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 1.2rem;
 }

 header { grid-area: header;}
 nav {grid-area: menu ;}
 main {grid-area: main; }
.ad1 {grid-area: ad1 ;}
.ad2 {grid-area: ad2; }
footer { grid-area: footer;}


HTML

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>GRID 3</title>
</head>


<body>
    
<div class="container">

    <header>header</header>
 
    <nav>menu</nav>

    <main>main</main>

    <aside class="ad1">Ad1</aside>

    <aside class="ad2">Ad2</aside>

    <footer>footer</footer>

</div>

</body>
</html>
