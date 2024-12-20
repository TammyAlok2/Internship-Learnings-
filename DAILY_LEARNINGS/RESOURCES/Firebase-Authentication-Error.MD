#In this article we will learn how I solve the firebase authentication error :
So on starting I configure firebase and setup a project there , in starting it working , but after some time it failed to work 
after debugging by sir we  find that I have given wrong rules in the firebase as well as the client and secret of google console expired 
so after we change it 

After that We checked but stil it not working then I changed by redirect uri to : http://localhost:3000/api/auth/callback to http://localhost:3000/api/auth/callback/google
then it start working fine 
