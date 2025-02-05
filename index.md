---
layout: default # This applies a default Jekyll layout. Customize as needed.
title: Clue2Solve Open Source Projects
---

#

# Welcome to Clue2Solve Open Source Projects

## About Clue2Solve

At Clue2solve, the motto is to build better developer experience. In this mission I have the tremendous pleasure to collaborate with some of the great friends I have made during my technology Journey over years.

You can look for Developer tools, Libraries, Cloud Automation tooling and even some Cloud Strategy related information here at Clue2Solve.

[More to come soon]

## Our Open Source Projects

Here you'll find a list of our open-source projects.

### [Pinecone Unofficial Java Client](pinecone-java-client)

The Pinecone Java Client is an unofficial Java library for interacting with PineconeDB, a vector database ideal for building vector search applications. This client library facilitates operations such as fetching index statistics, querying, and performing upsert and delete operations in PineconeDB.

- Project Home
- Project JavaDocs
- Project Core Contributors ( the Github Repo will always have the full list)

### [Spring Cloud Bedrock Starer](spring-cloud-bedrock-starter)

Lets make the developer experience for Spring and Java developers to use AWS bedrock simple and fun.

- Project Home
- Project JavaDocs
- Project Core Contributors ( the Github Repo will always have the full list)

## Contributing

Information on how to contribute to these projects.

## Contact Us

<form id="contact-form">
  <div class="form-group">
    <label for="name">Name:</label>
    <input
      type="text"
      id="name"
      name="contact_name"
      required
      placeholder="Your name"
    />
  </div>
  <div class="form-group">
    <label for="email">Email:</label>
    <input
      type="email"
      id="email"
      name="contact_email"
      required
      placeholder="Your email"
    />
  </div>
  <div class="form-group">
    <label for="message">Message:</label>
    <textarea
      id="message"
      name="message"
      required
      placeholder="Your message"
    ></textarea>
  </div>
  <button type="submit">Send</button>
</form>
<div id="form-status"></div>

<script
  type="text/javascript"
  src="https://cdn.emailjs.com/dist/email.min.js"
></script>
<script type="text/javascript">
  (function () {
    emailjs.init("AIsPTiYM-CFZwhDWv");
  })();

  const form = document.getElementById("contact-form");

  form.addEventListener("submit", function (event) {
    event.preventDefault();
    document.querySelector('button[type="submit"]').disabled = true;

    emailjs
      .sendForm("service_ryke6bi", "template_apnaww3", form)
      .then(
        function (response) {
          document.getElementById("form-status").innerHTML =
            "<p>Thank you for reaching out! We will get back to you shortly.</p>";
          form.reset();
        },
        function (error) {
          document.getElementById("form-status").innerHTML =
            "<p>Something went wrong, please try again later.</p>";
        }
      )
      .finally(function () {
        document.querySelector('button[type="submit"]').disabled = false;
      });
  });
</script>

<style>
  #contact-form {
    background-color: #f9f9f9;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin: 0 auto;
    width: 100%;
    display: grid;
    gap: 1rem;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

  label {
    display: block;
    font-size: 0.8rem;
    color: #606c71;
    margin-bottom: 5px;
  }

  input[type="text"],
  input[type="email"],
  textarea {
    padding: 10px;
    font-size: 16px;
    border-radius: 8px;
    border: 1px solid #ccc;
    transition: border-color 0.3s;
  }

  textarea {
    height: 150px;
    resize: vertical;
  }

  button[type="submit"] {
    background-color: #159957;
    background-image: linear-gradient(120deg, #155799, #159957);
    padding: 0.75rem 1rem;
    font-size: 16px;
    display: inline-block;
    color: rgba(255, 255, 255, 0.7);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 0.3rem;
    transition: color 0.2s, background-color 0.2s, border-color 0.2s;
    max-width: 15em;
  }

  button[type="submit"]:hover {
    opacity: 0.7;
    cursor: pointer;
  }

  #form-status p {
    margin-top: 10px;
    font-size: 16px;
    color: #159957;
  }
</style>
