Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.
0. 
profilePic = document.querySelector('.profile-image');
profilePic.setAttribute('src', 'https://placebear.com/400/400');
------------------------------------------------------------------------------------------------------------------------------------------------
Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.
1. 
skyPic = document.querySelector('#left-image .photography');
skyPic.setAttribute('src', 'https://placebear.com/g/325/225');
------------------------------------------------------------------------------------------------------------------------------------------------
Select the heading that says "Panda the Bear" and change it to your own name.
2. 
nameHeader = document.querySelector('h1.highlight');
nameHeader.innerText = 'Luke Leveille';
------------------------------------------------------------------------------------------------------------------------------------------------
Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)
3. 
header2 = document.querySelector('#employment h3');
header2.innerText = 'Hobbies';
------------------------------------------------------------------------------------------------------------------------------------------------
Change the colour of the body.
4. 
document.body.body.style.backgroundColor = '#88D';;
------------------------------------------------------------------------------------------------------------------------------------------------
Change the colour of each element using the highlight class. Use a for loop to do this.
5. 
highlights = document.querySelectorAll('.highlight');
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
actionIcon = document.querySelectorAll('.action-icon-bg');
for (let i = 0; i < actionIcon.length; i++) {
  actionIcon[i].style.backgroundColor = '#FB6';
}
------------------------------------------------------------------------------------------------------------------------------------------------
Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
8. 
nameField = document.querySelector('#message');
nameField.setAttribute('placeholder', 'identify yourself');
------------------------------------------------------------------------------------------------------------------------------------------------
Change the placeholder attribute of the message field to "state your business".
9. 
messageField = document.querySelector('#name');
messageField.setAttribute('placeholder', 'state your business');
------------------------------------------------------------------------------------------------------------------------------------------------
Give the name field a "value" attribute of "your nemesis".
10. 
nameField.setAttribute('value', 'your nemesis');
------------------------------------------------------------------------------------------------------------------------------------------------
Change the value attribute of the email field to "koalathebear@gmail.com".
11. 
emailField = document.querySelector('#email');
emailField.setAttribute('value', 'koalathebear@gmail.com');
------------------------------------------------------------------------------------------------------------------------------------------------
Change the value of the submit button on the contact form to "En garde!".
12. 
submitField = document.querySelector('#submit');
submitField.setAttribute('value', 'En garde!');
------------------------------------------------------------------------------------------------------------------------------------------------
We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
13. 
submitField.setAttribute('disabled', 'disabled');
------------------------------------------------------------------------------------------------------------------------------------------------
We should help Panda protect their privacy by erasing their personal details from the sidebar.
14. 
bioInfo = document.querySelector('.bio-info');
bioInfo.innerHTML = '';