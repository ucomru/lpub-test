---
title: Contact
date: 2024-07-20T23:05:30+03:00
draft: false
---

{{< rawhtml >}}

<form id="contact-form" action="https://formspree.io/f/xkgwolez" method="POST">
    <label for="contact-name">Name</label>
    <input type="text" id="contact-name" name="name" required>
    <label for="contact-email">Email</label>
    <input type="email" id="contact-email" name="_replyto" required>
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


{{< rawhtml >}}

<form id="contact-form" name="contact" method="POST" data-netlify="true">
    <label for="contact-name">Name</label>
    <input type="text" id="contact-name" name="name" required>
    <label for="contact-email">Email</label>
    <input type="email" id="contact-email" name="_replyto" required>
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

