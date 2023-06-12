<!-- <script>
export default {}
</script>

<template lang="">
  <div class="col-span-full md_col-span-2 pt-12 md_pt-24 text-center md_text-left dark:text-white">
    <h1
      class="fs-8 medium-fs-2 text-3xl leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-full"
    >
      A litle bit of our history
    </h1>
    <p class="w-70vh mx-auto mt-9 mb-5 font-bold">
      Grouzy is a mix of influence, obsession, passion and entrepreneurial DNA.
    </p>
    <p class="w-70vh mx-auto mt-9 mb-5">
      The founder, through his 16+ years of experience in sales, went from closing sales to solving
      problems, thanks to the understanding that companies pay for solutions to their problems.
      problems. And he realized that most of the problems companies had were process and team based.
    </p>
    <p class="w-70vh mx-auto mt-9 mb-5">
      Companies hire people to solve problems. But sometimes these problems are beyond human
      capacity to understand and solve. In those cases, that's where Blockchain technology comes in.
    </p>
    <p class="w-70vh mx-auto mt-9 mb-5">
      In his search for an efficient and revolutionary solution, the founder of our company
      discovered the immense potential of Blockchain technology to transform the way businesses
      operate. With a focus on improving internal processes and team collaboration, our company has
      focused on applying the Blockchain to solve the most complex business problems.
    </p>
    <p class="w-70vh mx-auto mt-9 mb-5">
      The Blockchain, with its ability to provide transparency, security and efficiency, allows
      businesses to operate in a more seamless and secure manner. By eliminating the need for
      middlemen and simplifying transaction verification, the Blockchain can help companies save
      time and resources, while increasing trust and accountability among team members.
    </p>
    <p class="w-70vh mx-auto mt-9 mb-5">
      Our company has developed a number of Blockchain-based solutions that are tailored to a
      variety of industries, from finance to logistics to retail to healthcare. These solutions are
      designed to optimize processes, enhance team collaboration and provide an unprecedented level
      of transparency and security.
    </p>
    <p class="w-70vh mx-auto mt-9 mb-5">
      The founder, with his strong sales background and deep understanding of Blockchain technology,
      has succeeded in forging a company that stands out in the field of Blockchain-based enterprise
      solutions. His passion and dedication have led our company to be recognized as an industry
      leader, with a solid reputation for innovation and excellence.
    </p>
  </div>
</template>

<style lang=""></style>
 -->

<template>
  <div class="container">
    <div class="about-us">
      <div
        class="col-span-full md_col-span-2 pt-12 md_pt-24 text-center md_text-left dark:text-white"
      >
        <h1
          class="fs-8 medium-fs-2 text-3xl leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-full"
        >
          A little bit of our history
        </h1>
        <p
          class="fs-8 medium-fs-2 text-3xl leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-full"
        >
          Grouzy is a mix of influence, obsession, passion and entrepreneurial DNA.
        </p>
        <div class="p-10 mx-auto notepad">
          <p class=" mt-9 mb-5">
            The founder, through his 16+ years of experience in sales, went from closing sales to
            solving problems, thanks to the understanding that companies pay for solutions to their
            problems. problems. And he realized that most of the problems companies had were process
            and team based.
          </p>
          <p class=" mt-9 mb-5">
            Companies hire people to solve problems. But sometimes these problems are beyond human
            capacity to understand and solve. In those cases, that's where Blockchain technology
            comes in.
          </p>
          <p class=" mt-9 mb-5">
            In his search for an efficient and revolutionary solution, the founder of our company
            discovered the immense potential of Blockchain technology to transform the way
            businesses operate. With a focus on improving internal processes and team collaboration,
            our company has focused on applying the Blockchain to solve the most complex business
            problems.
          </p>
          <p class=" mt-9 mb-5">
            The Blockchain, with its ability to provide transparency, security and efficiency,
            allows businesses to operate in a more seamless and secure manner. By eliminating the
            need for middlemen and simplifying transaction verification, the Blockchain can help
            companies save time and resources, while increasing trust and accountability among team
            members.
          </p>
          <p class=" mt-9 mb-5">
            Our company has developed a number of Blockchain-based solutions that are tailored to a
            variety of industries, from finance to logistics to retail to healthcare. These
            solutions are designed to optimize processes, enhance team collaboration and provide an
            unprecedented level of transparency and security.
          </p>
          <p class=" mt-9 mb-5">
            The founder, with his strong sales background and deep understanding of Blockchain
            technology, has succeeded in forging a company that stands out in the field of
            Blockchain-based enterprise solutions. His passion and dedication have led our company
            to be recognized as an industry leader, with a solid reputation for innovation and
            excellence.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imageUrl: "./src/assets/images/10492.jpg",
    }
  },
}
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600&display=swap');

$linespace: 30px;

.notepad {
  position: relative;
  color: black;
  width: 80%;
  padding: 30px;
  margin: 100px auto;
  text-align: center;
  background-color: #F6F6F6;
  height: 800px;
  background: linear-gradient(rgba(246, 246, 246, 0), #FCFCFC), linear-gradient(rgba(246, 246, 246, 1), rgba(246, 246, 246, 1) 30px, #EAEAEA 30px, #EAEAEA 31px);
  background-size: 100%, 100% 31px;
  box-shadow: 0 4px 4px rgba(0,0,0,0.2);
}

.notepad:before {
  content: '';
  height: 470px;
  width: 100%;
  position: absolute;
  top: -47px;
  left: 0;
  background: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/2065/paper_1.jpg');
  box-shadow: 0 10px 4px rgba(0, 0, 0, 0.2);
  z-index: -1;
}

h3 {
  font-size: 2em;
  font-family: 'Open Sans', sans-serif;
  color: #323232;
}

.container {
  max-width: 80rem;
}
.about-us {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 1em;
}

.about-us-image {
  display: flex;
  flex-direction: row;
}

.about-us-image img {
  max-width: 100%;
  height: auto;
}

.about-us-content p {
  margin: 0;
  padding: 0;
}
</style>
