PART 1
------------------------------------------------------------------------------------------------------------------------------------------------
Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.
0. 
var profilePic = document.querySelector('.profile-image');
profilePic.setAttribute('src', 'https://placebear.com/400/400');
------------------------------------------------------------------------------------------------------------------------------------------------
Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.
1. 
var skyPic = document.querySelector('#left-image .photography');
skyPic.setAttribute('src', 'https://placebear.com/g/325/225');
------------------------------------------------------------------------------------------------------------------------------------------------
Select the heading that says "Panda the Bear" and change it to your own name.
2. 
var nameHeader = document.querySelector('h1.highlight');
nameHeader.innerText = 'Luke Leveille';
------------------------------------------------------------------------------------------------------------------------------------------------
Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)
3. 
var header2 = document.querySelector('#employment h3');
header2.innerText = 'Hobbies';
------------------------------------------------------------------------------------------------------------------------------------------------
Change the colour of the body.
4. 
document.body.body.style.backgroundColor = '#88D';;
------------------------------------------------------------------------------------------------------------------------------------------------
Change the colour of each element using the highlight class. Use a for loop to do this.
5. 
var highlights = document.querySelectorAll('.highlight');
for (let i = 0; i < highlights.length; i++) {
  highlights[i].style.color = '#6B6';
}
------------------------------------------------------------------------------------------------------------------------------------------------
Change the font family of the h1 to 'monospace'.
6. 
nameHeader.style.fontFamily = 'monospace';
------------------------------------------------------------------------------------------------------------------------------------------------
Find a way to select the round icons in the sidebar and then change their colour.
7. 
var actionIcon = document.querySelectorAll('.action-icon-bg');
for (let i = 0; i < actionIcon.length; i++) {
  actionIcon[i].style.backgroundColor = '#FB6';
}
------------------------------------------------------------------------------------------------------------------------------------------------
Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
8. 
var nameField = document.querySelector('#message');
nameField.setAttribute('placeholder', 'identify yourself');
------------------------------------------------------------------------------------------------------------------------------------------------
Change the placeholder attribute of the message field to "state your business".
9. 
var messageField = document.querySelector('#name');
messageField.setAttribute('placeholder', 'state your business');
------------------------------------------------------------------------------------------------------------------------------------------------
Give the name field a "value" attribute of "your nemesis".
10. 
nameField.setAttribute('value', 'your nemesis');
------------------------------------------------------------------------------------------------------------------------------------------------
Change the value attribute of the email field to "koalathebear@gmail.com".
11. 
var emailField = document.querySelector('#email');
emailField.setAttribute('value', 'koalathebear@gmail.com');
------------------------------------------------------------------------------------------------------------------------------------------------
Change the value of the submit button on the contact form to "En garde!".
12. 
var submitField = document.querySelector('#submit');
submitField.setAttribute('value', 'En garde!');
------------------------------------------------------------------------------------------------------------------------------------------------
We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
13. 
submitField.setAttribute('disabled', 'disabled');
------------------------------------------------------------------------------------------------------------------------------------------------
We should help Panda protect their privacy by erasing their personal details from the sidebar.
14. 
var bioInfo = document.querySelector('.bio-info');
bioInfo.innerHTML = '';


PART 2
------------------------------------------------------------------------------------------------------------------------------------------------
Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)
0. 
var timeTravel = document.querySelector('#time-travel').parentNode;
timeTravel.parentNode.removeChild(timeTravel);
------------------------------------------------------------------------------------------------------------------------------------------------
That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().
1. 
var newPikachu = document.querySelector('#right-image img').cloneNode();
document.querySelector('section').appendChild(newPikachu);
------------------------------------------------------------------------------------------------------------------------------------------------
Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.
2. 
for (let i = 0; i < 10; i++) {
  newPikachu = document.querySelector('#right-image img').cloneNode();
  document.querySelector('section').appendChild(newPikachu);
}
------------------------------------------------------------------------------------------------------------------------------------------------
Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).
3. 
var bioInfo = document.querySelector('.bio-info');

var dateLine = document.querySelector('.bio-info li').cloneNode(true);

dateLine.childNodes[1].innerHTML = "Date";
dateLine.childNodes[3].innerHTML = "October 26, 2018";

bioInfo.appendChild(dateLine);