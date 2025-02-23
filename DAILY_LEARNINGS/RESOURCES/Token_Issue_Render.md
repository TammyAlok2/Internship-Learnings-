Here the issue is that when we connect frontend with backend there we store the token from the backend to the frontend , 
where we store the cookie for the session management , to check whether the user is login or not so the issue comes when our server
run on render.com and frontend is on vercel or other , then we token not come ,

Solution is : use cookie domain on cookie option also put your frontend on like bomboworld.com , backend is on api.bombooworld.com
