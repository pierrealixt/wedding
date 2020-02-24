<template>
  <div style='height:100%;'>
    <CairoSun></CairoSun>
    <div class='section section1 bg-green'>
      <MyWeirdText
        text='Tremblay Wedding'
        css='title'></MyWeirdText>
      
      <MyText
        v-bind:text="{
          line1: 'We are so excited',
          line2: 'to celebrate with you'
        }"
        css='intro'></MyText>

      <img 
        src='../assets/arrow_down.png' 
        class='arrow-down'
        alt='arrow down'
        v-on:click='clickArrowDown' />
    </div>

    <div id='section2' class='section section2 bg-yellow'>
      <p class='title'></p>
      <div class='day'>
        <MyWeirdText
          text='08 August'
          css='date'></MyWeirdText>
        <MyText
          v-bind:text="{
            line1: 'Wedding Party'
          }"
          css='activity'>
        </MyText>
        <ActivityDetails
          time='10:30am'
          location='Zeekovlei Yacht Club, Governors Walk, Cape Town'
          dresscode='Dressy Casual'
          notes='All food and drinks will be supplied. Families can get home by bedtime and the rest can party till the venue closes at 12ish.'>
        </ActivityDetails>
      </div>

      <hr />

      <div class='day'>
        <MyWeirdText
          text='09 August'
          css='date'></MyWeirdText>
        <MyText
          v-bind:text="{
            line1: 'Brunch (optional)'
          }"
          css='activity'>
        </MyText>
        <ActivityDetails
          time='09:00am'
          location="Tiger's Milk Restaurant, Sidmouth Road, Muizenberg"
          dresscode='Casual'
          notes='We ask guests to please bring <b>R150 cash</b> for your brunch. Please RSVP ASAP.'>
        </ActivityDetails>

        <MyButton
          text='RSVP'
          link='https://forms.gle/w6gPJRhQYKSospVw6'
          css='buttonrsvp'></MyButton>
      </div>

      <hr />

      <div class='day'>
        <MyWeirdText
          text='10 August'
          css='date'></MyWeirdText>
        <MyText
          v-bind:text="{
            line1: 'Hike (optional/weather dependant)'
          }"
          css='activity'>
        </MyText>
        <ActivityDetails
          time='08:00am'
          location="Lion's Head Hiking Trail, Signal Hill Road, Cape Town"
          dresscode='Active Wear'
          notes='This hike is for beginner fitness levels (aprox. 2h up and down). Be sure to pack water and snacks.'>
        </ActivityDetails>
      </div>


    </div>

    <div class='section section3 bg-green'>
      <MyWeirdText
        text='Accomodation'
        css='title'></MyWeirdText>
      <p class='content'>
        It would be rad if you found a place to stay in or around the town we live and LOVE: <b>Muizenberg</b>
      </p>
      <p class='content'>
        There are plenty of hosts and guesthouses around the area, even better try <a href='https://airbnb.com' target='_blank'>AirBnB</a>.
      </p>
      <p class='content'>
        Unfortunately we cannot host anyone at our place over this time.
      </p>

      <img 
        src='../assets/muizenberg.png' 
        class=''
        alt='Muizenberg, Cape Town' />
    </div>

    <div class='section section4 bg-yellow'>
      <MyWeirdText
        text='Wedding Registry'
        css='title'></MyWeirdText>

      <p class='content'>
        If you are coming from afar, please don’t stress about gifts, we understand that flights are very expensive and our most precious gift is celebrating with you.
      </p>
      <p class='content'>
        If you do want to gift us, please see our registry here.
        <MyButton
          text='Gift wishlist'
          link='https://docs.google.com/spreadsheets/d/1sm79c2q0Mn0-2Itq7b323p2NdpjLwv01eTByuBIfDGQ/edit?usp=sharing'
          css='buttonrsvp'></MyButton>
      </p>
    </div>

    <div class='section section5 bg-green'>
      <MyWeirdText
        text='Thank You'
        css='title'></MyWeirdText>
      <p class='content' style='font-size:24px'>
        For being in our lives.
      </p>
      <img 
        src='../assets/thankyou.png' 
        class='thankyou'
        alt='Thank you' />
      <p class='content'>
        We LOVE you and can’t wait to celebrate with you.
        <br />
        Have any Questions? Contact us, you know how;)
      </p>
      <p class='content'>
        xx PA & Carina
      </p>
    </div>
  </div>


</template>


<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import CairoSun from '@/components/CairoSun.vue';
import MyWeirdText from '@/components/MyWeirdText.vue';
import MyText from '@/components/Text.vue';
import ActivityDetails from '@/components/ActivityDetails.vue';
import MyButton from '@/components/MyButton.vue';


@Component({
  components: {
    CairoSun,
    MyWeirdText,
    MyText,
    ActivityDetails,
    MyButton,
  },
})

export default class About extends Vue {
  clickArrowDown() {
    location.href = '#';
    location.href = '#section2';
    location.href = '#information';
  }

// element.scrollTo({
//   top: 100,
//   left: 100,
//   behavior: 'smooth'
// });

// https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView
}
</script>

<style lang="scss">
.section {
  height: 100%;
}
.bg-green {
  background: #C2CCA2;
}

.bg-yellow {
  background: #FFE186;
}

h2 {
  margin-top: 0;
}

.title {
  p {
    font-size: 60px;
    color: #575757;
    text-transform: none;

    @media (min-width: 320px) and (max-width: 480px) {
      font-size: 42px;
    }
  }
}

p.content {
  width: 543px;
  margin: 20px auto;
  display: block;
  text-align: center;
  color: #181818;
  line-height: 20px;
  font-size: 16px;
  letter-spacing: 2.3px;
  text-transform: none;
  @media (min-width: 320px) and (max-width: 480px) {
    width: auto;
  }
}

.section1 {
  .title {
    padding-top: 25%;
  }
  .intro {
    p {
      font-size: 24px;
      line-height: 28px;
      text-align: center;
      color: #181818;
      @media (min-width: 320px) and (max-width: 480px) {
        font-size: 20px;
        margin-top: 20px;
      }
    }

  }

  .arrow-down {
    margin-top: 100px;
    cursor: pointer;
  }
}

.section2 {
  @media (min-width: 320px) and (max-width: 480px) {
    height: auto;
  }

  hr {
    display: none;

    @media (min-width: 320px) and (max-width: 480px) {
      display: block;
      width: 50px;
      border: 1px solid #181818;
      margin: 20px auto;
    }

  }
  .title {
    padding-top: 10%;
  }

  .day {
    float: left;
    width: 33%;
    @media (min-width: 320px) and (max-width: 480px) {
      width: 100%;
      float: none;
    }

    .buttonrsvp {
      @media (min-width: 320px) and (max-width: 480px) {
        margin-top: 2vh;
        margin-bottom: 3vh;
      }
    }
  }

  .date {
    p {
      font-size: 48px;
      line-height: 61px;
      text-align: center;
      letter-spacing: 5.42667px;
      color: #575757;
      text-transform: none;
    }
  }

  .activity {
    p {
      font-size: 16px;
      line-height: 19px;
      text-align: center;
      letter-spacing: 2.31111px;
      color: #181818;
      padding-top: 30px;
      text-transform: none;
    }
  }
}

.section3 {
  .title {
    padding-top: 15%;
  }

}

.section4 {
  .title {
    padding-top: 15%;
  }
}

.section5 {
  .title {
    padding-top: 5%;
  }
  img {
    @media (min-width: 320px) and (max-width: 480px) {
      width: 320px;
      margin: 0 auto;
    }
}

}


</style>

