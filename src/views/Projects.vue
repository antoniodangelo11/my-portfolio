<script>
  export default{
    data() {
      return {
        projects: [ 
          { 
            id: 1,
            title: "Social Posts",
            collaborators: "No",
            description: "Clone of Facebook",
            image: "./src/assets/img/socialpost.png",
            // image2: "/01SocialPosts2.jpeg",
            // image3: "/01SocialPosts3.jpeg",
            // image4: "/01SocialPosts4.jpeg",
            // image5: "/01SocialPosts5.jpeg",
            video: "",
            technologies: "HTML, CSS, JS",
            link_netlify: "",
            link_github: "https://github.com/antoniodangelo11/js-social-posts",
          }
        ]
      }
    },
  }
</script>

<template>
  <main>
    <h1 class="text-center">MY PROJECT</h1>

    <div class="max-w-sm bg-blue-400 border border-gray-200 rounded-lg shadow dark:bg-gray-100 dark:border-gray-700"
      v-for="project in projects" :key="project.id"
    >
      <a href="#">
        <img class="rounded-t-lg" :src="project.image" alt=""/>
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
  </main>
</template>

<style></style>
