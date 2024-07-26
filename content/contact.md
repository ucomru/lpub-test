---
title: Contact
date: 2024-07-20T23:05:30+03:00
draft: false
---


## simple


{{< rawhtml >}}

<form id="contact-form" name="contact" method="POST" data-netlify="true">
    <label for="contact-name">Name</label>
    <input type="text" id="contact-name" name="name" required>
    <label for="contact-email">Email</label>
    <input type="email" id="contact-email" name="_replyto" required>
    <label for="contact-subject">Subject</label>
    <input type="text" id="contact-subject" name="subject" maxlength="60" required>
    <div class="radio-container">
        <input type="radio" id="message" name="message-type" value="Message" checked>
        <label for="message">Message</label>
        <input type="radio" id="security-alert" name="message-type" value="Security Alert">
        <label for="security-alert">Security Alert</label>
    </div>
    <textarea id="contact-message" name="message" required></textarea>
    <button type="submit" id="contact-submit">Send</button>
</form>

{{< /rawhtml >}}


---
---


## with JS


{{< rawhtml >}}

<form id="contact-form" name="contact" method="POST" data-netlify="true" onsubmit="return customizeSubject()">
    <label for="contact-name">Name</label>
    <input type="text" id="contact-name" name="name" maxlength="45" required>
    <label for="contact-email">Email</label>
    <input type="email" id="contact-email" name="_replyto" required>
    <label for="contact-subject">Subject</label>
    <input type="text" id="contact-subject" name="message-subject" maxlength="60" required>
    <div class="radio-container">
        <input type="radio" id="message" name="message-type" value="Message" checked>
        <label for="message">Message</label>
        <input type="radio" id="security-alert" name="message-type" value="Security Alert">
        <label for="security-alert">Security Alert</label>
    </div>
    <label for="contact-message">Message</label>
    <textarea id="contact-message" name="message" required></textarea>
    <button type="submit" id="contact-submit">Send</button>
</form>

<script>
function customizeSubject() {
    var form = document.getElementById('contact-form');
    var messageType = form.querySelector('input[name="message-type"]:checked').value;
    var messageSubject = form.querySelector('input[name="message-subject"]').value;
    var subject = "Lpub.org " + messageType + ": " + messageSubject;
    var subjectInput = document.createElement('input');
    subjectInput.type = 'hidden';
    subjectInput.name = 'subject';
    subjectInput.value = subject;
    form.appendChild(subjectInput);
    return true;
}
</script>

{{< /rawhtml >}}

