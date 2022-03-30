---
layout: page
title: Submit
permalink: /submit/
---

Rules: READ ALL DIRECTIONS CAREFULLY

Art to be submitted can be any size howver must be a ratio of 2.5 x 3.5

Image size should not be over 10mb, if so please message (@PepePeddler) before submitting. If you are making a large file for your asset you can make a different display image for the directory.

Issuance must be LOCKED using the lock token function on Counterparty.

No divisible assets.

NSFW is ok when done in an artistic manner with explanation/description included with the asset.

Minimum token supply is 21, no max, (No Burning lower than 21 Please) Physical Art, to be sold with the token, can be issued as 1 of 1's (please contact @PepePeddler directly).

No websites, no QR codes on the cards.

Do not distribute your cards until they are confirmed and live of the website.

Please consider donating btc, xcp or even a card to help support the project, and cover any assosiated fees required to run it.
[bc1qfzfjr4e4wsm97erhdj9lnfaf6jeh4m0vunmsv0](https://xchain.io/address/bc1qfzfjr4e4wsm97erhdj9lnfaf6jeh4m0vunmsv0){:target="_blank"}


*Note: Please make sure your assests are minted before making a submission!*{: .small}

<form
  action="https://usebasin.com/f/1a1d2b97c41f"
  method="POST"
  enctype="multipart/form-data"
  id="my-contact-form"
>
<label for="email">Email <span class="small">(required)</span></label>
<input type="email" name="email" placeholder="john@doe.com" required />
<label for="message">Message <span class="small">(required)</span></label>
<textarea name="message" wrap="hard" required>
name: ASSET_NAME
author: ASSET_AUTHOR
image: https://i.imgur.com/ASSET_IMAGE.jpg
video: https://i.imgur.com/ASSET_VIDEO.mp4 # optional
date: YYYY-MM-DD # mint date
description: A SHORT DESCRIPTION FOR THE SERIES
subs: 
  -
    name: FIRST_SUBASSET_NAME
    image: https://i.imgur/FIRST_SUBASSET_IMAGE.jpg
    supply: FIRST_SUBASSET_SUPPLY 
  -
    name: SECOND_SUBASSET_NAME
    image: https://i.imgur/SECOND_SUBASSET_IMAGE.jpg
    supply: SECOND_SUBASSET_SUPPLY 
</textarea>
<button type="submit" id="form-button">Send</button>
<div id="form-message"></div>
</form>

<script type="text/javascript">
var form = document.getElementById("my-contact-form");
var formMessage = document.getElementById("form-button");
var formButton = document.getElementById("form-button");
form.onsubmit = function(event) {
  event.preventDefault();

  if (confirm("Please make sure your submission is correct and confirm that your tokens are minted on the blockchain!") == true) {
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
