---
title: Contact
date: 2024-07-20T23:05:30+03:00
hideDate: true
draft: false
---

{{< rawhtml >}}

<form id="contact-form" name="contact" method="POST" data-netlify="true" onsubmit="return customizeSubject()">
    <label for="contact-name">Name</label>
    <input type="text" id="contact-name" name="name" maxlength="45" required>
    <label for="contact-email">Email</label>
    <input type="email" id="contact-email" name="_replyto" required>
    <label for="contact-message-subject">Subject</label>
    <input type="text" id="contact-message-subject" name="message-subject" maxlength="60" required>
    <div class="radio-container">
        <label for="contact-radio-message">Message</label>
        <input type="radio" id="contact-radio-message" name="message-type" value="Message" checked>
        <label for="contact-radio--alert">Security Alert</label>
        <input type="radio" id="contact-radio-alert" name="message-type" value="Security Alert">
    </div>
    <textarea id="contact-message" name="message" required></textarea>
    <input type="hidden" id="contact-subject" name="subject">
    <button type="submit" id="contact-submit">Send</button>
</form>

<script>
function customizeSubject() {
    var form = document.getElementById('contact-form');
    var messageSubject = form.querySelector('input[name="message-subject"]').value;
    var messageType = form.querySelector('input[name="message-type"]:checked').value;
    var subject = "Lpub.org " + messageType + ": " + messageSubject;
    var subjectInput = form.querySelector('input[name="subject"]');
    subjectInput.value = subject;
    return true;
}
</script>

{{< /rawhtml >}}

---

If you discover any security vulnerabilities or issues, please select "Security Alert" and 
provide detailed information in the message field. We take all security concerns seriously and 
will address them promptly.
