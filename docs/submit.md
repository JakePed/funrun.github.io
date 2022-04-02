---
layout: page
title: Submit
permalink: /submit/
---

Please Read Submission guidelines before submitting

Art to be submitted must be a ratio of 2.5 x 3.5 (ex, 400x560), or 1:1 (square)

Images on the site are loaded via the hosted url, so we recommend keeping file sizes down as much as possible to speed up loading times. 

Issuance must be LOCKED using the lock token 
No divisible assets.

NSFW is fine, when done in an artistic manner with explanation/description included with the asset.

Minimum token supply is 21, (No Burning lower than 21 to respect the other artists and collectors) 
In the event this happens, the artists work will have all links removed 

Physical Art should be issued as a 1 of 1 with digital extras or prints being issued as subassests (please contact @PepePeddler directly to arange this).

No websites or QR codes

Cards must not be distributed before they are confirmed and live of the website. Any distribution prior will result in the work not being listed.

*Note: Please make sure your assests are minted before making a submission!*{: .small}

<form
    action="https://usebasin.com/f/1944773b2de6"
    method="POST"
    enctype="multipart/form-data"
    id="form"
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
var form = document.getElementById("form");
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
