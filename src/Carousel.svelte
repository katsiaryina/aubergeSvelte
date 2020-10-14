<script>
  const next = () => {
    const img = document.querySelector(".slider-img");
    img.src = "http://localhost:5000/img/bowl.jpg";
  };
</script>

<style>
  section {
    width: 100%;
    height: 700px;
    position: relative;
  }
  img {
    width: 100%;
    height: 100%;
  }
  button {
    padding: 10px;
    background-color: red;
    position: absolute;
    top: 20px;
  }
</style>

<section>
  <img class="slider-img" src="./img/book.jpg" alt="" />
  <button on:click={next}>next</button>
</section>
