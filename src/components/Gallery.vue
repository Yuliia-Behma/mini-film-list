<script setup>
import OneFilm from "../components/OneFilm.vue";

const films = [
    {
        img: "https://m.media-amazon.com/images/M/MV5BMWY1MGExNTAtNTNjMy00ZTIyLTg1NmQtMTM2MjViNzYwYzgxXkEyXkFqcGdeQXVyMTE5MTg5NDIw._V1_.jpg",
        title: "Breaking Bad",
        genres: "Crime drama",
        description: "A chemistry teacher diagnosed with inoperable lung cancer turns to manufacturing and selling methamphetamine with a former student in order to secure his family's future.",
        rating: 5
    },
    {
        img: "https://m.media-amazon.com/images/M/MV5BNjNhZTk0ZmEtNjJhMi00YzFlLWE1MmEtYzM1M2ZmMGMwMTU4XkEyXkFqcGdeQXVyNjU0OTQ0OTY@._V1_.jpg",
        title: "The Silence of the Lambs",
        genres: "Crime",
        description: "A young F.B.I. cadet must receive the help of an incarcerated and manipulative cannibal killer to help catch another serial killer, a madman who skins his victims.",
        rating: 4
    },
    {
        img: "https://m.media-amazon.com/images/M/MV5BMTUxMzQyNjA5MF5BMl5BanBnXkFtZTYwOTU2NTY3._V1_.jpg",
        title: "The Green Mile",
        genres: "Drama",
        description: "A tale set on death row, where gentle giant John Coffey possesses the mysterious power to heal people's ailments. When the lead guard, Paul Edgecombe, recognizes John's gift, he tries to help stave off the condemned man's execution.",
        rating: 4
    },
    {
        img: "https://m.media-amazon.com/images/M/MV5BZmU0M2Y1OGUtZjIxNi00ZjBkLTg1MjgtOWIyNThiZWIwYjRiXkEyXkFqcGdeQXVyMTQxNzMzNDI@._V1_.jpg",
        title: "Back to the Future",
        genres: "Sci-Fi",
        description: "Marty McFly, a 17-year-old high school student, is accidentally sent 30 years into the past in a time-traveling DeLorean invented by his close friend, the maverick scientist Doc Brown.",
        rating: 5
    },
    {
        img: "https://m.media-amazon.com/images/M/MV5BMjExMTg5OTU0NF5BMl5BanBnXkFtZTcwMjMxMzMzMw@@._V1_.jpg",
        title: "WALL·E",
        genres: "Animation",
        description: "In the distant future, a small waste-collecting robot inadvertently embarks on a space journey that will ultimately decide the fate of mankind.",
        rating: 4
    },
    {
        img: "https://m.media-amazon.com/images/M/MV5BNzQzOTk3OTAtNDQ0Zi00ZTVkLWI0MTEtMDllZjNkYzNjNTc4L2ltYWdlXkEyXkFqcGdeQXVyNjU0OTQ0OTY@._V1_.jpg",
        title: "The Matrix",
        genres: "Sci-Fi",
        description: "When a beautiful stranger leads computer hacker Neo to a forbidding underworld, he discovers the shocking truth--the life he knows is the elaborate deception of an evil cyber-intelligence.",
        rating: 5
    },
]
</script>

<template>
  <div class="main-container">
    <h1>Your best movies gallery</h1>
    <div class="frame" >
      <oneFilm v-for="film in films" :key="film.title" :film></oneFilm>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  max-width: 1200px;
  height: 100%;
  background-color: #a8a8a8;
  border-right: 2px solid #adf449;
  border-left: 2px solid #adf449;
  padding: 30px;
}
.main-container h1 {
  text-align: center;
  font-family: "Jost", sans-serif;
  font-weight: 800;
  font-size: 40px;
  color:#adf449;
  text-shadow: 2px -2px 5px #0000003d,
  -2px -2px 5px #0000003d;
}

.frame {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 15px;
  margin-top: 20px;
}
</style>
