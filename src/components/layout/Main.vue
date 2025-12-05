<script>
import Education from '@/components/cards/Education.vue'
import Experience from '@/components/cards/Experience.vue'
import Skill from '@/components/cards/Skill.vue'
import Project from '@/components/cards/Project.vue'
import Award from '@/components/cards/Award.vue'

export default {
  name: 'Main',
  data() {
    return {
      cards: {
        education: [
          {
            image: '/images/chandigarh_university.png',
            name: 'Chandigarh University',
            title: 'Bachelor in Computer Science Engineering',
            subtitle: '2020 - 2024',
            percentage: '- 9 CGPA',
          },
          {
            image: '/images/suditi_global_academy.png',
            name: 'Suditi Global Academy',
            title: 'Intermediate XI - XII (CBSE)',
            subtitle: '2018-2020',
            percentage: '- 85%',
          },
          {
            image: '/images/akanksha_global_acadmey.png',
            name: 'Akanksha Global Acadmey',
            title: 'High School IX - X (CBSE)',
            subtitle: '2016-2018',
            percentage: '- 92%',
          },
        ],
        experience: [
          {
            date: 'Present',
            location: 'Chandigarh',
            image: '/images/alexa.png',
            role: 'Graphic Designer',
            name: 'Alexa Dev Community',
            description: `Creatively Designing and Developing web UI for Chandigarh University’s Alexa Developer Community, upcoming big launch of full website.`,
          },
          {
            date: 'Oct 2021 - Nov 2021',
            location: 'Online',
            image: '/images/github.png',
            role: 'Hacktoberfest Contributor',
            name: 'Github',
            description: `Contributed 8 PR’s in various open source projects. Great experience and learning alot about working with Github and open-source. Connecting with developers`,
          },
          {
            date: 'Jan 2021 - March 2021',
            location: 'Online',
            image: '/images/winter_of_code.png',
            role: 'Contributor',
            name: 'Winter of Code',
            description: `Overwhelming to be a part of DSC NSEC project - DSC NSEC Algorithms for Winter of Code 2020. First introduction to Git and Github. How github is used by most of the programmers in order to manage the projects.`,
          },
          {
            date: 'Oct 2020 - Dec 2020',
            location: 'Online',
            image: '/images/google.png',
            role: '30Days of Google Cloud',
            name: 'Google',
            description: `Hands on practice on Google Cloud Platform - the tool that powers apps like Google Search, Gmail and YouTube. As part of the program had learned the concepts like computing, application development, big data & machine learning using cloud.`,
          },
        ],
        skill: [
          {
            isBigCard: true,
            image: '/images/figma.png',
            title: 'Figma',
            subtitle: 'Web UI Design, Prototyping',
          },
          {
            isBigCard: true,
            image: '/images/java.png',
            title: 'Java',
            subtitle: 'Software Development',
          },
          {
            isBigCard: true,
            image: '/images/python.png',
            title: 'Python',
            subtitle: 'Design workspace',
          },
          {
            isBigCard: false,
            image: '/images/html.png',
            title: 'HTML 5',
            subtitle: 'Structural Design',
          },
          {
            isBigCard: false,
            image: '/images/css.png',
            title: 'CSS 3',
            subtitle: 'Style Design',
          },
          {
            isBigCard: false,
            image: '/images/wordpress.png',
            title: 'Wordpress',
            subtitle: 'Web development',
          },
          {
            isBigCard: false,
            image: '/images/vscode.png',
            title: 'VS Code',
            subtitle: 'Code editor',
          },
          {
            isBigCard: false,
            image: '/images/notion.png',
            title: 'Notion',
            subtitle: 'Project management',
          },
        ],
        project: [
          {
            image: '/images/figma.png',
            name: 'Alexa Dev Community Landing Page',
            description: 'Web UI design for alexa developers comunity',
            logo: '/icons/figma--blue.svg',
            link: { url: 'https://figma.com', anchor: 'https://figma.com' },
          },
          {
            image: '/images/lighting.png',
            name: 'Portfolio Webpage',
            description: 'Personal Portfolio webpage with resume and blog',
            logo: '/icons/link--blue.svg',
            link: {
              url: 'https://anuragyadav365.github.io',
              anchor: 'https://anuragyadav365.github.io',
            },
          },
        ],
        award: [
          {
            image: '/images/responsive_web_design.png',
            title: 'freeCodeCamp',
            subtitle: 'Responsive Web Design',
            dates: 'Dec 2021 - Feb 2022',
          },
          {
            image: '/images/google.png',
            title: 'Data Structure & Algorithms',
            subtitle: 'Google',
            dates: 'Mar 2021 - Jun 2021',
          },
        ],
      },
    }
  },
  components: {
    Education,
    Experience,
    Skill,
    Project,
    Award,
  },
}
</script>

<template>
  <div class="main">
    <div class="sections">
      <div class="section">
        <div class="section__title">Education</div>
        <div class="section_content">
          <div class="cards cards--education">
            <Education
              v-for="(item, index) in cards.education"
              :key="index"
              :image="item.image"
              :name="item.name"
              :title="item.title"
              :subtitle="item.subtitle"
              :percentage="item.percentage"
            />
          </div>
        </div>
      </div>
      <!-- end education -->
      <div class="section">
        <div class="section__title">Achievements</div>
        <div class="section__content">
          <div class="experiences">
            <Experience
              v-for="(item, index) in cards.experience"
              :key="index"
              :experience="item"
            />
          </div>
        </div>
      </div>
      <!-- end  experiences -->
      <div class="section">
        <div class="section__title">Tools/Skills</div>
        <div class="section__content">
          <div class="cards skills cards--skills">
            <Skill
              v-for="{ isBigCard, image, title, subtitle } in cards.skill"
              :key="title"
              :isBigCard
              :image
              :title
              :subtitle
            />
          </div>
        </div>
      </div>
      <!-- end tools/skills -->
      <div class="section">
        <div class="section__title">Latest projects</div>
        <div class="section__content">
          <div class="cards cards--projects">
            <Project
              v-for="{ image, name, description, logo, link } in cards.project"
              :key="name"
              :image
              :name
              :description
              :logo
              :link
            />
          </div>
        </div>
      </div>
      <!-- end latest projects -->
      <div class="section">
        <div class="section__title">Certificates & Awards</div>
        <div class="section__content">
          <div class="cards cards--certificates">
            <Award
              v-for="{ image, title, subtitle, dates } in cards.award"
              :key="title"
              :image
              :title
              :subtitle
              :dates
            />
          </div>
        </div>
      </div>
      <!-- end awards -->
    </div>
  </div>
</template>

<style scoped></style>
