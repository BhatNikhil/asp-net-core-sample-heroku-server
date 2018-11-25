# ASP.NET Core Sample Server
Sample AspNetCore Project, Dockerized and Connected to Heroku

__Points to remember:__  
The Internal Port number must bind to the $PORT environment variable, and neither to any hardcoded port number, nor to the EXPOSE port number in the Docker File  

__Instructions to Deploy the Docker instance on Heroku:__  
1. Build And Publish the Project  
2. Copy the docker file to the Publish Folder  
3. Open Terminal and Navigate to the publish folder  
4. Cmd: heroku login  
5. Cmd: heroku container:login  
6. Cmd: docker build -t <image-name> .  
7. Cmd: docker tag <image-name> registry.heroku.com/{heroku-app-name}/web  
8. Cmd: docker push registry.heroku.com/{heroku-app-name}/web  
9. Cmd: heroku container:release web -a <heroku-app-name>  
  
__References:__  
* Major Reference: https://dotnetthoughts.net/hosting-aspnet-core-applications-on-heroku-using-docker/  
* Minor Reference: https://blog.devcenter.co/deploy-asp-net-core-2-0-apps-on-heroku-eea8efd918b6  
