
<template>
   <div class="">
      <div
         class="text-white monserrat-semibold-italic text-lg lg:text-3xl py-7 lg:px-10 flex justify-center lg:justify-between">
         <img src="../assets/images/star.svg" class="single-star-small lg:single-star scale-star" />
         <!-- <img src="../assets/images/Purple-Lens.svg" class="absolute z-10" /> -->
         <div class="absolute right-0 px-3">
            <Typed :options="mantra">
               <div class="typing inline"></div>
            </Typed>
            <div class="flex justify-end">
               <img src="../assets/images/curly-line.svg" class="mr-4" />
            </div>
         </div>
      </div>

      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto mt-10">
            <div class="grid md:grid-cols-2 gap-7 items-center text-white relative">
               <div class="text-center md:text-left">
                  <!-- <img src="../assets/images/Title.svg" /> -->
                  <span class="flex justify-end">
                     <img src="../assets/images/lightbulb.gif" class="w-[100px] bulbglow" />
                  </span>
                  <div class="clashdisplay-bold text-white text-4xl md:text-6xl text-center md:text-left">

                     <Typed :options="options">
                        <h1 class="typing inline"></h1>
                        <img src="../assets/images/chain.svg" class="inline w-[50px]" />
                        <img src="../assets/images/spark.svg" class="inline w-[50px]" />
                     </Typed>
                  </div>
                  <div class="text-white monserrat-reg mt-4">Participate in getlinked tech Hackathon 2023 stand a chance to
                     win a Big prize</div>
                  <button type="button" data-te-ripple-init data-te-ripple-color="light" @click="reloadpage(1)"
                     class="monserrat-reg primary-btn mt-4 mr-3 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                     Register
                  </button>
                  <div class="unica-one text-5xl mt-10">
                     {{ hour }}<span class="text-xs">H</span> &nbsp;{{ minutes.toString() == '60' ? '00' : minutes }}<span
                        class="text-xs">M</span> &nbsp;{{ seconds.toString() == '60' ? '00' : seconds }}<span
                        class="text-xs">S</span>
                  </div>
               </div>
               <div>
                  <img src="../assets/images/man-wearing-smart.png" style="filter: grayscale(100%); width: 100%" />
                  <img src="../assets/images/virtual-reality.svg"
                  class="absolute bottom-0  virtual-svg xs:w-[80%] sm:w-[100%] md:w-[45%]" />
               </div>
            </div>
         </div>
      </div>

      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto py-10">
            <div class="grid md:grid-cols-2 gap-10 items-center text-white ">
               <img src="../assets/images/bigidea.svg" class="floating-image" />
               <div class="">
                  <div ref="elementone">
                  <Typed :options="introduction" v-if="toggleIntroduction">
                     <div class="typing clashdisplay-bold text-white text-4xl text-center md:text-left" ></div>
                     </Typed>
                  </div>
                  <div class="monserrat-reg text-white leading-7 mt-5 text-center md:text-left" data-aos="fade-right">
                     Our tech hackathon is a melting pot of visionaries, and its purpose is as
                     clear as day: to shape the future. Whether you're a coding genius, a
                     design maverick, or a concept wizard, you'll have the chance to transform
                     your ideas into reality. Solving real-world problems, pushing the boundaries
                     of technology, and creating solutions that can change the world,
                     that's what we're all about!
                  </div>
               </div>
            </div>
         </div>
      </div>

      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto py-10">
            <div class="grid md:grid-cols-2 gap-10 items-center text-white ">
               <img src="../assets/images/lady-sitting.svg" class="floating-image md:hidden" />
               <div class="">
                  <div ref="elementtwo">
                  <Typed :options="rules" v-if="toggleRules">
                    <div class="typing clashdisplay-bold text-white text-4xl text-center md:text-left" ></div>
                  </Typed>
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5 text-center md:text-left" data-aos="fade-right">
                     Our tech hackathon is a melting pot of visionaries, and its purpose is as
                     clear as day: to shape the future. Whether you're a coding genius, a
                     design maverick, or a concept wizard, you'll have the chance to transform
                     your ideas into reality. Solving real-world problems, pushing the boundaries
                     of technology, and creating solutions that can change the world,
                     that's what we're all about!
                  </div>
               </div>
               <img src="../assets/images/lady-sitting.svg" class="floating-image hidden md:block" />
            </div>
         </div>
      </div>

      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto py-[6rem]">
            <div class="grid md:grid-cols-2 gap-10 items-center text-white ">
               <img src="../assets/images/judges.svg" class="floating-image w-full" />
               <div class="text-center md:text-left">
                  <div ref="elementthree">
                  <Typed :options="judge" v-if="toggleJudge">
                    <div class="typing clashdisplay-bold text-white text-4xl"></div>
                  </Typed>
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5">
                     <span class="text-[#FF26B9] monserrat-semibold ">Innovation and Creativity</span>: Evaluate the
                     uniqueness and creativity
                     of the
                     solution. Consider whether it addresses a real-world problem in a novel
                     way or introduces innovative features.
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5">
                     <span class="text-[#FF26B9] monserrat-semibold ">Functionality</span>: Assess how well the solution
                     works. Does it perform its
                     intended functions effectively and without major issues? Judges would
                     consider the completeness and robustness of the solution.
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5">
                     <span class="text-[#FF26B9] monserrat-semibold ">Impact and Relevance</span>: Determine the potential
                     impact of the solution
                     in the real world. Does it address a significant problem, and is it relevant
                     to the target audience? Judges would assess the potential social,
                     economic, or environmental benefits.
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5">
                     <span class="text-[#FF26B9] monserrat-semibold ">Technical Complexity</span>: Evaluate the technical
                     sophistication of the solution.
                     Judges would consider the complexity of the code, the use of advanced
                     technologies or algorithms, and the scalability of the solution.
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5">
                     <span class="text-[#FF26B9] monserrat-semibold ">Adherence to Hackathon Rules:</span>: Judges will
                     Ensure that the team adhered
                     to the rules and guidelines of the hackathon, including deadlines, use of
                     specific technologies or APIs, and any other competition-specific requirements.
                  </div>
                  <button type="button" data-te-ripple-init data-te-ripple-color="light"
                     class="monserrat-reg primary-btn mt-10 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                     Read more
                  </button>
               </div>
            </div>
         </div>
      </div>

      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto py-[6rem]">
            <div class="grid md:grid-cols-2 gap-10 items-center text-white ">
               <div class="text-center md:text-left">
                  <div ref="elementfour">
                  <Typed :options="questions" v-if="toggleQuestions">
                    <div class="typing clashdisplay-bold text-white text-4xl"></div>
                  </Typed>
                  </div>
                  <div class="monserrat-reg text-white leading-7  mt-5">
                     We got answers to the questions that you might
                     want to ask about getlinked Hackathon 1.0
                  </div>
                  <a class="flex justify-between mt-7 py-3 monserrat-reg border-b border-b-[#D434FE]" data-te-collapse-init
                     data-te-ripple-init data-te-ripple-color="light" href="#collapseExample1" role="button"
                     aria-expanded="false" aria-controls="collapseExample1">
                     <div>Can I work on a project I started before the hackathon?</div>
                     <div class="text-[#D434FE] text-[20px]">+</div>
                  </a>
                  <div class="!visible hidden" id="collapseExample1" data-te-collapse-item>
                     <div
                        class="block rounded-b-lg monserrat-reg bg-transparent border-b border-b-[rgba(255,255,255,0.18)] border-x border-x-[rgba(255,255,255,0.18)]  p-4  dark:bg-neutral-700 dark:text-neutral-50">
                        Some placeholder content for the collapse component. This panel is
                        hidden by default but revealed when the user activates the relevant
                        trigger.
                     </div>
                  </div>
                  <a class="flex justify-between mt-7 py-3 monserrat-reg border-b border-b-[#D434FE]" data-te-collapse-init
                     data-te-ripple-init data-te-ripple-color="light" href="#collapseExample2" role="button"
                     aria-expanded="false" aria-controls="collapseExample2">
                     <div>What happens if I need help during the hackathon?</div>
                     <div class="text-[#D434FE] text-[20px]">+</div>
                  </a>
                  <div class="!visible hidden" id="collapseExample2" data-te-collapse-item>
                     <div
                        class="block rounded-b-lg monserrat-reg bg-transparent border-b border-b-[rgba(255,255,255,0.18)] border-x border-x-[rgba(255,255,255,0.18)]  p-4  dark:bg-neutral-700 dark:text-neutral-50">
                        Some placeholder content for the collapse component. This panel is
                        hidden by default but revealed when the user activates the relevant
                        trigger.
                     </div>
                  </div>
                  <a class="flex justify-between mt-7 py-3 monserrat-reg border-b border-b-[#D434FE]" data-te-collapse-init
                     data-te-ripple-init data-te-ripple-color="light" href="#collapseExample3" role="button"
                     aria-expanded="false" aria-controls="collapseExample3">
                     <div>What happens if I don't have an idea for a project?</div>
                     <div class="text-[#D434FE] text-[20px]">+</div>
                  </a>
                  <div class="!visible hidden" id="collapseExample3" data-te-collapse-item>
                     <div
                        class="block rounded-b-lg monserrat-reg bg-transparent border-b border-b-[rgba(255,255,255,0.18)] border-x border-x-[rgba(255,255,255,0.18)]  p-4  dark:bg-neutral-700 dark:text-neutral-50">
                        Some placeholder content for the collapse component. This panel is
                        hidden by default but revealed when the user activates the relevant
                        trigger.
                     </div>
                  </div>
                  <a class="flex justify-between mt-7 py-3 monserrat-reg border-b border-b-[#D434FE]" data-te-collapse-init
                     data-te-ripple-init data-te-ripple-color="light" href="#collapseExample4" role="button"
                     aria-expanded="false" aria-controls="collapseExample4">
                     <div>Can I join a team or do I have to come with one?</div>
                     <div class="text-[#D434FE] text-[20px]">+</div>
                  </a>
                  <div class="!visible hidden" id="collapseExample4" data-te-collapse-item>
                     <div
                        class="block rounded-b-lg monserrat-reg bg-transparent border-b border-b-[rgba(255,255,255,0.18)] border-x border-x-[rgba(255,255,255,0.18)]  p-4  dark:bg-neutral-700 dark:text-neutral-50">
                        Some placeholder content for the collapse component. This panel is
                        hidden by default but revealed when the user activates the relevant
                        trigger.
                     </div>
                  </div>
                  <a class="flex justify-between mt-7 py-3 monserrat-reg border-b border-b-[#D434FE]" data-te-collapse-init
                     data-te-ripple-init data-te-ripple-color="light" href="#collapseExample5" role="button"
                     aria-expanded="false" aria-controls="collapseExample5">
                     <div>What happens after the hackathon ends?</div>
                     <div class="text-[#D434FE] text-[20px]">+</div>
                  </a>
                  <div class="!visible hidden" id="collapseExample5" data-te-collapse-item>
                     <div
                        class="block rounded-b-lg monserrat-reg bg-transparent border-b border-b-[rgba(255,255,255,0.18)] border-x border-x-[rgba(255,255,255,0.18)]  p-4  dark:bg-neutral-700 dark:text-neutral-50">
                        Some placeholder content for the collapse component. This panel is
                        hidden by default but revealed when the user activates the relevant
                        trigger.
                     </div>
                  </div>
                  <a class="flex justify-between mt-7 py-3 monserrat-reg border-b border-b-[#D434FE]" data-te-collapse-init
                     data-te-ripple-init data-te-ripple-color="light" href="#collapseExample6" role="button"
                     aria-expanded="false" aria-controls="collapseExample6">
                     <div>Can I work on a project I started before the hackathon?</div>
                     <div class="text-[#D434FE] text-[20px]">+</div>
                  </a>
                  <div class="!visible hidden" id="collapseExample6" data-te-collapse-item>
                     <div
                        class="block rounded-b-lg monserrat-reg bg-transparent border-b border-b-[rgba(255,255,255,0.18)] border-x border-x-[rgba(255,255,255,0.18)]  p-4  dark:bg-neutral-700 dark:text-neutral-50">
                        Some placeholder content for the collapse component. This panel is
                        hidden by default but revealed when the user activates the relevant
                        trigger.
                     </div>
                  </div>
               </div>
               <div class="">
                  <div class="flex justify-center position-contents">
                     <img src="../assets/images/small-question.svg" class="mt-5" />
                     <img src="../assets/images/purplestar.svg" class="scale-star" style="position: relative; left: 20px;" />
                     <img src="../assets/images/big-question.svg" class="mx-12" />
                     <img src="../assets/images/small-question.svg" class="mt-5" />
                  </div>
                  <img src="../assets/images/man-thinking.svg" class="floating-image w-full" />
               </div>
            </div>
         </div>
      </div>


      <div class="">
         <div class="container mx-auto py-[6rem]">
            <div class="text-center">
               <div ref="elementfive">
                  <Typed :options="timelines" v-if="toggleTimelines">
                    <div class="typing clashdisplay-bold text-white text-4xl"></div>
                  </Typed>
                  </div>
               <div class="monserrat-reg text-white mt-5">
                  Here is the breakdown of the time we anticipate<br />
                  using for the upcoming event.
               </div>
            </div>
            <img src="../assets/images/purplestar.svg" class="timeline-purple-star scale-star" />
            <div class="grid grid-cols-12 mt-10 items-end text-white ">
               <div class="hidden md:block md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-right mb-3">Hackathon Announcement</div>
                     <div class="text-right text-white text-sm font-normal font-['Montserrat'] leading-7">The
                        getlinked tech hackathon 1.0 is formally announced<br />to the general public and teams begin to
                        get ready to register</div>
                  </div>
               </div>
               <div class="col-span-2">
                  <div class="relative">
                     <div class="w-[0px] h-[100px] border-2 border-fuchsia-500 mx-auto relative -top-[14px]"></div>
                     <div
                        class="w-[35px] h-[35px] mx-auto bg-gradient-to-l from-purple-600 to-fuchsia-500 rounded-[26.50px] flex justify-center items-center">
                        <div class="text-white text-2xl font-bold font-['Montserrat']">1</div>
                     </div>
                  </div>
               </div>
               <div class="col-span-10 md:col-span-5">
                  <div>
                     <div class="md:hidden">
                        <div class="monserrat-semibold text-[#D434FE] text-left mb-3">Hackathon Announcement</div>
                        <div class="text-left text-white text-sm font-normal font-['Montserrat'] leading-7">The
                           getlinked tech hackathon 1.0 is formally announced<br />to the general public and teams begin to
                           get ready to register</div>
                     </div>
                     <div class="monserrat-semibold text-[#D434FE] text-left mt-3">November 18, 2023</div>
                  </div>
               </div>
            </div>


            <div class="grid grid-cols-12 mt-10 items-end text-white ">
               <div class="hidden md:block md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-right">November 18, 2023</div>
                  </div>
               </div>
               <div class="col-span-2">
                  <div class="relative">
                     <div class="w-[0px] h-[100px] border-2 border-fuchsia-500 mx-auto relative -top-[14px]"></div>
                     <div
                        class="w-[35px] h-[35px] mx-auto bg-gradient-to-l from-purple-600 to-fuchsia-500 rounded-[26.50px] flex justify-center items-center">
                        <div class="text-white text-2xl font-bold font-['Montserrat']">2</div>
                     </div>
                  </div>
               </div>
               <div class="col-span-10 md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-left mb-3">Teams Registration begins</div>
                     <div class="text-left text-white text-sm font-normal font-['Montserrat'] leading-7">Interested teams
                        can now show their interest in the
                        getlinked tech hackathon 1.0 2023 by proceeding to register</div>
                     <div class="md:hidden">
                        <div class="monserrat-semibold text-[#D434FE] text-left mt-3">November 18, 2023</div>
                     </div>
                  </div>
               </div>
            </div>


            <div class="grid grid-cols-12 mt-10 items-end text-white ">
               <div class="hidden md:block md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-right mb-3">Teams Registration ends</div>
                     <div class="text-right text-white text-sm font-normal font-['Montserrat'] leading-7">Interested
                        Participants are no longer Allowed to
                        register</div>
                  </div>
               </div>
               <div class="col-span-2">
                  <div class="relative">
                     <div class="w-[0px] h-[100px] border-2 border-fuchsia-500 mx-auto relative -top-[14px]"></div>
                     <div
                        class="w-[35px] h-[35px] mx-auto bg-gradient-to-l from-purple-600 to-fuchsia-500 rounded-[26.50px] flex justify-center items-center">
                        <div class="text-white text-2xl font-bold font-['Montserrat']">3</div>
                     </div>
                  </div>
               </div>
               <div class="col-span-10 md:col-span-5">
                  <div>
                     <div class="md:hidden">
                        <div class="monserrat-semibold text-[#D434FE] text-left mb-3">Teams Registration ends</div>
                        <div class="text-left text-white text-sm font-normal font-['Montserrat'] leading-7">Interested
                           Participants are no longer Allowed to
                           register</div>
                     </div>
                     <div class="monserrat-semibold text-[#D434FE] text-left mt-3">November 18, 2023</div>
                  </div>
               </div>
            </div>


            <div class="grid grid-cols-12 mt-10 items-end text-white ">
               <div class="hidden md:block md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-right">November 18, 2023</div>
                  </div>
               </div>
               <div class="col-span-2">
                  <div class="relative">
                     <div class="w-[0px] h-[100px] border-2 border-fuchsia-500 mx-auto relative -top-[14px]"></div>
                     <div
                        class="w-[35px] h-[35px] mx-auto bg-gradient-to-l from-purple-600 to-fuchsia-500 rounded-[26.50px] flex justify-center items-center">
                        <div class="text-white text-2xl font-bold font-['Montserrat']">4</div>
                     </div>
                  </div>
               </div>
               <div class="col-span-10 md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-left mb-3">Announcement of the accepted teams
                        and ideas</div>
                     <div class="text-left text-white text-sm font-normal font-['Montserrat'] leading-7">All teams whom
                        idea has been accepted into getlinked tech
                        hackathon 1.0 2023 are formally announced</div>
                     <div class="md:hidden">
                        <div class="monserrat-semibold text-[#D434FE] text-left mt-3">November 18, 2023</div>
                     </div>
                  </div>
               </div>
            </div>



            <div class="grid grid-cols-12 mt-10 items-end text-white">
               <div class="hidden md:block md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-right mb-3">Getlinked Hackathon 1.0 Offically
                        Begins</div>
                     <div class="text-right text-white text-sm font-normal font-['Montserrat'] leading-7">Accepted teams
                        can now proceed to build their
                        ground breaking skill driven solutions</div>
                  </div>
               </div>
               <div class="col-span-2">
                  <div class="relative">
                     <div class="w-[0px] h-[100px] border-2 border-fuchsia-500 mx-auto relative -top-[14px]"></div>
                     <div
                        class="w-[35px] h-[35px] mx-auto bg-gradient-to-l from-purple-600 to-fuchsia-500 rounded-[26.50px] flex justify-center items-center">
                        <div class="text-white text-2xl font-bold font-['Montserrat']">5</div>
                     </div>
                  </div>
               </div>
               <div class="col-span-10 md:col-span-5">
                  <div>
                     <div class="md:hidden">
                        <div class="monserrat-semibold text-[#D434FE] text-left mb-3">Getlinked Hackathon 1.0 Offically
                           Begins</div>
                        <div class="text-left text-white text-sm font-normal font-['Montserrat'] leading-7">Accepted teams
                           can now proceed to build their
                           ground breaking skill driven solutions</div>
                     </div>
                     <div class="monserrat-semibold text-[#D434FE] text-left mt-3">November 18, 2023</div>
                  </div>
               </div>
            </div>


            <div class="grid grid-cols-12 mt-10 items-end text-white ">
               <div class="hidden md:block md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-right">November 18, 2023</div>
                  </div>
               </div>
               <div class="col-span-2">
                  <div class="relative">
                     <div class="w-[0px] h-[100px] border-2 border-fuchsia-500 mx-auto relative -top-[14px]"></div>
                     <div
                        class="w-[35px] h-[35px] mx-auto bg-gradient-to-l from-purple-600 to-fuchsia-500 rounded-[26.50px] flex justify-center items-center">
                        <div class="text-white text-2xl font-bold font-['Montserrat']">6</div>
                     </div>
                  </div>
               </div>
               <div class="col-span-10 md:col-span-5">
                  <div>
                     <div class="monserrat-semibold text-[#D434FE] text-left mb-3">Demo Day</div>
                     <div class="text-left text-white text-sm font-normal font-['Montserrat'] leading-7">Teams get the
                        opportunity to pitch their projects to judges.
                        The winner of the hackathon will also be announced on
                        this day</div>
                     <div class="md:hidden">
                        <div class="monserrat-semibold text-[#D434FE] text-left mt-3">November 18, 2023</div>
                     </div>
                  </div>
               </div>
            </div>
         </div>
      </div>


      <div class="">
         <div class="container mx-auto py-10">
            <div class="grid md:grid-cols-3">
               <div class="md:col-span-2"></div>
               <div class="md:col-span-1">
                  <div ref="elementsix">
                  <Typed :options="rewards" v-if="toggleRewards">
                    <div class="typing clashdisplay-bold text-white text-4xl text-center md:text-left"></div>
                  </Typed>
                  </div>
                  <div class="monserrat-reg text-white leading-7 mt-5 text-center md:text-left">
                     Highlight of the prizes or rewards for winners and<br /> for participants.
                  </div>
               </div>
            </div>
            <div class="grid md:grid-cols-2 gap-10 items-center text-white ">
               <img src="../assets/images/trophy.svg" class="floating-image md:w-3/4 md:mx-auto my-10 md:my-0" />
               <div class="">
                  <img src="../assets/images/Rewards.svg" />
               </div>
            </div>
         </div>
      </div>


      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto py-[6rem]">
            <div class="text-center">
               <div ref="elementseven">
                  <Typed :options="partners" v-if="togglePartners">
                    <div class="typing clashdisplay-bold text-white text-4xl"></div>
                  </Typed>
                  </div>
               <div class="monserrat-reg text-white mt-5">
                  Getlinked Hackathon 1.0 is honored to have the following major
                  companies as its partners and sponsors
               </div>
            </div>
            <!-- <div class="p-10 mt-10 rounded-[5px] border border-fuchsia-500"> -->
            <img src="../assets/images/Partners.svg" class="w-full mt-10" />
            <!-- </div> -->
         </div>
      </div>


      <div class="border-b border-b-[rgba(255,255,255,0.18)]">
         <div class="container mx-auto py-10">
            <div class="grid md:grid-cols-2 gap-10 items-center text-white ">
               <div class="">
                  <div ref="elementeight">
                  <Typed :options="privacy" v-if="togglePrivacy">
                    <div class="typing clashdisplay-bold text-white text-4xl text-center md:text-left"></div>
                  </Typed>
                  </div>
                  <div class="text-opacity-75 text-sm font-normal font-['Montserrat'] leading-7 mt-5">Last updated on
                     September 12, 2023</div>
                  <div class="monserrat-reg text-white leading-7  mt-5 text-center md:text-left mt-8">
                     Below are our privacy & policy, which outline a lot of goodies.
                     it’s our aim to always take of our participant
                  </div>
                  <div class="rounded-[5px] border border-fuchsia-500 p-10 mt-12">
                     <div class="text-white text-sm font-normal font-['Montserrat'] leading-[30.30px] mt-12">At getlinked
                        tech
                        Hackathon 1.0, we value your privacy and are committed to protecting your personal
                        information. This Privacy Policy outlines how we collect, use, disclose, and safeguard
                        your data when you participate in our tech hackathon event. By participating in our event,
                        you consent to the practices described in this policy.</div>
                     <div class="text-fuchsia-500 text-base font-bold font-['Montserrat'] leading-[34.62px] mt-8">Licensing
                        Policy</div>
                     <div class="text-white text-sm font-bold font-['Montserrat'] leading-[30.30px] mt-5">Here are terms of
                        our Standard License:</div>
                     <div class="flex items-start mt-8">
                        <img src="../assets/images/listterms.svg" />
                        <div class="monserrat-reg text-white text-sm ml-5">The Standard License grants you a non-exclusive
                           right to
                           navigate and register for our event</div>
                     </div>
                     <div class="flex items-start mt-8">
                        <img src="../assets/images/listterms.svg" />
                        <div class="monserrat-reg text-white text-sm ml-5">You are licensed to use the item available at
                           any free source
                           sites, for your project developement</div>
                     </div>
                     <div class="flex justify-center">
                        <button type="button" data-te-ripple-init data-te-ripple-color="light"
                           class="monserrat-reg primary-btn mt-10 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                           Read more
                        </button>
                     </div>
                  </div>
               </div>
               <div class="privacypolicy">
                  <img src="../assets/images/security-man.svg" class="floating-image mt-10" />
               </div>
            </div>
         </div>
      </div>
   </div>
   <Footer />
</template>

<script setup>
import { onMounted } from "vue";
import { Typed } from "@duskmoon/vue3-typed-js";
import {
   Collapse,
   Ripple,
   initTE,
} from "tw-elements";


const options = {
   strings: ["getlinked Tech <br /> Hackathon <span class='text-[#D434FE]'>1.0</span>"],
   loop: false,
   typeSpeed: 40,
};

const mantra = {
   strings: ["Igniting a Revolution in HR <div class='inline'>Innovation</div>", "Catalyzing Technology Transformation and <div class='inline'>Innovation</div>", "Farming the Future: Innovate, Tech, <div class='inline'>Lead</div>"],
   loop: true,
   typeSpeed: 40,
};

const introduction = {
    strings: ["Introduction to getlinked <br /><span class='text-[#D434FE]'>tech Hackathon 1.0</span>"],
    loop: false,
    typeSpeed: 20,
};

const rules = {
    strings: ["Rules and <br /><span class='text-[#D434FE]'>Guidelines</span>"],
    loop: false,
    typeSpeed: 20,
};

const judge = {
    strings: ["Judging Criteria <br /><span class='text-[#D434FE]'>Key attributes</span>"],
    loop: false,
    typeSpeed: 20,
};

const questions = {
    strings: ["Frequently Ask<br /><span class='text-[#D434FE]'>Question</span>"],
    loop: false,
    typeSpeed: 20,
};

const timelines = {
    strings: ["Timelines"],
    loop: false,
    typeSpeed: 20,
};

const rewards = {
    strings: ["Prizes and <br /><span class='text-[#D434FE]'>Rewards</span>"],
    loop: false,
    typeSpeed: 20,
};

const partners = {
    strings: ["Partners and Sponsors"],
    loop: false,
    typeSpeed: 20,
};

const privacy = {
    strings: ["Privacy Policy and <br /><span class='text-[#D434FE]'>Terms</span>"],
    loop: false,
    typeSpeed: 20,
};

const hour = ref(4);
const minutes = ref(60);
const seconds = ref(60);
const elementone = ref(null)
const elementtwo = ref(null)
const elementthree = ref(null)
const elementfour = ref(null)
const elementfive = ref(null)
const elementsix = ref(null)
const elementseven = ref(null)
const elementeight = ref(null)
// const { $hello } = useNuxtApp()
const toggleIntroduction = ref(false)
const toggleRules = ref(false)
const toggleJudge = ref(false)
const toggleQuestions = ref(false)
const toggleTimelines = ref(false)
const toggleRewards = ref(false)
const togglePartners = ref(false)
const togglePrivacy = ref(false)

onMounted(() => {
   initTE({ Collapse, Ripple });
   

   setInterval(() => {
      seconds.value -= 1
      // console.log(seconds.value);
      if (seconds.value == 0) {
         seconds.value = 60
         minutes.value -= 1
         if (minutes.value == 59) {
            // minutes.value = 60
            hour.value -= 1
         }
      }
   }, 1000);
})

const reloadpage = (type) => {
    if (type == 1) {
        window.location.href = `${window.location.origin}/register`
    } else {
        window.location.href = `${window.location.origin}/contactus`
    }
}

function isElementVisible(el) {
  const rect = el.getBoundingClientRect();
  return (
    rect.top >= 0 &&
    rect.left >= 0 &&
    rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
    rect.right <= (window.innerWidth || document.documentElement.clientWidth)
    );
  }
  
  function checkElementVisibilityone() {
     let yourElement;
    yourElement = elementone.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
         toggleIntroduction.value = true
   } else {
      // Element is not visible, do something else
      toggleIntroduction.value = false
    }
  }
  
  function checkElementVisibilitytwo() {
     let yourElement;
    yourElement = elementtwo.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      toggleRules.value = true
   } else {
      // Element is not visible, do something else
      toggleRules.value = false
    }
  }

  function checkElementVisibilitythree() {
     let yourElement;
    yourElement = elementthree.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
      toggleJudge.value = true
   } else {
      // Element is not visible, do something else
      toggleJudge.value = false
    }
  }
  
  function checkElementVisibilityfour() {
     let yourElement;
    yourElement = elementfour.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
      toggleQuestions.value = true
   } else {
      // Element is not visible, do something else
      toggleQuestions.value = false
    }
  }
  
  function checkElementVisibilityfive() {
     let yourElement;
    yourElement = elementfive.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
      toggleTimelines.value = true
   } else {
      // Element is not visible, do something else
      toggleTimelines.value = false
    }
  }
  
  function checkElementVisibilitysix() {
     let yourElement;
    yourElement = elementsix.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
      toggleRewards.value = true
   } else {
      // Element is not visible, do something else
      toggleRewards.value = false
    }
  }
 
  function checkElementVisibilityseven() {
     let yourElement;
    yourElement = elementseven.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
      togglePartners.value = true
   } else {
      // Element is not visible, do something else
      togglePartners.value = false
    }
  }
  
  function checkElementVisibilityeight() {
     let yourElement;
    yourElement = elementeight.value
    if (!yourElement) {
      return;
    }
    if (isElementVisible(yourElement)) {
      // Element is visible, do something
      togglePrivacy.value = true
   } else {
      // Element is not visible, do something else
      togglePrivacy.value = false
    }
  }
  
  // Attach the scroll event listener to the window or container
  window.addEventListener('scroll', checkElementVisibilityone);
  window.addEventListener('scroll', checkElementVisibilitytwo);
  window.addEventListener('scroll', checkElementVisibilitythree);
  window.addEventListener('scroll', checkElementVisibilityfour);
  window.addEventListener('scroll', checkElementVisibilityfive);
  window.addEventListener('scroll', checkElementVisibilitysix);
  window.addEventListener('scroll', checkElementVisibilityseven);
  window.addEventListener('scroll', checkElementVisibilityeight);





// const handleScroll = () => { // The main function you want fired by scrolling.
// 	console.log('hello')
// }
// handleScroll()

</script>
