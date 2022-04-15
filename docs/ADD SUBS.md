---
layout: page
title: Add Sub Assests
permalink: /add-subs/
---

PLEASE READ CAREFULLY

Use your subassests to expand your work, create a sub collection, a multi panel piece, Allow other artist to create iterations or make your main assest a grail block for art drops. It's completely up to you how you use the subassests associated to your work.


Subassests are added manually to the site, so please allow some time for updates to show.

- Sub asset name (ASSET.SUBNAME)
- Image link
- Supply
- Artist (if another artist) 


<form
  action="https://usebasin.com/f/1420aab1fcd8"
  method="POST"
  enctype="multipart/form-data"
  id="add-subs"
>
<label for="email">Email <span class="small">(required)</span></label>
<input type="email" name="email" placeholder="john@doe.com" required />
<label for="text">Artist name <span class="small">(required)</span></label>
<input type="text" name="Artist Name" />
<label for="text">Xchain Asset Link <span class="small">(required)</span></label>
<input type="text" name="Asset Link" />
<label for="text">Image/GIF URL <span class="small">(required)</span></label>
<input type="text" name="Image/GIF URL" />
<label for="text">Supply <span class="small">(required)</span></label>
<input type="text" name="Token Supply" />
<button type="submit" id="form-button">Send</button>
<div id="form-message"></div>
</form>

<script type="text/javascript">
var form = document.getElementById("my-contact-form");
var formMessage = document.getElementById("form-button");
var formButton = document.getElementById("form-button");
form.onsubmit = function(event) {
  event.preventDefault();

  if (confirm("Please make sure your submission is correct") == true) {
    formMessage.innerHTML = "Sending...";
    formMessage.disabled = true;
    var formData = new FormData(form);
    var xhr = new XMLHttpRequest();
    xhr.open("POST", form.action, true);
    xhr.onload = function(e) {
      console.log(xhr);
      if (xhr.status === 200) {
        formMessage.innerHTML = "Thank you!";
      } else {
        formMessage.innerHTML = "Please try again!"
        formMessage.disabled = false;
      }
    };
    xhr.send(formData);
  }
};
</script>
