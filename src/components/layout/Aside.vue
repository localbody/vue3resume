<script setup>
import Header from '@/components/Header.vue';
import Quotes from '../UI/Quotes.vue';
import Row from '../UI/Row.vue';
</script>

<template>
    <div class="aside">
        <Header src="/images/photo.jpg" name="Anurag Yadav" alt="Anurag Yadav" />
        <!--  -->
        <Quotes text="A well-organized, creative and goaloriented graduate possessing
        excellent communication, problem-solving and leadership skills with a
        flair to explore Computer Science Engineering" /> 
        <!--  -->
        <hr />
        <!--  -->
        <div class="rows rows--infos">
            <Row icon="/icons/mail.svg" title="Email" :link="{ href: 'mailto:anuragyadavmnp@gmail.com', title: 'anuragyadavmnp@gmail.com' }" />
            <Row icon="/icons/link.svg" title="Website" :link="{ href:'https://anuragyadav365.github.io/portfolio.html', title: 'https://anuragyadav365.github.io/portfolio.html' }" />
            <Row icon="/icons/phone.svg" title="Phone" :link="{ href:'tel:+(+91) 981 5533 309', title: '(+91) 981 5533 309' }" />
            <Row icon="/icons/location.svg" title="Address" :link= "{ title: 'Hallomajra, Chandigarh, India' }" />
        </div>
        <!--  -->
        <hr />
        <!--  -->
        <div class="rows rows--socials">
            <span class="rows__title">Socials</span>
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/instagram.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">Instagram</span>
                    <div class="row__subtitle">
                        <a class="row__link" href="@anurag.yadav.007">@anurag.yadav.007</a>
                    </div>
                </div>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/github.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">Github</span>
                    <div class="row__subtitle">
                        <a class="row__link" href="@anuragyadav365">@anuragyadav365</a>
                    </div>
                </div>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/twitter.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">Twitter</span>
                    <div class="row__subtitle">
                        <a class="row__link" href="@anuragmnp">@anuragmnp</a>
                    </div>
                </div>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/linkdin.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">Linkedin</span>
                    <div class="row__subtitle">
                        <a class="row__link" href="@anuragyadav">@anuragyadav</a>
                    </div>
                </div>
            </div>
        </div>
        <!--  -->
        <hr />
        <div class="rows rows--languages">
            <span class="rows__title"> Languages </span>
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/hindi.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">Hindi</span>
                    <div class="row__subtitle">
                        <span class="row__text">Native</span>
                    </div>
                </div>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/english.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">English</span>
                    <div class="row__subtitle">
                        <span class="row__text">Professional working</span>
                    </div>
                </div>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/spanish.svg" alt="" />
                </div>
                <div class="row__wrapper">
                    <span class="row__title">Spanish</span>
                    <div class="row__subtitle">
                        <span class="row__text">Elementary</span>
                    </div>
                </div>
            </div>
            <!--  -->
        </div>
        <!--  -->
        <hr />
        <!--  -->
        <div class="rows rows--hobbies-interests">
            <span class="rows__title">Hobbies & Interests</span>
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/gaming.svg" alt="" />
                </div>
                <span class="row__subtitle">Gaming</span>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/travelling.svg" alt="" />
                </div>
                <span class="row__subtitle">Travelling</span>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/sketching.svg" alt="" />
                </div>
                <span class="row__subtitle">Sketching/Graffitti</span>
            </div>
            <!--  -->
            <div class="row">
                <div class="row__icon">
                    <img src="/icons/blogging.svg" alt="" />
                </div>
                <span class="row__subtitle">Blogging</span>
            </div>
            <!--  -->
        </div>
    </div>
</template>

<style scoped></style>