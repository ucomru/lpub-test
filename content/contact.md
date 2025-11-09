---
title: Contact
date: 2024-07-20T23:05:30+03:00
hidemeta: true
draft: false
---

{{< rawhtml >}}

<form class="contact-form" name="contact" method="POST" data-netlify="true" netlify-honeypot="bot-field" onsubmit="return customizeSubject()">
  <input type="hidden" name="form-name" value="contact">
  <input type="text" name="bot-field" style="display:none">

  <div class="form-group">
    <label class="form-label" for="name">Name</label>
    <input type="text" id="name" name="name" maxlength="45" required>
  </div>

  <div class="form-group">
    <label class="form-label" for="email">Email</label>
    <input type="email" id="email" name="email" required>
  </div>

  <div class="form-group">
    <label class="form-label" for="message-subject">Subject</label>
    <input type="text" id="message-subject" name="message-subject" maxlength="60" required>
  </div>

  <fieldset>
    <legend class="form-label">Message Type</legend>
    <label><input type="radio" name="message-type" value="Message" checked> Message</label>
    <label><input type="radio" name="message-type" value="Security Alert"> Security Alert</label>
  </fieldset>

  <div class="form-group">
    <label class="form-label" for="message">Message</label>
    <textarea id="message" name="message" required></textarea>
  </div>

  <input type="hidden" id="final-subject" name="subject">

  <button type="submit">Send</button>
</form>

<script>
function customizeSubject() {
    const form = document.forms['contact'];
    const subjectInput = form.querySelector('input[name="subject"]');
    const subject = `Lpub.org ${form["message-type"].value}: ${form["message-subject"].value}`;
    subjectInput.value = subject;
    return true;
}
</script>

{{< /rawhtml >}}

---

If you discover any vulnerabilities or security issues, please choose “Security Alert” above and describe the issue in detail. We take all reports seriously.

---
---

{{< rawhtml >}}

<p>If you have any questions or concerns, feel free to <a href="#" id="email-link">write us</a></p>

<script>
(function(){
    const user = "test_addr";
    const domain = "lpub.org";
    const link = document.getElementById("email-link");
    link.setAttribute("href", "mailto:" + user + "@" + domain);
    link.textContent = user + "@" + domain;
})();
</script>

<noscript>
  <p><em>[Enable JavaScript to view]</em></p>
</noscript>

{{< /rawhtml >}}

---
