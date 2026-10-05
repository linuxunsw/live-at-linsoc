<script>
  import { asset } from '$app/paths';
  const pengwing = asset('/pengwing.png');
</script>
<footer>
  <p>Hosted with &lt;3 by the <a target="_blank" href="https://linuxunsw.org/"><i class="las la-link"></i>UNSW Linux Society</a></p>
  <img class="logo" src={pengwing} alt="">
</footer>

<style>
  footer {
    color: white;
    text-align: center;
    padding: 50px;
    padding-bottom: 0px;
    overflow-y: hidden;
    display: flex;
    /*flex-direction: column;*/
    justify-content: right;
  }
  a {
    color: white;
    text-decoration: underline dotted;
  }
  a:hover {
    text-decoration: underline;
  }

  .logo {
    image-rendering: pixelated;
    width: 100px;
    transform: translate(0, 10px);
    transition: all 0.1s;
  }

  footer:hover .logo {
    transform: none;
  }
</style>
