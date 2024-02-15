<script>
  export default{
    data() {
      return {
        projects: [ 
          { 
            id: 1,
            title: "Social Posts",
            collaborators: "No",
            description: "Facebook clone",
            image: "./src/assets/img/socialpost.png",
            video: "",
            technologies: "HTML, CSS, JS",
            link_netlify: "https://antonio-dangelo-socialpost.netlify.app",
            link_github: "https://github.com/antoniodangelo11/js-social-posts",
          },
          {
            id: 2,
            title: "Spotify Web",
            collaborators: "No",
            description: "SpotifyWeb clone",
            image: "./src/assets/img/spotifyweb.png",
            video: "",
            technologies: "HTML, CSS",
            link_netlify: "https://antonio-dangelo-spotifyweb.netlify.app",
            link_github: "https://github.com/antoniodangelo11/html-css-spotifyweb.git",
          },
          {
            id: 3,
            title: "Avada Driving",
            collaborators: "No",
            description: "Avada Driving clone",
            image: "./src/assets/img/avadadriving.png",
            video: "",
            technologies: "HTML, CSS",
            link_netlify: "https://antonio-dangelo-avadadriving.netlify.app",
            link_github: "https://github.com/antoniodangelo11/proj-html-vuejs.git",
          },
        ]
      }
    },
  }
</script>

<template>
  <main>
    <div class="container_card m-auto">
      <h1 class="text-center text-red-600 font-bold text-2xl mb-3">My Projects</h1>

      <div class="flex flex-wrap justify-center gap-3">
        <div v-for="project in projects" :key="project.id">

          <div class="max-w-sm h-full w-80 bg-blue-300 border border-gray-200 rounded-lg shadow dark:bg-gray-100 dark:border-gray-700">
            <a href="#">
              <img class="rounded-t-lg h-52 w-96" :src="project.image" alt=""/>
            </a>

            <div class="p-5">
              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ project.title }}</h5>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400"><span class="font-bold">Description: </span>{{ project.description }}</p>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400"><span class="font-bold">Technologies: </span>{{ project.technologies }}</p>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400"><span class="font-bold">Collaborators: </span>{{ project.collaborators }}</p>
              <a :href="project.link_netlify" class="inline-flex items-center px-3 py-2 mr-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                Netlify
              </a>
              <a :href="project.link_github" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                Github
              </a>
            </div>
          </div>

        </div>
      </div>
    </div>
    
  </main>
</template>

<style></style>
