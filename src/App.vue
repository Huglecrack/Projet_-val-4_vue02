<template>

  <header>
    <ul>
      <li class="home"><a href="#"><img src="@/assets/images/accueil.png" alt="logoHome"></a></li>
      <li><a href="./liensPages/indexquatrecentsquatre.html" class="headerCV"><img src="@/assets/images/cv.png" alt="logoCV"></a></li>
      <li><a href="./liensPages/stylequatrecentsquatre.html" class="headerFDC"><img src="@/assets/images/formulaire-de-contact.png" alt="logoFormulaire"></a></li>
    </ul>
  </header>

  <main>
    <section>
      <h1>HUGO Leplingard</h1>
      <h3>portfolio</h3>
      <p>Étudiant en développement Front-end au CEF, je m'appelle Hugo, je fais 1m84.</p>
    </section>

    <article>
      <div class="slider-wrapper">
        <button id="prev-slide" class="slide-button material-symbols-rounded"><</button>

        <ul class="image-list">
          <li>
            <h2>Curiculum Vitae</h2>

            <div class="containerCont01">
              <img src="@/assets/images/CVfond.png" alt="CVfond" class="fondImage01">

              <div class="middleCont01">
                  <img src="@/assets/images/cv.png" alt="logoCV" id="modale1">
              </div>
            </div>
          </li>

          <li>
            <h2>Formulaire</h2>

            <div class="containerCont02">
                <img src="@/assets/images/formulaireFond.png" alt="formulaireFond" class="fondImage02">

                <div class="middleCont02">
                    <img src="@/assets/images/formulaire-de-contact.png" alt="logoFormulaire" id="modale2">
                </div>
            </div>
          </li>
        </ul>

        <button id="next-slide" class="slide-button material-symbols-rounded">></button>
      </div>
      <div class="slider-scrollbar">
        <div class="scrollbar-track">
          <div class="scrollbar-thumb"></div>
        </div>
      </div>
    </article>
  </main>

  <div id="modale3">
    <button>Appuyez pour ouvrir la Modale</button>
  </div>

  <aside>
    <form class="containerEnvoie" action="#">
      <input type="text" id="Name" placeholder="Nom/Prénom" required><br>
      <input type="text" id="Subject" placeholder="Objet" required><br>
      <textarea id="Message" placeholder="Votre message" autocomplete="off" rows="10" cols="10" required></textarea><br>

      <button id="submit">Envoyer</button>
    </form>
  </aside>

  <div class="cube"></div>

  <footer>

    <div>
      <a href="https://fr.linkedin.com/in/hugo-leplingard-924793262"><img src="@/assets/images/linkedin.png" alt="linkedin"></a>
      <a href="./liensPages/twi.html"><img src="@/assets/images/twitter.png" alt="twitter"></a>
      <a href="https://github.com/Huglecrack/Projet_-val-4_vue02.git"><img src="@/assets/images/github.png" alt="github"></a>
    </div>

    <p>Dernière mise à jour le 20 avril 2024</p>

  </footer>
</template>


<script setup>

  const initSlider = () => {
    const imageList = document.querySelector(".slider-wrapper .image-list");
    const slideButtons = document.querySelectorAll(".slider-wrapper .slide-button");
    const sliderScrollbar = document.querySelector("figure .slider-scrollbar");
    const scrollbarThumb = sliderScrollbar.querySelector(".scrollbar-thumb");
    const maxScrollLeft = imageList.scrollWidth - imageList.clientWidth;

    scrollbarThumb.addEventListener("mousedown", (e) => {
      const startX = e.clientX;
      const thumbPosition = scrollbarThumb.offsetLeft;
      const maxThumbPosition = sliderScrollbar.getBoundingClientRect().width - scrollbarThumb.offsetWidth;

      const handleMouseMove = (e) => {
        const deltaX = e.clientX - startX;
        const newThumbPosition = thumbPosition + deltaX;

        const boundedPosition = Math.max(0, Math.min(maxThumbPosition, newThumbPosition));
        const scrollPosition = (boundedPosition / maxThumbPosition) * maxScrollLeft;
                
        scrollbarThumb.style.left = `${boundedPosition}px`;
        imageList.scrollLeft = scrollPosition;
      }

      const handleMouseUp = () => {
        document.removeEventListener("mousemove", handleMouseMove);
        document.removeEventListener("mouseup", handleMouseUp);
      }

      document.addEventListener("mousemove", handleMouseMove);
      document.addEventListener("mouseup", handleMouseUp);
    });

    slideButtons.forEach(button => {
      button.addEventListener("click", () => {
        const direction = button.id === "prev-slide" ? -1 : 1;
        const scrollAmount = imageList.clientWidth * direction;
        imageList.scrollBy({ left: scrollAmount, behavior: "smooth" });
      });
    });

    const handleSlideButtons = () => {
      slideButtons[0].style.display = imageList.scrollLeft <= 0 ? "none" : "flex";
      slideButtons[1].style.display = imageList.scrollLeft >= maxScrollLeft ? "none" : "flex";
    }

    const updateScrollThumbPosition = () => {
      const scrollPosition = imageList.scrollLeft;
      const thumbPosition = (scrollPosition / maxScrollLeft) * (sliderScrollbar.clientWidth - scrollbarThumb.offsetWidth);
      scrollbarThumb.style.left = `${thumbPosition}px`;
    }

    imageList.addEventListener("scroll", () => {
      updateScrollThumbPosition();
      handleSlideButtons();
    });
  }

  window.addEventListener("resize", initSlider);
  window.addEventListener("load", initSlider);

  const envoieMail = document.getElementById('submit');
  if (envoieMail == onclick) {
    alert('votre message à bien été envoyé');
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

main article {
  margin: 0 15%;
  display: flex;
  border-radius: 8px;
  background-color: #2d2d2d;
  box-shadow: 0 0 10px #2d2d2d;
  flex-direction: column;
  align-items: center;
}

figure {
  margin-top: 100px;
}

figure h2 {
  padding-left: 150px;
}

.containerCont01 {
  margin-top: 10px;
  width: 400px;
  height: 500px;
  background-color: #080808;
}

.fondImage01 {
  width: 100%;
  height: 100%;
}

.containerCont01:hover .fondImage01 {
  transition: 1s ease;
  opacity: 0.3;
}

.containerCont01:hover .middleCont01 {
  opacity: 1;
  transition: 1s ease;
}

.containerCont01:hover + .headerCV {
  background-color: #080808;
}

.containerCont01:hover + .headerCV {
  background-color: #080808;
}

.containerCont01:hover + .cube {
  opacity: 1;
}

.middleCont01 {
  opacity: 0;
}

.middleCont01 img {
  position: absolute;
  top: 50%;
  left: 19%;
  width: 80px;
  height: 80px;
}

.middleCont01:hover {
   cursor: zoom-in;
}

.containerCont02 {
  margin-top: 10px;
  width: 400px;
  height: 500px;
  background-color: #080808;
}

.fondImage02 {
  width: 100%;
  height: 100%;
}

.containerCont02:hover .fondImage02 {
  transition: 1s ease;
  opacity: 0.3;
}

.containerCont02:hover .middleCont02 {
  opacity: 1;
  transition: 1s ease;
}

.containerCont02:hover + .headerFDC {
  background-color: #080808;
}

.containerCont02:hover + .headerFDC {
  background-color: #080808;
}

.containerCont02:hover + .cube {
  opacity: 1;
}

.middleCont02 {
  opacity: 0;
}

.middleCont02 img {
  position: absolute;
  top: 50%;
  left: 54%;
  width: 80px;
  height: 80px;
}

.middleCont02:hover {
  cursor: zoom-in;
}
 
.modale3{
  right: 0;
  left: 0;
  margin-top: 150px;
  display: flex;
  justify-content: center;
}

.modale3 button {
  font-family: 'Lato', sans-serif;
  background-color: #3024b0;
  color: #b7b7ce;
  font-size: 15px;
  padding: 15px 25px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.slider-wrapper {
  position: relative;
}

.slide-button {
  position: absolute;
  top: 50%;
  outline: none;
  border: none;
  height: 50px;
  width: 50px;
  z-index: 5;
  color: #fff;
  display: flex;
  cursor: pointer;
  font-size: 2.2rem;
  background: #000;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  transform: translateY(-50%);
}

.slide-button:hover {
  background: #404040;
}

.slide-button#prev-slide {
  left: -25px;
}

.slide-button#next-slide {
  right: -25px;
}

.image-list {
  display: grid;
  grid-template-columns: repeat(10, 1fr);
  gap: 18px;
  font-size: 0;
  list-style: none;
  margin-bottom: 30px;
  overflow-x: auto;
  scrollbar-width: none;
}

.image-list::-webkit-scrollbar {
  display: none;
}

.image-item {
  width: 325px;
  height: 400px;
  object-fit: cover;
}

.slider-scrollbar {
  height: 24px;
  width: 100%;
  display: flex;
  align-items: center;
}

.scrollbar-track {
  background: #ccc;
  width: 100%;
  height: 2px;
  display: flex;
  align-items: center;
  border-radius: 4px;
  position: relative;
}

.slider-scrollbar:hover .scrollbar-track {
  height: 4px;
}

.scrollbar-thumb {
  position: absolute;
  background: #000;
  top: 0;
  bottom: 0;
  width: 50%;
  height: 100%;
  cursor: grab;
  border-radius: inherit;
}

.scrollbar-thumb:active {
  cursor: grabbing;
  height: 8px;
  top: -2px;
}

.scrollbar-thumb::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  top: -10px;
  bottom: -10px;
}

@media only screen and (max-width: 1023px) {
  .slide-button {
    display: none !important;
  }

  .image-list {
    gap: 10px;
    margin-bottom: 15px;
    scroll-snap-type: x mandatory;
  }

  .image-item {
    width: 280px;
    height: 380px;
  }

  .scrollbar-thumb {
    width: 20%;
  }
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

.cube {
  opacity: 0;
  width: 70px;
  height: 70px;
  bottom: 0;
  right: 0;
  position: fixed;
  background-color: rgb(0, 0, 0);
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
