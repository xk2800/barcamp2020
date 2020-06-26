<template>
  <div class="icons">
    <a href="https://www.facebook.com/ITsocietyMMU" target="_blank" class="facebook"><i class="fa fa-facebook"></i>Facebook</a>
    <a href="https://www.instagram.com/itsocietymmu/" target="_blank" class="instagram"><i class="fa fa-instagram"></i>Instagram</a>
  </div>
</template>

<style scoped>
  .icons {
    position: fixed;
    top: 80%;
    right: 0%;
    width: 280px;
    display: flex;
    flex-direction: column;
    z-index: 9999;
  }

  .icons a {
    text-decoration: none;
    text-transform: uppercase;
    padding: 10px;
    font-size: 1.8em;
    font-family: 'Oswald', sans-serif;
    margin: 2px;
    text-align: left;
    border-radius: 50px 0px 0px 50px;
    transform: translate(220px, 0px);
    transition: all 0.5s;
  }

  .icons a:hover {
    transform: translate(0px, 0px);
  }

  .icons a i {
    margin-right: 20px;
    background-color: white;
    height:40px;
    width:40px;
    color:black;
    text-align: center;
    line-height: 40px;
    border-radius:50%;
  }

  .icons a:hover i {
    transform: rotate(-25deg)
  }

  .icons a i.fa-facebook {
    color: #2C80D3;
  }

  .icons a i.fa-instagram {
    color: #C71585;
  }

  .facebook {
    background-color: #2C80D3;
    color:white;
  }

  .instagram {
    background-color: #C71585;
    color:white;
  }
</style>
