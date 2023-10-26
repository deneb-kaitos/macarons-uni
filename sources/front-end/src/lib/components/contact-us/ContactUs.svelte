<style>
h1 {
  padding: 1rem 0;
}

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
      background-color: var(--main-background-color);
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

<h1>drop us a line</h1>
<!-- <h2>drop us a line</h2> -->
<form id="contact-us-form">
    <div class="first-name">
      <label for="first-name-id">first name</label>
      <input id="first-name-id" type="text" name="first-name" required />
    </div>
    <div class="last-name">
      <label for="last-name-id">last name</label>
      <input id="last-name-id" type="text" name="last-name" required />
    </div>
    <div class="email">
      <label for="email-id">email</label>
      <input id="email-id" type="email" name="email" required />
    </div>
    <div class="subject">
      <label for="subject-id">subject</label>
      <input id="subject-id" type="text" name="subject" required />
    </div>
    <div class="message">
      <label for="message-id">message</label>
      <textarea id="message-id" name="message" required></textarea>
    </div>
    <div class="submit">
      <button type="submit">send</button>
    </div>
</form>