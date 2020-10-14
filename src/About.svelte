<script>
  if (window.height == 600) {
    console.log("hello");
    // div.style.background = red;
  }
</script>

<style>
  div {
    background-image: url("./img/book.jpg");
    background-position: center center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 800px;
    padding: 100px;
  }
  span {
    position: relative;
  }

  span:after {
    position: absolute;
    content: "";
    display: block;
    bottom: 0;
    left: 0;
    line-height: 1;
    height: 7px;
    width: 100%;
    background-color: #1d2cf0;
    transform-origin: left bottom;
    transform: scaleX(1);
    transition: transform 0.4s linear;
  }

  span:hover:after {
    transform: scaleX(0);
    transform-origin: right bottom;
    transition: transform 0.4s linear;
  }
</style>

<div>
  <h2>
    <span>Lorem ipsum</span>
    dolor sit, amet consectetur adipisicing elit. Aliquid corporis quis
    architecto corrupti vero suscipit fugiat amet ea tempora qui?
  </h2>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti reiciendis
    accusantium commodi maxime consequuntur, maiores velit, sapiente doloribus
    temporibus reprehenderit officia! Ex doloribus maiores suscipit veniam
    laboriosam molestias officiis magni! Sint libero molestiae laboriosam,
    suscipit voluptas praesentium nesciunt iste perspiciatis.
  </p>
</div>
