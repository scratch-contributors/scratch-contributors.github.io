<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1 style="color: black">Contributors</h1>
      <h3>Managers</h3>
      <div>
        <div v-for="manager in managers" :key="manager.name">
          <User :user="manager.name" :bio="manager.bio" />
          <hr />
        </div>
      </div>
      <br />
      <br />
      <br />
      <h3>Curators</h3>
      <div>
        <div v-for="curator in curators" :key="curator.name">
          <User :user="curator.name" :bio="curator.bio" />
          <hr />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Meet the contributors",
      managers: [
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
      ],
      curators: []
    };
  }
};
</script>
