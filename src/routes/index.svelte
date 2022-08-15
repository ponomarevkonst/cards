    <div class="wrapper">
      <ul class="cards">
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-6.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-3.png" alt="card-img">
          </div>
        </li>
        <li class="card flip">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-4.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-1.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-2.png" alt="card-img">
          </div>
        </li>
        <li class="card flip">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-4.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-7.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-5.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-8.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-3.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-1.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-2.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-8.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-7.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-6.png" alt="card-img">
          </div>
        </li>
        <li class="card">
          <div class="view front-view">
            <img src="images/que_icon.png" alt="icon">
          </div>
          <div class="view back-view">
            <img src="images/img-5.png" alt="card-img">
          </div>
        </li>
      </ul>
    </div>
    
    
    <style>
    /* Import Google Font - Poppins */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
body{
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: white;
}
.wrapper{
  padding: 25px;
  border-radius: 10px;
  background: #f0f0f0;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}
.cards, .card, .view{
  display: flex;
  align-items: center;
  justify-content: center;
}
.cards{
  height: 400px;
  width: 400px;
  flex-wrap: wrap;
  justify-content: space-between;
}
.cards .card{
  cursor: pointer;
  list-style: none;
  user-select: none;
  position: relative;
  perspective: 1000px;
  transform-style: preserve-3d;
  height: calc(100% / 4 - 10px);
  width: calc(100% / 4 - 10px);
}
.card.shake{
  animation: shake 0.35s ease-in-out;
}
@keyframes shake {
  0%, 100%{
    transform: translateX(0);
  }
  20%{
    transform: translateX(-13px);
  }
  40%{
    transform: translateX(13px);
  }
  60%{
    transform: translateX(-8px);
  }
  80%{
    transform: translateX(8px);
  }
}
.card .view{
  width: 100%;
  height: 100%;
  position: absolute;
  border-radius: 7px;
  background: #fff;
  pointer-events: none;
  backface-visibility: hidden;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
  transition: transform 0.25s linear;
}
.card .front-view img{
  width: 45px;
}
.card .back-view img{
  max-width: 45px;
}
.card .back-view{
  transform: rotateY(-180deg);
}
.card.flip .back-view{
  transform: rotateY(0);
}
.card.flip .front-view{
  transform: rotateY(180deg);
}
@media screen and (max-width: 500px) {
  .cards{
    height: 350px;
    width: 350px;
  }
  .card .front-view img{
    width: 40px;
  }
  .card .back-view img{
    max-width: 40px;
  }
}
@media screen and (max-width: 530px) {
  .cards{
    height: 300px;
    width: 300px;
  }
  .card .front-view img{
    width: 35px;
  }
  .card .back-view img{
    max-width: 35px;
  }
}
    </style>