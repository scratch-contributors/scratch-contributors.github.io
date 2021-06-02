<template>
  <div class="container">
    <Header />
    <div class="margined">
      <div>
        <h1>Welcome to the new site for the Scratch Contributors!</h1>
        <p>
          We are a studio on <a href="https://scratch.mit.edu/">Scratch</a> that
          celebrates everybody who has contributed to scratch! This includes:
        </p>
        <ul>
          <li>
            <a href="https://en.scratch-wiki.info/wiki/Scratch_Team">
              Scratch Team Members
            </a>
          </li>
          <li>Scratch Moderators</li>
          <li>
            <a href="https://en.scratch-wiki.info/wiki/Scratch_Mentors">
              Scratch Mentors
            </a>
          </li>
          <li>Scratch Design Studio (SDS) Curators, Helpers and Translators</li>
          <li>
            <a href="https://scratch.mit.edu/studios/146521/">
              Scratch Welcoming Committee (SWC) Members, Curators, Reviewers and
              Translators
            </a>
          </li>
          <li>
            <a href="https://scratch.mit.edu/studios/28715018/">
              Scratch Propose Projects to be Featured (PPTBF) Curators and
              Translators
            </a>
          </li>
          <li>
            <a href="https://scratch-wiki.info"> Scratch Wiki Contributors </a>
          </li>
          <li>
            .. and more! Check the
            <a href="https://scratch.mit.edu/studios/26371714/"
              >studio description</a
            >
            for the whole list!
          </li>
        </ul>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home",
    };
  },
};
</script>
