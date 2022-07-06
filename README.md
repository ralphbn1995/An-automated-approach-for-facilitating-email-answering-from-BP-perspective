
<h1 align="left">E-mail Responses Recommendation from Business Process Perspectives</h1>

### About The Project
<p align="justify">Most businesses and individuals communicate using email, which is the most frequent and successful method. The volume of emails received every day in the corporate sector is substantial, and fast responses to each email are crucial. This creates a lot of work for the company, especially for the employees relying on emails to perform their daily business activities, which induces manual and repetitive tasks (i.e., for writing emails). In this paper, we present a robotic process automation approach for enhancing business process (BP) management in emailing systems through the recommendation of BP knowledge and the textual contents of email responses. Our system relies on the history of email exchanges to learn a recommender model. It is based on cutting-edge technologies that can convert an unstructured email log into a structured event log organizing BP knowledge present in emails. Essentially, our proposed system suggests a list of email responses templates based on a received e-mail. The approach detects each BP knowledge in the received email thread and passes that information to a Long short-term memory model which predicts the next set of BP knowledge. We thereafter employ successive functions to provide suggestions to email users based on the predicted set of BP knowledge. Part of the Enron public email data set has been used to validate our method.</p>

### Getting Started
This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisite
###Structured event log

<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a></div>

<p align="justify">To learn from the previously received emails useful BP knowledge enabling the generation of BP oriented recommendations concerning email responses, we converted the email log of previously sent emails into a structure called event log to associate with each email all the useful BP knowledge. To do so, we were based on the worf of Elleuch et al. [1] </p>
  
 <p align="justify"> <strong> [1] Elleuch, M., Ismaili, O. A., Laga, N., Gaaloul, W., & Benatallah, B. (2020, September). Discovering activities from emails based on pattern discovery approach. In International Conference on Business Process Management (pp. 88-104). Springer, Cham.</strong></p>
 
 
<p align="justify">To better understand the structure of the generated event log, we show in the above figure an example of an event log extract. For each event of identifier Ev_ID, the event log extract reports the following attributes:</p>

<ul>
  <li>The occurred activity A<sub>cto</sub> = (AN<sub>occ</sub>, BD<sub>occ</sub>, BC<sub>occ</sub>) where AN<sub>occ</sub>, BD<sub>occ</sub> and BC<sub>occ</sub> refer respectively to the occurrences of its components: activity name, business data and business context;</li>
  <li>The speech act of the occurred activity (SA);</li>
  <li>Textual indices concerning the performers of the occurred activity (A<sub>tind</sub>);</li>
  <li>Email attributes where the activity occurred (em): ID to refer to its unique identifier, timestamp to refer to its sending time, Sender and Recipients to capture email interlocutors and Conv<sub>ID</sub> to capture the conversation ID to which the email belongs;</li>
  <li>The set of threads ID to which the event belong (Th<sub>id</sub>);</li>
</ul>



<p align="right">(<a href="#top">back to top</a>)</p>

