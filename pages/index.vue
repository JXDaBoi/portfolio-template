<template>
  <div class="flex flex-col w-screen h-full">
    <!-- Your name, profile picture and contact -->
    <HeadWrapper
      name="JXDaBoi"
      title="Just a Uni Student"
      userImgURL="../img/Goddess.jpg"
      phone="+60102292811"
      email="jingxiangdaboi@gmail.com"
    />
    <!-- About Me -->
    <AboutWrapper
      aboutMe="Just a normal university student that is alone :'("
      linkedInURL="NA"
      languages="Chinese, English"
      nationality="Malaysian"
      interest="Badminton, Games :)"
    />
    <!-- Working Experience -->
    <CareerWrapper>
      <template v-slot:career>
        <Career companyName="XMUM" title="Degree Student" startDate="Feb 2020" endDate="NA">
          <!-- List of what you had did in the company -->
          <template v-slot:experience>
            <ul class="text-gray-600 list-inside list-disc mt-2 px-4">
              <li>DMT Student</li>
              <li>Learning languagues such as C/C++, Java, Python and Ruby</li>
            </ul>
          </template>
        </Career>
      </template>
    </CareerWrapper>
    <!-- Achievement -->
    <AchievementWrapper project="5" client="5" award="2"/>
    <!-- Portfolio -->
    <PortfolioWrapper>
      <template v-slot:portfolio>
        <div class="grid grid-cols-1 md:grid-cols-3">
          <ProjectCard
            imgUrl="../img/github.png"
            name="Guild Plugin"
            project="Minecraft Plugin"
            projectURL="https://github.com"
          />
        </div>
      </template>
    </PortfolioWrapper>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "A Normal Website"
    };
  }
};
</script>