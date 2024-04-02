<template>

  <header>
    <ul>
      <li class="home"><a href="#"><img src="@/assets/images/accueil.png" alt="logoHome"></a></li>
      <li><a href="./lien_page/404.html"><img src="@/assets/images/cv.png" alt="logoCV"></a></li>
      <li><a href="./lien_page/404.html"><img src="@/assets/images/formulaire-de-contact.png" alt="logoFormulaire"></a></li>
    </ul>
  </header>

  <main>
    <section>

      <h1>HUGO Leplingard</h1>
      <h3>porte-folio</h3>
      <p>Étudiant en développement Front-end au CEF, je m'appelle Hugo, je fais 1m84.</p>

    </section>

    <article>

      <figure>
        <h2>Curiculum Vitae</h2>

        <div class="container">
          <img src="./assets/images/CVfond.png" alt="CVfond" class="fond-image">

          <div class="middle">
            <img src="./assets/images/cv.png" alt="logoCV">
          </div>
        </div>
      </figure>

      <figure>
        <h2>Formulaire</h2>

        <div class="container">
          <img src="./assets/images/formulaireFond.png" alt="formulaireFond"  class="fond-image">

          <div class="middle">
            <img src="./assets/images/formulaire-de-contact.png" alt="logoFormulaire">
          </div>
        </div>
      </figure>

    </article>
  </main>

  <contenu></contenu>

  <aside>
    <form class="containerEnvoie" action="#">
      <input type="text" id="Name" placeholder="Nom/Prénom" required><br>
      <input type="text" id="Subject" placeholder="Objet" required><br>
      <textarea id="Message" placeholder="Votre message" autocomplete="off" rows="10" cols="10" required></textarea><br>

      <button type="submit">Envoyer</button>
    </form>
  </aside>

  <footer>

    <div>
      <a href="https://fr.linkedin.com/in/hugo-leplingard-924793262"><img src="@/assets/images/linkedin.png" alt="linkedin"></a>
      <a href="./lien_page/twi.html"><img src="@/assets/images/twitter.png" alt="twitter"></a>
      <a href="https://github.com/Huglecrack/Projet_-val-4_vue02.git"><img src="@/assets/images/github.png" alt="github"></a>
    </div>

    <p>Dernière mise à jour le 20 mars 2024</p>

  </footer>
</template>



<script setup>
  import Contenu from './components/contenu.vue';

  function EnvoieEmail(e) {
    e.preventdefault();

    const Name = document.getElementById('Name').value;
    const Subject = document.getElementById('Subject').value;
    const  Message = document.getElementById('Message').value;

    Email.send({
      Host : "smtp.elasticemail.com",
      Username : "hleplingard04@gmail.com",
      Password : "C318A590E2D14B0C0EBBD4B8BF3AF5F52EC2",
      To : 'hleplingard04@gmail.com',
      From : Name,
      Subject : Subject,
      Body : Message
    }).then(
      message => alert(message)
    );
    return alert('message bien envoyé');
  }
</script>



<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@400&family=Raleway:wght@400&display=swap');

  header {
    width: 100%;
    top: 0;
    left: 0;
    background-color:#2d2d2d;
    position: fixed;
    z-index: 1;
  }

  header ul {
    display: flex;
    height: 100%;
    width: 100%;
    float: left;
    padding: 0;
    margin: 0;
    transition: all 0.4s ease;
    text-align: center;
    justify-content: space-evenly;
    flex-direction: row;
  }

  header ul li{
    width: 33.33%;
    padding: 20px;
    list-style-type: none;
  }

  header ul li img {
    width: 50px;
    height: 50px;
  }

  header ul .home {
    background-color: #3024b0;
  }

  header ul li:hover {
    background-color: #080808;
  }

  header a.home img:hover {
    background-color: #080808;
  }

  main {
    margin-top: 150px;
  } 

  main section {
    margin-left: 80px;
  }

  main article {
    display: flex;
    justify-content: center;
  }

  main article h2 {
    margin: 30px 160px;
  }

  .container {
    width: 70%;
    height: 90%;
    position: relative;
    background-color: #080808;
  }
    
  .fond-image {
    opacity: 1;
    display: block;
    width: 100%;
    height: auto;
    transition: .5s ease;
    backface-visibility: hidden;
  }

  .container:hover .fond-image {
    opacity: 0.3;
  }

  .middle {
    transition: .5s ease;
    opacity: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    -ms-transform: translate(-50%, -50%);
  }

  .container:hover .middle {
    opacity: 1;
  }

  .middle img {
    width: 90px;
    height: 90px;
  }

  .middle:hover {
    cursor: zoom-in;
  }

  .container:active .fond-image {
    opacity: 1;
    z-index: 1;
    transform:scale(1.5);
  }

  .container:active .middle {
    opacity: 0;
  }

  aside {
    display: flex;
    justify-content: center;
  }

  aside form {
    margin-top: 130px;
    background-color: #2d2d2d;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px #2d2d2d;
  }

  aside form input, textarea {
    display: block;
    width: 500px;
    padding: 8px;
    margin-bottom: 16px;
    box-sizing: border-box;
    border: solid 2px #080808;
    border-radius: 1%;
  }

  aside form button {
    background-color: #3024b0;
    color: #b7b7ce; 
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  footer {
    margin-top: 30px;
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  footer div {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  footer div a img {
    display: flex;
    margin: 15px 30px 5px;
    height: 70px;
    width: 70px;
  }

  footer div a img:hover {
    cursor: pointer;
    opacity: 75%;
  }

  footer p {
    font-size: 15px;
  }
</style>
