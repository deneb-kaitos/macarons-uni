<script>
  import Label from '$lib/controls/Label/Label.svelte';
  import Button from '$lib/controls/Button/Button.svelte';
  import H1 from '$lib/controls/h1/H1.svelte';
</script>
<style>
  form {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr 3fr 1fr;
    grid-template-areas:
      'first-name last-name'
      'email subject'
      'message message'
      'submit submit';
    ;
    gap: 0.5rem;

    & > div {
      display: flex;
      flex-direction: column;
      padding: 0.5rem 0;
    }

    & :is(input[type="text"], input[type="email"], textarea) {
      border: none;
      border-bottom: 1px solid var(--theme-light_gray);
      /* background-color: var(--main-background-color); */
    }


    & .first-name {
      grid-area: first-name;
    }
    & .last-name {
      grid-area: last-name;
    }
    & .email {
      grid-area: email;
    }
    & .subject {
      grid-area: subject;
    }
    & .message {
      grid-area: message;

      & textarea {
        width: 100%;
        height: 100%;
        resize: none;
      }
    }
    & .submit {
      grid-area: submit;
      display: flex;
      justify-content: center;
      align-items: center;
      
      & button[type="submit"] {
        min-width: 8rem;
        cursor: pointer;
      }
    }
  }
</style>

<H1>drop us a line</H1>
<form id="contact-us-form">
    <div class="first-name">
      <Label forElement="first-name-id" text="first name" />
      <input id="first-name-id" type="text" name="first-name" required />
    </div>
    <div class="last-name">
      <Label forElement="last-name-id" text="last name" />
      <input id="last-name-id" type="text" name="last-name" required />
    </div>
    <div class="email">
      <Label forElement="email-id" text="email" />
      <input id="email-id" type="email" name="email" required />
    </div>
    <div class="subject">
      <Label forElement="subject-id" text="subject" />
      <input id="subject-id" type="text" name="subject" required />
    </div>
    <div class="message">
      <Label forElement="message-id" text="message" />
      <textarea id="message-id" name="message" required></textarea>
    </div>
    <div class="submit">
      <Button buttonType="submit" buttonText="submit" />
    </div>
</form>