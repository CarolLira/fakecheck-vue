<template>
  <div class="home">
    <AppHeader />
    <main>
      <div class="home__form-container">
        <AppDescription />
        <form class="news-form" @submit.prevent="sendNews">
          <AppTextarea v-model="news" text="Cole sua notícia aqui" />
          <AppButton text="Checar" />
          {{ verification }}
        </form>
      </div>
    </main>
  </div>
</template>

<script>
import axios from 'axios';
import AppHeader from "@/components/AppHeader.vue";
import AppDescription from "@/components/AppDescription.vue";
// import AppForm from "@/components/AppForm.vue";
import AppTextarea from "@/components/AppTextarea.vue";
import AppButton from "@/components/AppButton.vue";

export default {
  name: "Home",
  components: {
    AppHeader,
    AppDescription,
    // AppForm,
    AppTextarea,
    AppButton,
  },
  data() {
    return {
      news: "",
      verification: "",
    };
  },
  methods: {
    sendNews() {
      if (this.news) {
        this.news.replace(/["]/g, " ");
        this.news.replace(/[']/g, " ");
        axios.post('http://localhost:5000/', { "texto": this.news})
        .then((response) => {
          if (response.data) {
            this.verification = response.data == 'True' ? 'Verdadeira' : 'Falsa';
          }
        })
      }
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../../styles/index";

main {
  padding: 2.5rem;
}

@media only screen and (min-width: $medium) {
  .home {
    &__form-container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  }
}

.news-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  form {
    width: 100%;
    display: grid;
    grid-template-rows: auto;
    row-gap: 15px;
  }
}

@media only screen and (min-width: $medium) {
  .news-form {
    width: 70%;
  }
}

</style>
