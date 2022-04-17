---
layout: page
title: Submit
permalink: /submit/
---

PLEASE READ CAREFULLY BEFORE SUBMITTING:

Canvas & File Sizes:
- It's your canvas, no more trimming!
- If you can keep file sizes for the site to a minimum whilst preserving the details 10mb is fine.

Supply & Submission:
- Min Supply of 21
- Issuance must be LOCKED
- No direct website links

Guidelines:
- NSFW is fine, if done in an artistic manner with a good explanation/description included.
- No burning lower than 21 to respect the collection community and other artists.

Required to submit:
- Currently there is no token burn required. Instead artist are asked to contribute/participate in the community evolving art piece: THETIMESNEWS - <a href="https://rarebtc.art/comcard/">Click Here</a>

<img src="https://bafybeid56ngwqopaj2afzil5ohdqligfcsz65rqccmxocidrfkzcw44tsy.ipfs.nftstorage.link/" max-width="100%" height="auto">

*Blocks MUST NOT be distributed before they are confirmed and live on the website. Any distribution prior to this will result in the work not being added to the collection.

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
<label for="message">Description<span class="small">(required)</span></label>
    <textarea name="message"></textarea>
<button type="submit" id="form-button">Submit</button>
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
