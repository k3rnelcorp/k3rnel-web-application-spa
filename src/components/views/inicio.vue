<template>
  <div class="inicio">
    <div class="h1">
      <Introduction
        title="k3rnel"
        subtitle="'Dedo no cu e tecnologia'"
        description="Originalmente chamado de 3society"
      />
    </div>
    <div class="closureContainer">
      <div class="closure">
        <h3 class="caTitle ca">Encerramento de atividades</h3>
        <h6 class="caSubtitle ca">Pronunciamento Oficial.</h6>
        <p class="pronouncement defaultFont">
          A k3rnel está encerrando suas atividades, o que acontecera no dia 11
          de outubro de 2020. Tivemos uma breve estadia, porem assim como o
          Snapchat e qualquer rede social que a Google tenha criado (ou pelo
          menos tentado), morremos prematuramente.
        </p>
        <p class="defaultFont end italic">- J, Mateus</p>
      </div>
      <div class="containerMM">
        <p class="textMM">
          NUNCA DEIXE ALGUÉM TE DIZER QUE VOCÊ NÃO CONSEGUE, DIGA VOCÊ MESMO:<br />
          "EU NÃO CONSIGO"
        </p>
      </div>
    </div>
    <div class="history">
      <img class="convencao" :src="Convencao" alt="convencao" />
      <div class="textHistoryContainer">
        <h3>PvP's intensos</h3>
        <p class="defaultFont">
          No pubg disputamos quem matará o maldito mexicano primeiro.
        </p>
        <p class="defaultFont">
          Pior que um inimigo do teu lado é o Araújo com uma granada.
        </p>
        <p class="defaultFont">Thiago? Nem mic tem.</p>
        <p class="defaultFont">
          Junin, o famoso busca globo. Só headshot de cualidade.
        </p>
        <p class="defaultFont">
          Maicão no meio da putaria, bala voando, nego morrendo: "Estou com
          Deus".
        </p>
        <p class="defaultFont">"Loot da base? loot da base!"</p>
      </div>
    </div>
    <div class="programmingContainer">
      <div class="programmingTitleContainer">
        <p class="programmingTitle"> Programação</p>
      </div>
      <div class="circleContainer">
        <ProgressCircle subtitle="Habilidade" :progress="20" :stroke="12" :diameter="250" />
        <ProgressCircle subtitle="Gambiarra" :progress="50" :stroke="12" :diameter="250" />
        <ProgressCircle subtitle="Pesquisa" :progress="65" :stroke="12" :diameter="250" />
        <ProgressCircle subtitle="Stack Overflow" :progress="100" :stroke="12" :diameter="250" />
      </div>
    </div>
  </div>
</template>

<script>
import Introduction from "../templates/Introduction";
import ProgressCircle from "../templates/ProgressCircle"
import Convencao from "../../assets/convencao.jpeg";
export default {
  name: "inicio",
  components: {
    Introduction,
    ProgressCircle
  },
  data() {
    return {
      Convencao,
    };
  }
};
</script>

<style>

.h1 {
  margin: 110px 0;
}
.closureContainer {
  display: flex;
}

.containerMM {
  margin-left: 12px;
  margin-right: 150px;
  padding-left: 13px;
  display: flex;
  align-items: center;
  border-left: 1px solid rgba(255, 255, 255, 0.5);
}

.containerMM .textMM {
  font-family: "JetBrainsMono";
  color: rgba(255, 255, 255, 0.6);
  font-weight: 900;
  font-size: 0.9rem;
}

.closure {
  margin-left: 150px;
  display: flex;
  flex-direction: column;
}

.closure .ca {
  color: royalblue;
  font-family: "JetBrainsMono";
}

.closure .caTitle {
  font-size: 1.5rem;
}

.closure .caSubtitle {
  font-size: 0.9rem;
  margin-bottom: 15px;
}

.closure p {
  color: white;
  font-weight: 600;
}

.closure .end {
  align-self: flex-end;
}

.closure .italic {
  font-style: italic;
}

.history {
  margin-top: 100px;
  display: flex;
}

.convencao {
  height: 300px;
}

.textHistoryContainer {
  padding: 15px 20px;
}

.textHistoryContainer h3 {
  color: white;
  font-family: "JetBrainsMono";
  margin-bottom: 10px;
}

.textHistoryContainer p {
  color: white;
  font-weight: 600;
}

.programmingContainer {
  margin: 80px 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.programmingTitleContainer {
  display: flex;
  justify-content: center;
}

.programmingTitleContainer .programmingTitle {
  color: white;
  font-size: 2.5rem;
  font-family: "JetBrainsMono";
  margin: 35px;
}

.circleContainer {
  display: flex;
  justify-content: center;
}

@media (max-width: 1024px) {
  .h1 {
    margin: 70px 0;
  }

  .closure {
    margin-left: 70px;
  }

  .containerMM {
    margin-right: 70px;
  }

  .circleContainer {
    flex-wrap: wrap;
  }
}

@media (max-width: 768px) {

  .closure {
    margin-left: 30px;
  }

  .containerMM {
    margin-right: 20px;
  }

  .convencao {
    max-width: 80%;
    right: auto;
    max-height: calc(100vw * 0.74);
    width: auto;
    height: auto;
  }

  .textHistoryContainer {
    padding: 20px 20px;
  }

  .history {
    margin-top: 100px; 
    flex-direction: column;
    align-items: center;
  }

  .programmingContainer {
    margin: 70px 0;
  }
}

@media (max-width: 576px) {
  .closureContainer {
    flex-direction: column;
  }

  .containerMM {
    margin-right: 12px;
    padding-right: 5px;
    padding-left: 5px;
    padding-top: 15px;
    margin-top: 15px;
    border-top: 1px solid rgba(255, 255, 255, 0.5);
    border-left: none;
  }

  .closure {
    margin-right: 30px;
  }
}

@media (max-width: 320px) {
  .closure {
    margin: 0 10px;
  }
}
</style>