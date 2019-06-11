---
title: Contact Me
section_position: "sidebar"
form:
    name: contact-form
    fields:
        - name: bee
          type: honeypot

        - name: name
          label: Name
          placeholder: Enter your name
          autofocus: on
          autocomplete: on
          type: text
          validate:
            required: true

        - name: email
          label: Email
          placeholder: Enter your email address
          type: email
          validate:
            required: true
        
        - name: message
          label: Message
          type: textarea
          validate:
            required: true

    buttons:
        - type: submit
          value: Submit

    process:
        - email:
            from: "{{ config.plugins.email.from }}"
            to: "{{ config.plugins.email.to }}"
            subject: "[Contact from cv.marvinroman.me] {{ form.value.name|e }}"
            body: "{% include 'forms/data.html.twig' %}"
        - save:
            fileprefix: feedback-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        - message: Message received!

---

Let me know what I can do for you.