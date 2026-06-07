# Day 30

To identify whether youre using a login shell or a non login shell, 
``` type ps $$ ``` , this should the outcome of ``` -bash ``` , this means its a login shell, or type ``` shopt login_shell ```, to test a non login shell, change the hostname of your machine by typing ``` hostnamectl set-hostname newhostname ``` ,and try the shopt command again, to reinitialize the system and set the new hostname properly, type ``` exec bash ``` , and the new hostname should now be showing. 