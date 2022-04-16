---
layout: page
title: Com card
permalink: /comcard/
---

THETIMESNEWS: 

The Community asset aims to be the largest collective creation on bitcoins counterparty. An evolving asset which updates as new submissions are entered.

The asset works in a way that both supports the project and gives back to those that support the project.

Acts as a grail, which means all holders of the assest will receive all newly created subassest iterations as dividends, from the time of their creation.


How it works:

- Anyone can contribute to the evolving community asset.

- Right click and open the image below, in a new tab, save it (keep dimension the same)

- Make you own creative iteration.

- Submit below with required information

- Your assest will be minted (2009 supply) as a sub asset of THETIMESNEWS

- Dividends will be sent to current holders of the main asset

- Remaining supply will be sent to the given address along with token ownership


Submit your iteration here:

*0.5 XCP is required for the cost creation of the subassest and to help with the fees associated with dividends and transfer of tokens and ownership.

Send XCP to - 1GofUv9J8Rv5KJKw1An4VpqDrF7Hh7EdGW

<form
    action="https://usebasin.com/f/83cf165714bd"
    method="POST"
    enctype="multipart/form-data"
    id="form"
   >
<label for="email">Email <span class="small">(required)</span></label>
<input type="email" name="email" placeholder="john@doe.com" required />
<label for="text">Artist name <span class="small">(required)</span></label>
<input type="text" name="Artist Name" />
<label for="text">Asset Name <span class="small">(required)</span></label>
<input type="text" name="Asset Name" />
<label for="text">Image/GIF URL <span class="small">(required)</span></label>
<input type="text" name="Asset Name" />
<label for="text">XCP Transaction ID <span class="small">(required)</span></label>
<input type="text" name="XCP Transaction ID" />
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