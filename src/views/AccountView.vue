<script>
export default {
  data() {
    return {
      contas: [
        {
          id: 1,
          elo: 'Ouro',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 2,
          elo: 'Platina',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 3,
          elo: 'Desafiante',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 4,
          elo: 'Prata',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 5,
          elo: 'Ouro',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 6,
          elo: 'Mestre',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 7,
          elo: 'Grandmaster',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 8,
          elo: 'Diamante',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 9,
          elo: 'Diamante',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 10,
          elo: 'Diamante',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 11,
          elo: 'Diamante',
          level: 30,
          champions: 47,
          essence: 3569
        },
        {
          id: 12,
          elo: 'Diamante',
          level: 30,
          champions: 47,
          essence: 3569
        }
      ]
    }
  }
}
</script>
<template>
  <main id="main">
    <div class="title-block">
      <h1>Contas de League of Legends</h1>
    </div>
    <div id="content">
      <div id="account-container">
        <div class="card" v-for="conta in contas" :key="conta.id">
          <h1 class="account-elo">{{ conta.elo }}</h1>
          <img
            class="account-image"
            src="https://support-leagueoflegends.riotgames.com/hc/article_attachments/4415894930323/Challenger_Emblem_2022.png"
            alt=""
          />
          <p class="account-level">Level {{ conta.level }}</p>
          <p class="account-info">{{ conta.essence }} EA | {{ conta.champions }} Campe??es</p>
          <span class="account-look">Skins</span>
        </div>
      </div>
      <div id="navigation">
        <ul class="navigation-buttons">
          <li class="navigation-button">??? P??gina anterior</li>
          <li class="navigation-button">Pr??xima p??gina ???</li>
        </ul>
      </div>
    </div>
  </main>
</template>

<style scoped>
#main {
  display: flex;
  flex-direction: column;
  /* background-image: url(../assets/background.jpg); */
}
#main::before {
  content: '';
  background-image: url(../assets/rivenbg.jpg);
  background-size: cover;
  filter: opacity(30%);
  background-position: center;
  position: absolute;
  height: 100%;
  width: 100%;
}
.title-block {
  height: 35vh;

  display: flex;
  align-items: center;
  justify-content: center;
  padding-top: 2vh;
  padding-inline: 10vw;

  text-shadow: 0px 0px 15px black;
  font-size: 2rem;
  color: rgb(214, 214, 214);
  text-align: center;

  /* border-bottom: 1px solid #83b5ff; */
}
@media (max-width: 1065px) {
  .title-block {
    font-size: 1.3rem;
  }
}
@media (max-width: 450px) {
  .title-block {
    font-size: 1rem;
  }
}
#content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-bottom: 2vh;
}
#account-container {
  border-radius: 30px;
  padding: 6vh 5vh;
  margin-inline: 4vw;
  height: fit-content;

  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(3, 1fr);
  justify-items: center;
  row-gap: 30px;

  /* border: 2px solid rgb(0, 0, 0); */
  background-color: rgba(0, 0, 0, 0.3);
}
@media (max-width: 1200px) {
  #account-container {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media (max-width: 950px) {
  #account-container {
    grid-template-columns: repeat(2, 1fr);
    column-gap: 0px;
    padding-inline: 6vw;
  }
}
@media (max-width: 680px) {
  #account-container > .card {
    width: 220px;
  }
}
@media (max-width: 680px) {
  #account-container > .card {
    width: 220px;
  }
}
@media (max-width: 500px) {
  #account-container > .card {
    width: 150px;
    height: 250px;
  }
  .account-elo {
    font-size: 1.3rem;
  }
  .account-look {
    font-size: 8px;
  }
}
.card {
  height: 350px;
  width: 250px;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;

  border: 2px solid #c869ff;
  border-radius: 30px;
  background-color: rgba(0, 0, 0, 0.8);
  filter: opacity(100%);
}
.account-image {
  height: 15vh;
}
.account-elo {
  color: #b983ff;
  border-bottom: 1px solid;
  font-weight: bolder;
  cursor: default;
}
.account-elo {
  color: #83b5ff;
  cursor: default;
}
.account-level {
  color: #ffde83;
  cursor: default;
}
.account-info {
  color: #83b5ff;
  cursor: default;
  text-align: center;
}
.account-look {
  background-color: rgba(0, 0, 0, 0.8);
  border: 1px groove #b983ff;
  color: white;
  width: 60%;
  text-align: center;
  font-size: 1rem;
  border-radius: 8px;
  font-style: italic;
  cursor: pointer;
}
.account-look:hover {
  background-color: rgba(140, 0, 255, 0.1);
}
#navigation {
  display: flex;
  justify-content: center;
  grid-area: 4 / 2 / 4 / 4;
  margin-top: 2vh;
}
.navigation-buttons {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 2vw;
}
.navigation-button {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
  padding: 6px 15px;

  background-color: rgb(0, 0, 0);
  border: 2px groove #b983ff;
  font-weight: bolder;
  color: #b983ff;
  font-size: 1rem;

  cursor: pointer;
}
.navigation-button:hover {
  color: rgb(189, 189, 189);
}
</style>
