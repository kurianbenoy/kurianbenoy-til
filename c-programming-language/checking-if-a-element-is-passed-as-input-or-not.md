# Checking if a element is passed as input or not?

Usually most of the C programs I had learned in my school were expecting an input from start itself. Yet it's not always the case and it's a common principle to **never ever trust the user input**.

In C you can can check if the user input is valid or not by checking if it's value is 1 while reading. A sample program to do this is as shown below:

![](<../.gitbook/assets/WhatsApp Image 2021-09-22 at 9.38.35 PM.jpeg>)

According to function definition shared by Selvaraj:

scanf - On success, these functions return the number of input items successfully matched and assigned; this can be fewer than provided for, or even zero, in the event of an early matching failure. The value EOF is returned if the end of input is reached before either the first successful conversion or a matching failure occurs. EOF is also returned if a read error occurs, in which case the error indicator for the stream (see ferror(3)) is set, and errno is set to indicate the error.



A useful stackoverflow answer mentioning this

{% embed url="https://stackoverflow.com/questions/4159985/while-scanf-eof-or-scanf-1" %}

