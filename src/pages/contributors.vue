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
          <div>
            <User :user="curator.name" :bio="curator.bio" />
            <br />
            <br />
            <hr />
          </div>
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
      title: "Meet the contributors!",
    };
  },
  data() {
    return {
      managers: [
        // ⏬ is the list of managers. Only touch the below if you're adding/changing a manager
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
          bio: "Hi! My name is garnetluvcookie, but you can call me Aria. I contribute by being a Wiki Editor and a Forum helper (not on this account, though). I like contributing because I love helping others. Fun fact about me: I'm allergic to marshmallows :/.",
        },
        {
          name: "cards104171",
          bio: "Hi, I'm cards104171! Feel free to call me Cards. I'm a current Scratch Wiki Contributor and a past FPCAH Curator. I contribute because I like helping out fellow Scratchers and find it fun to be involved in the Scratch community. I'm also a female, bookworm, and nerd that likes to code and write! In addition, I'm learning more HTML/CSS and trying to improve my coding on Scratch.",
        },
        {
          name: "puppycutest",
          bio: "Hiya! My name is puppycutest, but everyone can call me Jojo! I contribute to the FPC Application Help Studio! I am a contributor to the Discussion Forums, I also am a curator of Future FPCs!  Contributing is fun because I get to play a part in helping the Scratch Community! A fun fact about me is that I am a voice actress and a GIANT bookworm! Scratch on! (^w^)",
        },
        {
          name: "dogsmakemehappy",
          bio: "Hi, I'm @dogsmakemehappy. I am a forum helper and a scratch wiki editor. I like to contribute because I am bored and it helps the community. I'm @shluffy as well.",
        },
        {
          name: "AmazingMech2418",
          bio: "Hi, I'm Mech! I help out on the open-source code end of Scratch through GitHub. I contribute here because I enjoy programming and this gives me a way to contribute to Scratch and program in JavaScript at the same time! Though, the Scratch Team does get mad when I submit pull requests for issues that don't say 'help wanted'. XD Though, I have had a pull request merged before in scratch-vm, which is what determines how Scratch runs projects. I also am helping the Scratch Team with a security feature I am working on at the request of @Paddle2See. I still do need to do a few more things before this can get rolled out, but it should be coming soon, and might even help repeal the Browser Extensions/Userscript Policy (or at least parts of it) while still maintaining security.",
        },
        {
          name: "leahcimto",
          bio: "Hello! I'm leahcimto, also known as Mike! A Scratch Welcoming Committee Reviewer, Manager of The Forum Helpers, Scratch Wiki Editor, Previous Scratch Design Studio Helper, Front Page Curator Application Help Curator, and a Propose Projects To Be Featured curator. I enjoy creating front-end websites and playing Minecraft. I hope to see you around!",
        },
        {
          name: "zigzaq",
          bio: "hi! i’m ann and i’m a scratch wiki editor and i like contributing because i like helping people! a fun fact about me is that i like rollerblading",
        },
        {
          name: "Mrcakeyman89",
          bio: "Hello! I'm Mrcakeyman89, a human who's been scratching for about 2 1/2 years! I like to help out here on the forums, (unofficial forum helper) and I work at the SDS studios. Besides animating and coding on scratch, I enjoy writing & reading books, playing keyboard, baking, and eating food. I run my own shop in the forums, work at 2 others, and is great a BBCode. I hope to chat with you later. See you around!",
        },
        {
          name: "nightmxre-",
          bio: "Hi! I'm nightmxre-. I am a SDS Helper, PPTBF Curator, and FPCAH Curator. I contribute because I enjoy helping around the Scratch community! I do coding in Scratch, Python, HTML & CSS. I am a 13 year old girl who loves photography, programming, sports, skateboarding, and science!",
        },
        {
          name: "ButterPopcorn8",
          bio: "Hey y'all, ButterPopcorn8 here(Otherwise known as Goose). I'm a FPCAH Curator and a Scratch Wiki Contributor. I'm a huge anime weeb and a bookworm. I'm also an self-taught artist who is too broke to get a stylus TvT <s>and has suffered from depression for a while</s>. I like to contribute cause I can help people out and give feedback and see different types of projects. Fun Fact: You're reading this.\n Now if y'all excuse me, ima go sleep. See ya <333",
        },
        {
          name: "9gr",
          bio: "Hello, I'm 9gr! I frequently go around foruming in the Advanced Topics. I am a forumer and a TFH Curator. I like contributing because I can help other people get better at scratching and other programming languages! Fun fact: ocular is better for searching the forums",
        },
        {
          name: "SausageMcSauce",
          bio: "I am SausageMcSauce, and I have been an active Scratch Wiki contributor since 2018, as well as being a member of the Forum Helpers studio. I find both editing the Scratch Wiki and posting in the forums enjoyable. Also, as a random fact because I am sort-of required to, my favourite colour is red (and I use British English).",
        },
        {
          name: "2GS6",
          bio: "Hello I am 2GS6. You probably know me as SDS Manager  the german Scratch Wiki, PPTBF or the FPCA studio. I love reading and science. With contributing you can help people and Scratch is a great place for everyone I am also a girl and learning HTML at school :)",
        },
        {
          name: "JPANDD",
          bio: "Hiya, I am JPANDD! I work on the wiki I help many FPC's after they get accepted learn how they can show their schedule! I am a proud helper of the [s]illuminati[/s] Scratch wiki! I also make funny, animations. And loads of different projects... I also am a really bad pixel art and game artist",
        },
        {
          name: "IrisPLime",
          bio: "Hiya! I'm Iris from the FPCAH. I contribute in the FPCAH because I love helping others improve their projects with constructive feedback. I'm a 10(nearly 11) year old girl who [s]likes[/s] loves k-pop (BlackPink), sports, drawing, and gymnastics! I started scratch when I was a little 9 year old and have continued ever since on the same account(this one) I am a Blink(BlackPink fan) and I am part of the student council. Anyway, Bye!",
        },
        {
          name: "Toripikchu",
          bio: "Hi im Tori! I'm an SDS Curater and I have been in the SDS ( scratch design studio) for about a year now. I enjoy helping the community becuase its fun and it gives me something to do when im bored. Im a member of the LGBTI+ community ( im trans ) and I enjoy playing videos games with friends in my spare time, I also like eating, and sleeping :)",
        },
      ],
      curators: [
        // ⏬ is the list of curators. Only touch the below if you're adding/changing/promoting a curator
        {
          name: "logdra",
          bio: "Hey! I’m logdra, your typical Scratcher who contributes in the Scratch Design Studios.  I started reviewing projects in the “In The Air” studio, and officially became a helper in “Colorless” and later “Expect the Unexpected”.  I contribute, because I like seeing different types of projects made by different Scratchers from across the world!  I’m also ambiverted, a nerd, a bookworm, an athlete, and nature enthusiast!",
        },
        {
          name: "-Sprout15-",
          bio: "Hiya!! I'm -Sprout15-, \nI have contributed in places such as FPCA help, and i have been a past FPC. I contribute because, helping people puts a smile on their face, and when they put a smile on their face, they make me smile. I absolutely enjoy hikes, piano, singing, coding and much more things!! Adios <3 ",
        },
        {
          name: "vedrc",
          bio: "Hey there! I’m @vedrc. I was a past FPC for Scratch and would love to help with feedback on your applications. I also was a curator of the old PPTBF studio. I contribute because I love Scratch a lot. I love seeing the diversity of projects created and how small creators can rise to become well known names within the community. I make noteblocks on Scratch, and have been playing piano for around 9 years now!",
        },
        {
          name: "bobcat0701",
          bio: "Why hello there I'm bobcat0701! I edit the wiki, add to pptbf, and help out on the forums. I use the he/him pronouns. I love to to help on scratch because I also do so irl. my cats and I thank everyone who helps out on scratch!",
        },
        {
          name: "Annabeth_Chase1979",
          bio: "Hi! I'm Paris! My account is Annabeth_Chase1979. I'm 15 years old and I love reading! I read 3 books a day, along with tutoring over 50 people, grading homework, creating homework etc..\nI love teaching my students! I try to get active on scratch as much as I can.\n\nI curate Propose Projects to be Featured.\nI like curating PPTBF, because when I add a project, scratchers are so happy and I love reading happy comments.\nCheck out my profile here!\n\n",
        },
        {
          name: "SomeCoderperson",
          bio: "Hey! I'm @somecoderperson, I contribute to the Scratch Welcoming Committee! I might contribute to more things in the future but for now, that's it. I contribute for a few reasons: 1. The Scratch Welcoming Committee is a place for welcoming new scratchers, I really enjoy welcoming them I guess! :P 2. New scratchers sometimes never really get welcomed, and that's not a nice way to start out in this website, so, there needs to be people to make sure that NEVER happens. That's where people like me come in! :) And remember, you don't have to be a member to welcome someone, everybody can do it! :D 3. New scratchers often need help and tips, and Google won't always help with things like that. :P So it's important to do that stuff, I really enjoy it!\n\nWell, bye! :D",
        },
        {
          name: "MoreThanEnuff",
          bio: "Haldo everybody everybody! I am MoreThanEnuff (but you can call me Jimmi/Jimmi Jackal). I mainly contribute on the forums, where I mainly answer questions in “Questions about Scratch” and give feedback on “Suggestions”. The main reason I contribute is so I can spread my knowledge of the site to others, and also make others happy. I am a member of the Scratch Object Show Community, and I've been using Scratch for nearly 6 years now.",
        },
        {
          name: "ninjaMAR",
          bio: "I'm ninjamar. I mainly use the forums helping people out in the advanced topics and questions about scratch. I contribute because I enjoy helping others and I get a chance to use my knowledge. I like python. I use linux. I'm an ATer.",
        },
        {
          name: "Mydoggiedaisy",
          bio: "Hello! I'm Mydoggiedaisy, commonly known as Daisy. I help out in the FPCAH, working on becoming more involved in the forums, and am working on a FPC application. I help out because I enjoy it; not for the titles or anything like that. I enjoy giving people constructive feedback, and working with them. I'm also your District 11 Divergent Slytherdor (personally I think everyone can only have one house. If I'm following that, I'm a  Gryffindor) who's unclaimed, although suspected to be a daughter of Zeus, Ares, or Hades, who loves reading, writing, and sports. ",
        },
        {
          name: "coco7nut",
          bio: "Hello! I'm Coco7nut, currently, I only contribute one place is Scratch Wiki. I love contributing because I want to help people and to tutorials. I know Python, C++, HTML, CSS, a little Java, and some Ruby. My favorite game engine is Unity. I like playing with Micro::Bit and Arduino. My browser / operating system: Windows NT 10.0, Chrome 90.0.4430.212, No Flash version detected. My favorite food is fish. My friend is @Renzejr although he's not active much. I have an account in telehack.com but Forbin and Wumpus always ban me ( They are the creator of telehack ).\n\nP/S: I love kumquats and they don't hack my account\n",
        },
        {
          name: "PUNNAMOODU",
          bio: "Hi there! I am Punnamoodu! I have been on scratch for 3 years now - but only recently did I start to become active as a Scratch contributor. I am active on the forums, the SDS, and the English Scratch Wiki. ",
        },
        {
          name: "P0tat0_Spy",
          bio: "Hi everybody, I'm P0tat0_Spy! I like to help out on Scratch where I can, and I frequently help out new Scratchers. I also make projects to inform people about scams and tricks on Scratch, (they're mainly love-farms and F4F confidence tricks). I believe in Assuming Good Faith — that is, believing that no action is intended to break the Scratch CG's or be mean, even if it looks that way on the surface. I have a Scratch Wiki account, but I'm rarely active on it as I could never get my head around the editor! I used to program in a different (and simpler) programming tool, but it shut down so I moved to Scratch. I'm currently trying to recreate a game which I made in the old language — I've been working on it for over a year now! I also maintain a website for the game, because a website shows everyone that you're serious. Thanks everybody! See you around!",
        },
        {
          name: "ScratchTag-",
          bio: "Helooi! I'm ScratchTag-, commonly known as tag. I predominantly contribute scratch as a PPTBF curator, Scratch wiki editor etc. moreover, I also help new scratchers and other scratch-related activities. I am very much interested in helping and cooperating with community because It gives my the positivity when hearing the scratchers' kind words and I am thankful to the scratch team for making this website.\nThanks",
        },
        {
          name: "aderne5739",
          bio: "Hi! I'm aderne5739, aka Ade. I'm a Wiki contributor. I ride horses and love to read! I like to contribute because I love grammar and I figured I would help people with their's. (Not saying anyone's grammar is bad!) Fun Fact: It's my scratchiversary today!",
        },
      ], // ⏫ is the list of curators. You shouldn't be touching stuff after this unless you know what you're doing
    };
  }
};
</script>
