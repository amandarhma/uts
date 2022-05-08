<template xmlns="http://www.w3.org/1999/html">
  <form class="d-flex">
    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
    <button @click="lihat" class="btn btn-outline-success" type="submit">Search </button>

    <section class="surah">
    <div class="judul">
      <h1 v-if="namasurah" class="judul">{{chapters.name_simple}}</h1>
    </div>
    </section>

  </form>
  <div class="about">
    <div class="alert alert-secondary" role="alert">
      <div v-for="chapters in chapters" :key="chapters">
        <a href="#">{{chapters.id}}. {{ chapters.name_complex }} "{{chapters.verses_count}} Ayat" {{ chapters.name_arabic }} </a>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name:"AboutView",
  data(){
    return {
      chapters: null,
    };
  },
  methods: {
    async getListChapter(){
      fetch("https://api.quran.com/api/v4/quran/verses/uthmani?chapter_number=1", {
        method: "GET",
      })
      fetch("https://api.quran.com/api/v4/chapters/1/info?language=id", {
        method: "GET",
      })
      fetch("https://api.quran.com/api/v4/chapters/1?language=id",{
        method: "GET",
      })
      fetch("https://api.quran.com/api/v4/chapters?language=id", {
        method: "GET",
      })
      .then((response) => {
        if (response.ok){
          return response.json();
        }
      })
      .then((json) => {
        this.chapters = json.chapters;
      });
    },
  },
  mounted() {
    this.getListChapter();
  },
};
</script>
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
