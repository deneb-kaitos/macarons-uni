<script>
  import {
    FacebookIcon,
    HeartIcon,
    InstagramIcon,
    TwitterIcon,
  } from 'svelte-feather-icons';
  import H1 from '$lib/controls/h1/H1.svelte';
  
  let iconSize = "48";
</script>

<style>
  address {
    display: grid;
    grid-template-columns: auto auto 1rem auto auto;
    grid-auto-rows: 1fr;
    grid-template-areas:
      'title title title title title'
      'first-work-day last-work-day . work-day-start-time work-day-end-time'
      'first-weekend-day last-weekend-day . weekend-start-time weekend-end-time'
      'address address address address address'
      'tel-title . . tel tel'
      'email-title . . email email'
      '. . . . icons'
    ;
    font-style: normal;
    column-gap: 1rem;
    /* row-gap: 1.5rem; */

    & > .align-left {
      justify-content: start;
    }

    & > .align-right {
      justify-content: end;
    }

    & :is(h1, div, a) {
      display: flex;
      align-items: center;
    }

    & div {
      font-variant: all-petite-caps;
    }

    & > h1 {
      grid-area: title;
      justify-content: end;
    }

    & > .first-work-day {
      grid-area: first-work-day;
    }

    & > .last-work-day {
      grid-area: last-work-day;
    }
    
    & > .work-day-start-time {
      grid-area: work-day-start-time;
    }

    & > .work-day-end-time {
      grid-area: work-day-end-time;
    }

    & > .first-weekend-day {
      grid-area: first-weekend-day;
    }

    & > .last-weekend-day {
      grid-area: last-weekend-day;
    }
    
    & > .weekend-start-time {
      grid-area: weekend-start-time;
    }

    & > .weekend-end-time {
      grid-area: weekend-end-time;
    }

    & > .address {
      grid-area: address;
    }

    & > .tel-title {
      grid-area: tel-title;
    }
    
    & > .tel {
      grid-area: tel;
    }

    & > .email-title {
      grid-area: email-title;
    }
    
    & > .email {
      grid-area: email;
    }

    & > .icons {
      grid-area: icons;
      justify-content: space-between;

      & > :is(:visited, :link) {
        color: var(--theme-blue);
      }
    }
  }
</style>

<address>
  <H1>
    we're open
  </H1>
    <div class="first-work-day align-left">monday</div>
    <div class="last-work-day align-left">friday</div>
    <div class="work-day-start-time align-right">11:00</div>
    <div class="work-day-end-time align-right">22:00</div>
    <div class="first-weekend-day align-left">saturday</div>
    <div class="last-weekend-day align-left">sunday</div>
    <div class="weekend-start-time align-right">11:00</div>
    <div class="weekend-end-time align-right">17:00</div>
    <div class="address">
Some Street 45
00000, City, Country
  </div>
  <div class="tel-title align-left">tel</div>
  <a class="tel align-right" href="tel:+012345678910123" target="_blank">+012345678910123</a>
  <div class="email-title align-left">email</div>
  <a class="email align-right" href="mailto:chef@macarons.uni" target="_blank">chef@macarons.uni</a>
  <div class="icons">
    <a class="icon" href="https://www.facebook.com/macarons-uni" target="_blank">
      <FacebookIcon size={iconSize} />
    </a>
    <a class="icon" href="https://instagram.com/macarons-uni" target="_blank">
      <InstagramIcon size={iconSize} />
    </a>
    <a class="icon" href="https://twitter.com/macarons-uni" target="_blank">
      <TwitterIcon size={iconSize} />
    </a>
  </div>
</address>