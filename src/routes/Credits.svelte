<script>
  import ls from './ls.svg';
</script>

<footer>
  <p>Hosted with &lt;3 by the <a target="_blank" href="https://linuxunsw.org/">UNSW Linux Society</a></p>
  <img class="logo" src={ls} alt="">
</footer>

<style>
  footer {
    color: white;
    text-align: center;
    padding: 50px;
    padding-bottom: 0px;
    overflow-y: hidden;
    display: flex;
    flex-direction: column;
  }
  a {
    color: white;
    text-decoration: underline dotted;
  }
  a:hover {
    text-decoration: underline;
  }

  .logo {
    position: relative;
    width: 100px;
    top: 25px
  }
</style>
