# CS305_Module5

# Introduction 
This repository contains functionality for the Chatbot API. It's purpose is to provide a webhook service that DialogFlow can send a webhook request and receive a webhook response. This will allow us to create intents that use fullfillment to call this API. Within this API, we can create custom functionality and pull from various sources to serve data to the Louie Chatbot.

# Getting Started
Step 1:
Make sure you have access to the Git repository. From there you will get the path to clone the repository down. I recommend creating a new folder (mine is projects_git) on your C drive and then cloning into that folder.

Step 2:
Install git (https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and clone the repository. Git comes with a command line interface, but feel free to download a GUI if you would prefer. I suggest doing the clone from the command line interface and then using Team Explorer in Visual Studio. Open the command line or git BASH and navigate to the folder you setup on your C drive. Run this command “git clone https://devops.internal.nau.edu/ITS-EIS/EISDev/_git/ChatCoreApiNauEdu”.

Step 3:
Download Visual Studio 2019 (https://visualstudio.microsoft.com/downloads/). I recommend Professional or Enterprise as they have more features, but they require a license. Marc Lord can bind a license to your nau.edu email if you have not used Visual Studio before. There is also a Community version which is similar to Professional but does not require a license, but it does not have as many code lens features to track changes across multiple users.  If you would prefer a light weight IDE or are using a different OS then Windows, then I recommend using Visual Studio Code (https://code.visualstudio.com/) which is a bit more simplistic and doesn’t require a license. If given the option to install IIS Express in the setup make sure to include it. 

Step 4:
Download Postman  (https://www.postman.com/downloads/). Postman will allow you to test the API and simulate Dialogflow calling the webhook fulfillment.

Step 5:
Import Postman collection containing requests to test this API locally and on Dev. The collection file is located in the Testing folder at the root of the project. To import the collection navigate to File > Import > File then select the JSOn file downloaded from the repo. 

Step 6:
Once Visual Studio is installed open the solution that is at C:\projects_git\ChatCoreApiNauEdu\src\Chat.WebApi. The file is called ChatWebApi.sln. Choose build solution in the top navigation under Build. If the build compiles successfully then you are good to start running the code. Choose Start Debugging, or press F5, it is in the Debug menu. With the debugger running, open your web browser and navigate to http://localhost:55556/index.html. You should then see a list of the endpoints in the API.

Step 7 (If you experience issues):
If installing Visual Studio did not setup IIS Express for you, you can download it from here https://www.microsoft.com/en-us/download/details.aspx?id=48264. If you get a message when building that says the .NET Core 3.1 framework is not present you can download the SDK from here https://dotnet.microsoft.com/download/dotnet-core/3.1. Please let me know if you run into any other issues not listed in Step 5 so that I can add them to this section.


# Build and Test
Using Visual Studio 2019 and IIS Express you can build the code and run it using the debugger. While the debugger is running you can see the results by opening your browser and going to http://localhost:55556/index.html. At this time we do not have any automated testing.

# Contribute
New code should be written in a feature branch and tested locally. Once ready to be incorporated in the development environment, a pull request should be used to merge the changes into the master branch. From there the approver should squash commits and cleanup the branch when it is integrated into the master branch. When a change is pushed to the master branch it will compile and release to the dev envrionment. You can see the build process in pipeline and release information in the release section. From there the release can be approved for test and prod.

# Useful Resources
https://cloud.google.com/dialogflow/es/docs/fulfillment-overview
https://cloud.google.com/dialogflow/es/docs/fulfillment-webhook
