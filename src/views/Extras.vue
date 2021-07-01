<template>
  <div class="extras">
    <h1 style="color: goldenrod;
    background-color: purple;
    margin-left:150px;
    margin-right: 150px">This is an extras page</h1>
  </div>
  <div class="main_content">
    <div class="explanation">
      Yukardaki h1 tag i inline css ile yapıldı, aşağıdakilerde ise farklı yöntemler uygulanacak <br/>
    oluşturduğum external CSS dosyasını main.js içerisinde import ettim.
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio, voluptatum? </p>
    </div>
    <div class="container">
      <div class="grid_item" id="first">
        <h3>Lorem ipsum dolor.</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias blanditiis delectus incidunt placeat quisquam soluta? Animi minima officiis sed sint tempore veritatis! Ab accusantium adipisci autem enim possimus praesentium repellat repellendus. Asperiores, consectetur consequatur dolorem est et labore, maxime molestiae molestias quia quibusdam, rem repudiandae voluptate! Dignissimos dolorem ex obcaecati.</p>
      </div>
      <div class="grid_item" id="second">
        <h3>Lorem ipsum dolor.</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam animi aspernatur at dignissimos, dolore dolores error facilis illo perferendis sint temporibus voluptate. Ad aut commodi consequuntur distinctio dolores eaque eos expedita impedit, in nihil, odio omnis quae repellat? Aliquid fugit incidunt minus modi molestiae natus quibusdam quos reprehenderit, sequi tempora!</p>
      </div>
      <div class="grid_item" id="third">
        <h3>Lorem ipsum dolor.</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus atque blanditiis cumque doloremque doloribus, eius molestiae officia pariatur perspiciatis, quia quibusdam voluptate. Atque doloribus earum ex impedit necessitatibus, officiis omnis. Accusamus aliquid beatae cumque error esse excepturi expedita facilis, inventore, iste iure, minus placeat quae quia vitae voluptatibus? Nesciunt, vel!</p>
      </div>
    </div>
  </div>
</template>
<!--<script>
/*<link rel="stylesheet" href="src/css/style.css"/>*/
import style from "/src/css/style.css"
</script>-->
