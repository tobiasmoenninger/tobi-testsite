---
layout: default
title: Contact
permalink: /contact/
---
<section class="page-section">
  <div class="page-inner narrow">
    <header class="page-header">
      <p class="page-kicker">Contact</p>
      <h1>Get in touch</h1>
    </header>

    <p class="contact-lead">
      For project inquiries, collaborations, or just to say hello — drop a message below
      or reach out on <a href="{{ site.social.linkedin }}">LinkedIn</a>.
    </p>

    <form action="https://formspree.io/f/{{ site.formspree_id }}" method="POST" class="contact-form">
      <div class="form-row">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" required>
      </div>
      <div class="form-row">
        <label for="email">Email</label>
        <input type="email" id="email" name="email" required>
      </div>
      <div class="form-row">
        <label for="message">Message</label>
        <textarea id="message" name="message" rows="6" required></textarea>
      </div>
      <button type="submit" class="btn">Send message</button>
    </form>
  </div>
</section>
