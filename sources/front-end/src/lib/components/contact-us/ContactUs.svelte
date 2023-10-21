<style>
  form {
    display: grid;
    grid-template-rows: 1fr 1fr auto 1fr;
    grid-template-areas:
      'title'
      'sub-title'
      'first-name last-name'
      'email subject'
      'message message'
      'submit submit';
    ;
    gap: 1rem;

    & h1 {
      grid-area: title;
    }

    & h2 {
      grid-area: sub-title;
    }

    & div > input[name="first-name"] {
      grid-area: first-name;
    }
  }
</style>

<h1>contact us</h1>
<h2>drop us a line</h2>
<form id="contact-us-form">
    <div>
      <input type="text" name="first-name" />
    </div>
    <div>
      <input type="text" name="last-name" />
    </div>
    <div>
      <input type="email" name="email" />
    </div>
    <div>
      <input type="text" name="subject" />
    </div>
    <div>
      <input type="text" name="message" />
    </div>
    <div>
      <button type="submit">send</button>
    </div>
</form>