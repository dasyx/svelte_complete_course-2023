<script>
    let name = 'Bob';
    let favoriteColor = 'red';
    let favoriteNumber = 42;
    let fontSize = 20;
    setTimeout(() => {
      name = 'John';
      favoriteColor = 'blue';
      fontSize = 40;
    }, 1000);
  </script>
  
  <h2>You rock and roll !!!</h2>
  <p style="color: {favoriteColor};">{name}</p>
  <p style="font-size: {fontSize}px;">This is a paragraph</p>
  <p>{favoriteNumber}</p>