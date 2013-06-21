---
layout: post
title: "Steganography"
date: 2013-06-19 21:42
comments: true
categories: 
---
{%blockquote Hidding Folder Behind an Image %}
{%endblockquote %}
{% img https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcQkZlLGh1eMQTQwZ9dvr0zGRtOk6pMYhxmuuy11TkK_y9EwryBN %}

Steganography is the art and science of writing hiden messages in such a way that no one, 
apart from the sender and intended recipient suspects the existence of the message. 
Example of Steganography we are going to try is 'Hidding a folder behind an image'.
Follow the steps below and you will learn a technique of steganography:

1. Create a folder containing all your secret files in it.
2. Here, the following things are needed :-
	-A folder containing all your secret files: here, 'hide' is the folder .
	-An image to hide the folder: here, image.jpg is the image used. 
3. Create a zip archive of the folder. In linux use the following to zip a folder :
	{% codeblock %} 
	zip -r hide.zip hide
	{% endcodeblock %}
4. Now we will use the linux command 'cat' which is used to for different purposes
	-displaying contents of file.	
	-creating new files.
	-combining copies of files.
5. The 'cat' command will read the image file first, then 'hide.zip' and will concatenate them together, and redirect the output in a file 'final.jpg'.
	{% codeblock %}
	cat image.jpg hide.zip > final.jpg
	{% endcodeblock %}
6. Now, the file 'final.jpg' will contain your secret folder but it would appear as an image to anyone unknown to this technique.
7. To see the hidden folder behind the image:
	{% codeblock %}
	unzip final.jpg
	{% endcodeblock %}

The advantage of steganography over cryptography alone is that messages do not attract attention to themselves. Plainly visible encrypted messages—no matter how unbreakable—will arouse suspicion, and may in themselves be incriminating in countries where encryption is illegal. Therefore, whereas cryptography protects the contents of a message, steganography can be said to protect both messages and communicating parties.
