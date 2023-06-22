---
layout: page
title: Contact
permalink: /contact/
---


Feel free to reach out with any comments or questions!

<form id="contact-form">
  <div class="mb-3">
    <label for="name" class="form-label">Name</label>
    <input type="text" class="form-control" id="name" name="entry.1961653833" required>
  </div>
  <div class="mb-3">
    <label for="email" class="form-label">Email</label>
    <input type="email" class="form-control" id="email" name="entry.259415346" required>
  </div>
  <div class="mb-3">
    <label for="message" class="form-label">Message</label>
    <textarea class="form-control" id="comment" name="entry.807267372" rows="5" required></textarea>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

<script>
    document.querySelector("#contact-form").addEventListener("submit", function(e) {
    e.preventDefault();

    var formData = new FormData(this);
    var formParams = new URLSearchParams(formData).toString();

    fetch("https://docs.google.com/forms/d/e/1FAIpQLSdiepBkUJxCkN1n-QNKlR6LR7OvJACo4F-HuBjQ4WobhmjEOA/viewform?usp=sf_link", {
        method: "POST",
        body: formParams,
        headers: {
        "Content-Type": "application/x-www-form-urlencoded"
        }
    })
    .then(function(response) {
        if (response.ok) {
        // Handle successful form submission
        console.log("Form submitted successfully");
        } else {
        // Handle form submission error
        console.error("Error submitting form");
        }
    })
    .catch(function(error) {
        // Handle network or other errors
        console.error("Error submitting form", error);
    });
    });
</script>