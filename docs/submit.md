---
layout: page
title: Submit
permalink: /submit/
---

PLEASE READ CAREFULLY

Canvas & File Sizes:
- It's your canvas, so it can be any size.
- No limit - All images on the site are loaded via url. (10mb is on the larger side, but you can always host a smaller file for use on the site if needed)

Supply & Submission:
- Min Supply of 21
- Issuance must be LOCKED
- No websites or QR codes
- 1 Sumbission at a time please (its only me at the moment)

Guidelines:
- NSFW is fine, if done in an artistic manner with explanation/description included with the asset.
- Burning supplies is fine, we just ask for no burning lower than 21 to respect the collection community and other artists

Required to submit:
- It's free.
- No token burn required, instead all successfull submissions donate a card (this will also prevent any assests being burned to 1). Plus in return you will recieve the RAREBTCART Series 1 Card l only be obtainable and distributed to artists.

Physical Art:
- If you want to make a Physical Piece, it can be issued as a 1 of 1 with official copies or "prints" being issued as subassests Please contact us at support@rarebtc.art


*Cards must NOT be distributed before they are confirmed and live of the website. Any distribution prior to this will result in the work not being added to the collection.

<form
  action="https://usebasin.com/f/17f8ff352369"
  method="POST"
  enctype="multipart/form-data"
  id="submisions"
>
<label for="email">Email <span class="small">(required)</span></label>
<input type="email" name="email" placeholder="john@doe.com" required />
<label for="text">Artist name <span class="small">(required)</span></label>
<input type="text" name="Artist Name" />
<label for="text">Xchain Asset Link <span class="small">(required)</span></label>
<input type="text" name="Asset Link" />
<label for="text">Image/GIF URL <span class="small">(required)</span></label>
<input type="text" name="Image/GIF URL" />
<label for="text">MP4 URL <span class="small">(not required)</span></label>
<input type="text" name="MP4 URL" />
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
