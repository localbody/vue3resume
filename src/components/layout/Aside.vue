<script>
import Header from '@/components/Header.vue'
import Quotes from '../UI/Quotes.vue'
import Row from '../UI/Row.vue'

export default {
  name: 'Aside',
  data() {
    return {
      itemsRows: {
        infos: [
          {
            icon: '/icons/mail.svg',
            title: 'Email',
            link: {
              href: 'mailto:anuragyadavmnp@gmail.com',
              title: 'anuragyadavmnp@gmail.com',
            },
          },
          {
            icon: '/icons/link.svg',
            title: 'Website',
            link: {
              href: 'https://anuragyadav365.github.io/portfolio.html',
              title: 'https://anuragyadav365.github.io/portfolio.html',
            },
          },
          {
            icon: '/icons/phone.svg',
            title: 'Phone',
            link: {
              href: 'tel:+(+91) 981 5533 309',
              title: '(+91) 981 5533 309',
            },
          },
          {
            icon: '/icons/location.svg',
            title: 'Address',
            link: { title: 'Hallomajra, Chandigarh, India' },
          },
        ],

        socials: [
          {
            icon: '/icons/instagram.svg',
            title: 'Instagram',
            link: {
              href: 'https://www.instagram.com/anurag.yadav.007/',
              title: '@anurag.yadav.007',
            },
          },
          {
            icon: '/icons/github.svg',
            title: 'Github',
            link: {
              href: 'https://github.com/AnuragYadav365',
              title: '@anuragyadav365',
            },
          },
          {
            icon: '/icons/twitter.svg',
            title: 'Twitter',
            link: {
              href: 'https://x.com/anuragmnp',
              title: '@anuragmnp',
            },
          },
          {
            icon: '/icons/linkdin.svg',
            title: 'Linkedin',
            link: {
              href: 'https://x.com/anuragmnp',
              title: '@anuragyadav',
            },
          },
        ],

        languages: [
          {
            icon: '/icons/hindi.svg',
            title: 'Hindi',
            link: {
              title: 'Native',
            },
          },
          {
            icon: '/icons/english.svg',
            title: 'English',
            link: {
              title: 'Professional working',
            },
          },
          {
            icon: '/icons/spanish.svg',
            title: 'Spanish',
            link: {
              title: 'Elementary',
            },
          },
        ],

        hobbies_interests: [
          {
            icon: '/icons/gaming.svg',
            title: 'Gaming',
          },
          {
            icon: '/icons/travelling.svg',
            title: 'Travelling',
          },
          {
            icon: '/icons/sketching.svg',
            title: 'Sketching',
          },
          {
            icon: '/icons/blogging.svg',
            title: 'Blogging',
          },
        ],
      },
    }
  },
  components: {
    Header,
    Quotes,
    Row,
  },
}
</script>

<template>
  <div class="aside">
    <Header photo="/images/photo.jpg" name="Anurag Yadav" />
    <Quotes
      text="A well-organized, creative and goaloriented graduate possessing
        excellent communication, problem-solving and leadership skills with a
        flair to explore Computer Science Engineering"
    />
    <hr />
    <div class="rows rows--infos">
      <div class="rows-wrapper">
        <Row
          v-for="(item, index) in itemsRows.infos"
          :row="item"
          :key="index"
        />
      </div>
    </div>
    <hr />
    <div class="rows rows--socials">
      <div class="rows-wrapper">
        <span class="rows__title">Socials</span>
        <Row
          v-for="(item, index) in itemsRows.socials"
          :row="item"
          :key="index"
        />
      </div>
    </div>
    <hr />
    <div class="rows rows--languages">
      <div class="rows-wrapper">
        <span class="rows__title"> Languages </span>

        <Row
          v-for="(item, index) in itemsRows.languages"
          :row="item"
          :key="index"
        />
      </div>
    </div>
    <hr />
    <div class="rows rows--hobbies-interests">
      <div class="rows-wrapper">
        <span class="rows__title">Hobbies & Interests</span>
        <Row
          v-for="(item, index) in itemsRows.hobbies_interests"
          :row="item"
          :key="index"
        />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
