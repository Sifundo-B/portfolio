<script>
    import HeadingText from "./HeadingText.svelte";
    import ProjectCard from "./ProjectCard.svelte";
  
    let values = [
      {
        src: "/dating-smartphone-man.svg",
        alt: "Smarphone man icon",
        title: 'Full Stack Development',
        description: `Most developers are only able to do frontend or backend. I can do both, saving you the trouble of finding multiple devs for your project`,
      },
      {
        src: "/laptop-smiley-1.svg",
        alt: "Laptop smiley icon",
        title: 'All types of software',
        description: `I've worked on many different projects. From full stack web and mobile applications. If you need something done, I'm your guy. And if not, I can point you in the right direction.`,
      },
    ];
  
    let projects = [
      {
        name: "Web and Mobile",
        src: "/full-stack-green.png",
        description: ``,
      }
    ];
    let otherProjectsCount = 4;
  
    let tools = [
      {
        name: ".Net",
        src: "/Core.png",
      },
      {
        name: "Azure SQL",
        src: "/azure sql.png",
      },
      {
        name: "Blazor WebAssembly",
        src: "/Blazor.png",
      },
      {
  
        name: "Angular",
        src: "/angular.svg",
      },
       {
  
        name: "Spring Boot",
        src: "/springboot.png",
      },
      {
        name: "PostgreSQL",
        src: "/postgresql.svg",
      },
      {
        name: "MSSQL",
        src: "/MSSQL.svg",
      },
      {
        name: "Typescript",
        src: "/typescript.svg",
      }
  
    ];
    let tools1 = [...tools].splice(0, 6);
    let tools2 = [...tools].splice(6, 6);
    let tools3 = [...tools].splice(12, 8);
  
    let links = [
      {
        src: "/linkedin.svg",
        href: "https://linkedin.com/in/sifundo-buthelezi-020439148",
        name: "Linkedin"
      },
      {
        src: "/github.svg",
        href: "https://github.com/Sifundo-B",
        name: "Github"
      },
    ]
  </script>
  <main>
    <div class="pb-24 pt-24">
      <div class="flex justify-center">
        <img class="w-60 h-60 rounded-full profile" alt="KomplitApp" src="Profile picture.JPG" />
      </div>
      <h1 class="text-5xl red-text font-thick text-center mb-12">
       Sifundo Buthelezi
      </h1>
      <HeadingText title="Software Developer" />
      <div class="text-center">
        <p>sifundo.buthelezi17@gmail.com</p>
      </div>
  
      <div class="grid grid-cols-12 mb-24 mt-4">
        <div />
        <div />
        <div />
        <div />
        <div />
        {#each links as { src, href, name }}
          <div class="flex flex-col items-center has-tooltip">
            <a {href}>
              <img class="w-12 h-12" alt="{name} logo" {src} />
            </a>
            <span
            class="tooltip rounded shadow-lg p-1  purp text-white text-xs -mt-8"
            >{name}</span
            >
          </div>
        {/each}
      </div>
      <div class="max-w-md mx-auto">
        <p class="text-sm mb-24 text-center">
          <span class="text-purple-800"></span>
        </p>
      </div>
  
  
      <div class=" purp pt-12 pb-12 mb-12">
        <!-- <HeadingText title={'<span class="italic">Value</span> Kami'} isPrimary /> -->
        <div class="grid grid-cols-2 mt-8#F72585">
          {#each values as { src, alt, title, description }}
            <div class="flex flex-col items-center mx-10">
              <img
                {src}
                {alt}
                class="w-24 h-24 mb-4 transform transition-transform hover:rotate-12"
              />
              <p class="text-lg text-center green-text font-medium tracking-wide">
                {@html title}
              </p>
              <p
                class="text-md text-center text-white mt-2 tracking-wide font-light"
              >
                {@html description}
              </p>
            </div>
          {/each}
        </div>
      </div>
  
      <HeadingText title="Things I do" />
      <br/>
      <br/>
      <br/>
      <div class="pl-12 pr-12 grid md:grid-cols-3 sm:grid-cols-2 gap-1 mb-24">
        {#each projects as { name, src, description, href }}
          <ProjectCard {name} {src} {description} {href} />
        {/each}
      </div>
      <div class=" purp pt-12 pb-12 mb-12">
          <div class="mt-8">
            <div class="flex flex-col items-center">
            <!-- <img
            {src}
            {alt}fill="#15F493"
            class="w-24 h-24 mb-4 transform transition-transform hover:rotate-12"
            /> -->
            <p class="text-6xl text-center green-text font-large tracking-wide">
              3+ Years experience
            </p>
            <p class="text-md text-center text-white mt-2 tracking-wide font-light">
              I've been coding for a while. I've helped a lot of projects get off the ground. If you need to take a project to completion, and make sure it can scale, I can help.
            </p>
          </div>
        </div>
      </div>
  
      <HeadingText title={'Tools I Use'} />
      <div class="grid grid-cols-12 mb-24 mt-8">
        <div />
        <div />
        <div />
        {#each tools1 as { name, src }}
          <div class="flex flex-col items-center has-tooltip icon">
            <img class="w-16 h-16" alt={`${name}`} {src} />
            <span
              class="tooltip rounded shadow-lg p-1  purp text-white text-xs -mt-8"
              >{name}</span
            >
          </div>
        {/each}
      </div>
      <div class="grid grid-cols-12 mb-24 mt-4">
        <div />
        <div />
        <div />
        {#each tools2 as { name, src }}
          <div class="flex flex-col items-center has-tooltip icon">
            <img class="w-16 h-16" alt={`${name}`} {src} />
            <span
              class="tooltip rounded shadow-lg p-1  purp text-white text-xs -mt-8"
              >{name}</span
            >
          </div>
        {/each}
      </div>
      <div class="grid grid-cols-12 mb-24 mt-4">
        <div />
        <div />
        <div />
        {#each tools3 as { name, src }}
          <div class="flex flex-col items-center has-tooltip icon">
            <img class="w-16 h-16" alt={`${name}`} {src} />
            <span
              class="tooltip rounded shadow-lg p-1  purp text-white text-xs -mt-8"
              >{name}</span
            >
          </div>
        {/each}
      </div>
  
      <div class="pr-12">
        <p class="text-xs text-right">
          Wonderful icons by <a href="https://streamlineicons.com" target="_blank"
            >Streamline</a
          >
          and <a href="https://devicon.dev/" target="_blank">Devicon</a>
        </p>
      </div>
    </div>
  </main>
  
  <style>
    .tooltip {
      visibility: hidden;
      position: absolute;
    }
    .has-tooltip:hover .tooltip {
      visibility: visible;
      z-index: 100;
    }
  
    ::-moz-selection {
      /* Code for Firefox */
      /* purple-800 */
      color: #5c21b6;
      /* purple-200 */
      background: #ddd6fe;
    }
  
    ::selection {
      color: #5c21b6;
      background: #ddd6fe;
    }
  
    .purp{
      background-color: #3A0CA3;
    }
  
    .red-text{
      color: #F72585;
    }
  
    .green-text{
      color: #15F493;
    }
  
    main {
      background-color: #1f1f1f;
      color: white;
    }
    .icon{
      border: 2px solid #15F493;
      border-radius: 100px;
      margin: auto;
      padding: auto;
    }
    .profile {
      border: 6px solid #15F493;
    }
  </style>
  