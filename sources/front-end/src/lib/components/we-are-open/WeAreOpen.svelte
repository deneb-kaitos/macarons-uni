<script>
  import {
    FacebookIcon,
    InstagramIcon,
    TwitterIcon,
  } from 'svelte-feather-icons';
  
  let iconSize = "48";
</script>

<style>
  article {
    display: flex;
    flex-direction: column;
    row-gap: 3rem;
  
    & > section {
      display: flex;
      flex-direction: column;
    }

    & > .open-days {
      gap: 1rem;
    }

    & > .open-days > .days-record {
      display: grid;
      grid-template-columns: repeat(2, 1fr) 3fr repeat(2, 1fr);
      grid-template-rows: 1fr;
      grid-template-areas:
        'day-from day-to . time-from time-to'
      ;
      border-bottom: 1px dotted var(--theme-light_gray_bright);

      & > div {
        display: flex;
        align-items: center;
      }

      & > .day-from {
        grid-area: day-from;
      }

      & > .day-to {
        grid-area: day-to;
      }

      & > :is(.day-from, .day-to) {
        justify-content: start;
      }

      & > :is(.time-from, .time-to) {
        justify-content: end;
      }

      & > .time-from {
        grid-area: time-from;
      }

      & > .time-to {
        grid-area: time-to;
      }
    }

    & > .contact-means {
      display: grid;
      grid-template-columns: auto 1fr;
      grid-auto-rows: 1fr;
      gap: 1rem;
      grid-template-areas:
        'phone-caption phone'
        'email-caption email'
      ;

      & > .phone-caption {
        grid-area: phone-caption;
      }

      & > .phone {
        grid-area: phone;
      }

      & > .email-caption {
        grid-area: email-caption;
      }

      & > .email {
        grid-area: email;
      }
    }

    & > .social-networks {
      flex-direction: row;
      column-gap: 0.5rem;
    }
  }
</style>

<article>
  <h1>
    we're open
  </h1>
  <section class="open-days">
    <div class="days-record">
      <div class="day-from">monday</div>
      <div class="day-to">friday</div>
      <div class="day-time-sep" />
      <div class="time-from">11:00</div>
      <div class="time-to">22:00</div>
    </div>
    <div class="days-record">
      <div class="day-from">saturday</div>
      <div class="day-to">sunday</div>
      <div class="day-time-sep" />
      <div class="time-from">11:00</div>
      <div class="time-to">17:00</div>
    </div>
  </section>
  <section class="our-address">
    <span>Some Street 45</span>
    <span>00000, City, Country</span>
  </section>
  <section class="contact-means">
    <div class="phone-caption">tel:</div>
    <a href="tel:0123456789" class="phone" target="_blank">0123456789</a>
    <div class="email-caption">email:</div>
    <a href="mailto:me@mysite.de" class="email" target="_blank">me@mysite.de</a>
  </section>
  <section class="social-networks">
    <a href="https://www.facebook.com/macarons-uni" target="_blank">
      <FacebookIcon size="{iconSize}" />
    </a>
    <a href="https://instagram.com/macarons-uni" target="_blank">
      <InstagramIcon size="{iconSize}" />
    </a>
    <a href="https://twitter.com/macarons-uni" target="_blank">
      <TwitterIcon size="48" />
    </a>
  </section>
</article>