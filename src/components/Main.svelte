<script>
  import Step from './Step.svelte';

  let steps = [
    {name: 'Sneaky Snacker', icon: 'fa-solid fa-cookie-bite'},
    {name: 'My Mixtape', icon: 'fa-solid fa-music'},
    {name: 'Stencil Shaper', icon: 'fa-solid fa-pencil'}
  ]

  let benefits = [
    {name: 'Excellent communicator', description: 'My approach to software engineering is informed by the better part of a decade of experience working within the hospitality sector as a chef. I have developed a skillset that prioritizes intentional communication, accountability, and team work as best practice.'},
    {name: 'Documentation enthusiast', description: 'One of my strong suits has always been writing. When it comes to development, I enjoy being able to document a piece of software\'s use-- identifying patterns, use cases, edge cases, and writing accessible user guides.'},
    {name: 'Empathetic collaborator', description:''},
    {name: 'Driven developer', description:''}
  ]

</script>

<main class='flex flex-col flex-1 p-4'>
  <section id='introPage' class='grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14'>
    <div class='flex flex-col Lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10'>
      <h2 class='font-semibold text-4xl sm:text-5xl md:text-6xl'>
        Hi! I'm <span class='poppins text-violet-400'>Andra</span> Steele<br/>Software
        <span class='poppins text-violet-400'>Engineer</span>
      </h2>
      <p class='text-base sm:text-lg md:text-xl'>
          My <span class='text-violet-400'>favorite tehcnologies and skills</span> include Node.js, React & React Native, API development, writing documentation, Express.js, PostgreSQL and system design.
      </p>
      <a class='blueShadow mx-auto lg:mr-auto text-base s:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-slate text-white-950 cursor-pointer'
      href='https://www.linkedin.com/in/andra-steele/'>
        <div class='absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200'/>
        <h4 class='relative z-9'>Get in touch &rarr;</h4>
      </a>
    </div>
    <div class='relative shadow-2xl grid place-items-center'>
      <!-- <img src={'images/profile.png'} alt="Profile image" class='object-cover z-[2] max-h-[70vh] opacity-2'/> -->
    </div>

  </section>
  <section id='projects' class='py-20 lg:py-32 flex flex-col gap-24'>
    <div class='flex flex-col gap-2 text-center'>
      <h6 class='text-lg sm:text-xl md:text-2xl'>
        A few of my creative endeavors.
      </h6>
      <h3 class='font-semibold text-3xl sm:text-4xl md:text-5xl'>
        Curious to <span class='poppins text-violet-400'>see</span> my work?
      </h3>
    </div>
    <div class='grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10'>
      <Step step={steps[0]}>
        <p>Sneaky snacker is an adventure game telling the story of a girl and her pup as they embark on a journey to acquire the elusive cookie jar. This full-stack game was created with
          <strong class='text-violet-400'>React, Socket.io, Inquirer.js, Material-UI, and OpenAI's ChatGPT API integration.</strong>
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>My Mixtape is a web application that creates personalized Spotify playlists based on a user's current vibe and saves to their Spotify profile. This project was created with
          <strong class='text-violet-400'>React, MongoDB, Auth0's Spotify integration, and the Spotify API's Authorization Code Flow.</strong>
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>Stencil Shaper is a cross-platform mobile application that is designed to help tattoo artists create custom stencils for their clients based on custom dimensions. StencilShaper provides an intuitive and user-friendly interface to customize and export stencils easily. This application was created with
          <strong class='text-violet-400'>React Native & Expo Go.</strong>
        </p>
      </Step>
     
    </div>

  </section>
  <section id='about' class='py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative'>
    <div class='flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4'>
      <h6 class='text-lg sm:text-xl md:text-2xl'>Want to know more?</h6>
      <h3 class='font-semibold text-3xl sm:text-4xl md:text-5xl'>A bit <span class='poppins text-violet-400'>about</span> me.</h3>
    </div>
    <p class='mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl'>I am</p>
    <div class='flex flex-col gap-20 w-full mx-auto max-w-[800px]'>
      {#each benefits as benefit}
      <!-- <div class='flex gap-6 sm:gap-8'> -->
       
      <!-- </div> -->
      {/each}
    </div>
  </section>
</main>