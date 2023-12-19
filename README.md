# ClimateCognize
Repository for ClimateCognize app that integrates the latest NLP climate-related text classification models into a Web App.
\
This application provides a web interface where users can interact with the latest NLP climate-related text classification models within the browser.
\
The users of the application can use the interface to classify text with a chosen model and perform the selected task, either by entering it manually in a text box, or by importing a whole dataset.
\
All users can contribute to the improvement of the models by consenting to the storing of the data that they enter and labeling it with the correct labels.
\
The application has two types of users: **regular users**, who can only use the interface for the classification of their data and provide their data to the database, and **admins** who can additionally filter this dataset, export it, and train the models on the community provided dataset, after cleaning of the data.

### Tasks
The texts can be processed on a variety of different NLP tasks that are available for selection within the interface:
- **Climate Topic Detection** - detection of the presence of climate-related topics in a given text
- **Sentiment Analysis** - classification of climate-related sentiment in a given text
- **Identification of Climate Commitments and Actions** - identification of whether a given paragraph is about climate-related commitments and actions or not
- **Determination of specificity** - determining whether a given climate-related paragraph is specific or not
- **Assignment of a climate disclosure category** - assigning a climate disclosure category to climate-related paragraphs based on the four categories of the recommendations of the [Task Force on Climate-related Financial Disclosures (TCFD)](https://www.fsb-tcfd.org/publications/)

### Models
The models that are utilized for the processing of these tasks come from [ClimateBert](https://www.chatclimate.ai/climatebert), as well as our own models further pre-trained for the Climate Topic Detection task.

## Repositories for the application
This repository is a central repository for all of the different integrated systems that this app consists of.
\
The code for the application is split into different GitHub repositories, depending on which integrated system is the code for.
- [**ClimateCognize Frontend**](https://github.com/gorgilazarev3/climate-cognize-frontend) - The interface for the application is developed in React, with Bootstrap 5 as the design framework. The frontend is in charge of providing the visual interface that the users interact with.
- [**ClimateCognize Backend**](https://github.com/gorgilazarev3/climate-cognize) - The main logic of the application is developed in Java SpringBoot, doing all the request handling and data processing and further forwarding the calls to the models.
- [**ClimateCognize Models API**](https://github.com/gorgilazarev3/climatecognize-models-api) - The API for providing the models capabilities is developed in Python, with a FastAPI endpoint available for all climate-related NLP tasks and models. The API receives the requests from the backend, does the predictions and performs the tasks, returning the output of the models that is propagated back to the backend for formatting and processing.



