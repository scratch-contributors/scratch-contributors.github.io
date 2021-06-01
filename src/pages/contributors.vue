<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1>Contributors</h1>
      <h3>Managers</h3>
      <div>
        <div v-for="manager in managers" :key="manager.name">
          <br />
          <User :user="manager.name" :bio="manager.bio" />
          <br />
          <hr />
        </div>
      </div>
      <br />
      <br />
      <br />
      <h3>Curators</h3>
      <div>
        <div v-for="curator in curators" :key="curator.name">
          <br />
          <User :user="curator.name" :bio="curator.bio" />
          <br />
          <hr />
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: 'Meet the contributors!'
    }
  },
  data() {
    return {
      managers: [ // ⏬ is the list of managers. Only touch the below if you're adding/changing a manager
        {
          name: "wangat",
          bio: "Hi! I'm wangat! I contribute in many places, as an Scratch Welcoming Committee Reviewer, Scratch Design Studio Helper, The Forum Helpers Curator, Scratch Wiki Contributor, Propose Projects to be Featured Curator, and Front Page Curator Application Help Curator. I contribute because I like helping Scratch a better place! I'm also 13, male, a Ravenclaw, and know some HTML. You can usually find me on the forums, the SDS, and SWC! :D",
        },
        {
          name: "ConfusedBiscuit",
          bio: "Hi! I’m Biscuit/Takara. I’m the occasional forum helper because I like to help around when I get a chance! Other than that I’m your local marine biology junkie",
        },
        {
          name: "President_Dave",
          bio: "Hi I'm Dave! I'm a wiki editor, forum helper (not in the studio) and FPCAH! I contribute because scratch allowed me to code things I've never do before! and because of that I'm learning python! and getting to know it. Now I want scratchers to be able to do that too! By providing information and many more I just like being generally helpful :0",
        },
        {
          name: "han614698",
          bio: "Hi, I’m han! I’m a verified Forum Helper curator, former PPTBF curator, and I am quite active. I contribute because I love helping out other people! I know python, HTML, Scratch, Snap! JS and CSS. I have 2200+ posts on the forums. I’m one of the only 2000+ posters that doesn't have an account for cubeupload etc and doesn't have nono word (forumer inside joke lol).",
        },
        {
          name: "TheDogLover796",
          bio: "Hai! I'm TheDogLover796! Feel free to call me Dog/DogLover  I contribute by being a past SDS Helper, and I help out in the forums sometimes, but and not a forum helper curator/manager. I contribute because 1st of all, it's actually pretty fun, and 2nd of all,  it's nice to have the feeling when you help someone  A fun fact about me is I love dogs, and am a SMC Judge!",
        },
        {
          name: "CleverComment",
          bio: "Hi there! My name is CleverComment, but you can call me Clev or CC or Clever. XD  I contribute by helping in the FPCA and FPCAH studios and being a Scratch Camp counselor in 2020.  I like contributing because it's awesome! I love helping other people. I'm actually from New Zealand!",
        },
        {
          name: "garnetluvcookie",
          bio: "Hi! My name is garnetluvcookie, but you can call me Aria. I contribute by being a Wiki Editor and a Forum helper (not on this account, though). I like contributing because I love helping others. Fun fact about me: I'm allergic to marshmallows :/."
        },
        {
          name: "cards104171",
          bio: "Hi, I'm cards104171! Feel free to call me Cards. I'm a current Scratch Wiki Contributor and a past FPCAH Curator. I contribute because I like helping out fellow Scratchers and find it fun to be involved in the Scratch community. I'm also a female, bookworm, and nerd that likes to code and write! In addition, I'm learning more HTML/CSS and trying to improve my coding on Scratch."
        },
        {
          name: "puppycutest",
          bio: "Hiya! My name is puppycutest, but everyone can call me Jojo! I contribute to the FPC Application Help Studio! I am a contributor to the Discussion Forums, I also am a curator of Future FPCs!  Contributing is fun because I get to play a part in helping the Scratch Community! A fun fact about me is that I am a voice actress and a GIANT bookworm! Scratch on! (^w^)"
        },
        {
          name: "dogsmakemehappy",
          bio: "Hi, I'm @dogsmakemehappy. I am a forum helper and a scratch wiki editor. I like to contribute because I am bored and it helps the community. I'm @shluffy as well."
        },
        {
          name: "AmazingMech2418",
          bio: "Hi, I'm Mech! I help out on the open-source code end of Scratch through GitHub. I contribute here because I enjoy programming and this gives me a way to contribute to Scratch and program in JavaScript at the same time! Though, the Scratch Team does get mad when I submit pull requests for issues that don't say 'help wanted'. XD Though, I have had a pull request merged before in scratch-vm, which is what determines how Scratch runs projects. I also am helping the Scratch Team with a security feature I am working on at the request of @Paddle2See. I still do need to do a few more things before this can get rolled out, but it should be coming soon, and might even help repeal the Browser Extensions/Userscript Policy (or at least parts of it) while still maintaining security."
        },
        {
          name: "leahcimto",
          bio: "Hello! I'm leahcimto, also known as Mike! A Scratch Welcoming Committee Reviewer, Manager of The Forum Helpers, Scratch Wiki Editor, Previous Scratch Design Studio Helper, Front Page Curator Application Help Curator, and a Propose Projects To Be Featured curator. I enjoy creating front-end websites and playing Minecraft. I hope to see you around!"
        },
        {
          name: "zigzaq",
          bio: "hi! i’m ann and i’m a scratch wiki editor and i like contributing because i like helping people! a fun fact about me is that i like rollerblading"
        },
        {
          name: "Mrcakeyman89",
          bio: "Hello! I'm Mrcakeyman89, a human who's been scratching for about 2 1/2 years! I like to help out here on the forums, (unofficial forum helper) and I work at the SDS studios. Besides animating and coding on scratch, I enjoy writing & reading books, playing keyboard, baking, and eating food. I run my own shop in the forums, work at 2 others, and is great a BBCode. I hope to chat with you later. See you around!"
        },
        {
          name: "nightmxre-",
          bio: "Hi! I'm nightmxre-. I am a SDS Helper, PPTBF Curator, and FPCAH Curator. I contribute because I enjoy helping around the Scratch community! I do coding in Scratch, Python, HTML & CSS. I am a 13 year old girl who loves photography, programming, sports, skateboarding, and science!"
        },
        {
          name: "ButterPopcorn8",
          bio: "Hey y'all, ButterPopcorn8 here(Otherwise known as Goose). I'm a FPCAH Curator and a Scratch Wiki Contributor. I'm a huge anime weeb and a bookworm. I'm also an self-taught artist who is too broke to get a stylus TvT <s>and has suffered from depression for a while</s>. I like to contribute cause I can help people out and give feedback and see different types of projects. Fun Fact: You're reading this.\n Now if y'all excuse me, ima go sleep. See ya <333"
        }
      ],
      curators: [ // ⏬ is the list of curators. Only touch the below if you're adding/changing/promoting a curator
        {
          name: "logdra",
          bio: "Hey! I’m logdra, your typical Scratcher who contributes in the Scratch Design Studios.  I started reviewing projects in the “In The Air” studio, and officially became a helper in “Colorless” and later “Expect the Unexpected”.  I contribute, because I like seeing different types of projects made by different Scratchers from across the world!  I’m also ambiverted, a nerd, a bookworm, an athlete, and nature enthusiast!"
        },
        {
          name: "-Sprout15-",
          bio: "Hiya!! I'm -Sprout15-, \nI have contributed in places such as FPCA help, and i have been a past FPC. I contribute because, helping people puts a smile on their face, and when they put a smile on their face, they make me smile. I absolutely enjoy hikes, piano, singing, coding and much more things!! Adios <3 "
        },
        {
          name: "vedrc",
          bio: "Hey there! I’m @vedrc. I was a past FPC for Scratch and would love to help with feedback on your applications. I also was a curator of the old PPTBF studio. I contribute because I love Scratch a lot. I love seeing the diversity of projects created and how small creators can rise to become well known names within the community. I make noteblocks on Scratch, and have been playing piano for around 9 years now!"
        },
        {
          name: "bobcat0701",
          bio: "Why hello there I'm bobcat0701! I edit the wiki, add to pptbf, and help out on the forums. I use the he/him pronouns. I love to to help on scratch because I also do so irl. my cats and I thank everyone who helps out on scratch!"
        }
      ] // ⏫ is the list of curators. You shouldn't be touching stuff after this unless you know what you're doing 
    };
  }
};
</script>
