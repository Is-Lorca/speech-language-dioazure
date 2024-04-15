# DIO Challenge — Speech and Language on Azure ML
The files used to complete these challenges are located in the Input and Output folders, being the source files and their results, respectively.

# Step by Step:
In this challenges, I needed to use two different resources, the **Azure AI Speech** resource and **Language** resource, let’s start configuring them:

### Azure AI Speech Resource:
1. Open the **Azure AI Speech Studio** signing in with your Microsoft account;
2. Select **Settings** then _**Create a resource**_. Configure it with the following settings:
	
    **Name of new resource**: _enter a Unique name_;
	
    **Subscription**: _your subscription at Azure_;
	
    **Region**: _Select a supported region_;
	
    **Price Tier**: _Free F0_ (if available, otherwise select Standard S0);
	
    **Resource group**: _Select or create a resource group with a unique name_;
3. Select **Create resource** and wait until the resource has been created and then select _Use resource_. The Get Started with Speech page is displayed.

The first resource is, now, ready to be used.

### Language Resource:
1. Open the Azure portal at https://portal.azure.com, signing in with your Microsoft account if you are not already signed in;
2. Click the _**+ Create a resource**_ button and search for _Language service_;
![language_tile](screenshots/Captura%20de%20tela%202024-04-15%20184853.png)
3. Select **create** a Language Service plan, you will be taken to a page to **Select additional features**, keep the default selection and click _Continue to create your resource_;
4. On the page _**Create Language**_, configure it with the following settings:
	
    **Subscription**: _Azure subscription_;
	
    **Resource group**: _Select or create a resource group with a unique name_;
	
    **Region**: _East US_;
	
    **Name**: _A unique name_;
	
    **Pricing tier**: _Free F0 or S (if F0 is not available)_;
	
    **By checking this box I acknowledge…** (_Selected_);
5. Select _**Review + create**_ then **Create** and wait for deployment to complete.

#### _**Configure your resource in Azure AI Language Studio:**_
1. Open _Language Studio_ at https://language.cognitive.azure.com and sign in
2. When prompted with _Select an Azure resource_, make the following configurations:
	
    **Azure directory**: _Default Directory, the directory you are using_;
	
    **Azure subscription**: _Select your subscription_;
	
    **Resource type**: _Language_;
	
    **Resource name**: _select the Language service resource you created_;

Select **Done**.

Now, the second and last resource is ready, we can begin with the challenges.

## Challenges:
### 1. Speech to Text:
1. Select https://aka.ms/mslearn-speech-files to download speech.zip (also located in the Input directory of the first challenge);
2. On the Get started with Speech page, Select **_Try out Real-time speech to text_**;
![real-time_speech_tile](screenshots/Captura%20de%20tela%202024-04-15%20191451.png)

3. Click **Browse files** and navigate to the folder where you saved the file saved previously, select the audio you want to be transcribed and wait for the results.

Try other audio to see different results.

### 2. Analyzing reviews with Language Studio:
1. Go to the website: https://language.cognitive.azure.com;
2. On the _Welcome to Language Studio_ select the **Classify text** tab and select the **Analyze sentiment and mine opinions** tile;

    ![analyse_sentiment_tile](screenshots/Captura%20de%20tela%202024-04-15%20200135.png)

3. Under Select text language, select **English**;
4. Under Select your Azure resource, select your resource;
5. Under _Enter your own text, upload a file or use one of our sample texts_, copy and paste the following review:
```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
```
6. Check the box and then select _**Run**_;
7. Notice, now, that the document is analyzed for sentiment, as well as each _sentence_.

## Finalizing:
If you have already finished all the exercises above, delete any resources that you no longer need. This will avoid unnecessary costs for you:

1. Open the Azure Portal at https://portal.azure.com and select the resource group that contains the resource you created;
2. Select the resource, click on **Delete** and then **_Yes_** to confirm.