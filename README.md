
<h1 align="left">E-mail Responses Recommendation from Business Process Perspectives</h1>

### About The Project
<p align="justify">Today, emailing systems are one of the information systems that are increasingly used for performing business process (BP) activities. The emails that present the execution logs of these information systems are therefore rich in business knowledge. This makes their analysis to improve their management an added value in the context of BPM (BP management). However, the emails are of unstructured textual nature, which makes this difficult. As a result, employees have only partial access to corporate email business knowledge if they only rely on traditional search methods, which are additionally slow and time consuming. Furthermore, employees usually have to compose emails when performing their repetitive BP activities, even though their textual contents tend to be similar. In this paper, we propose an automated approach to improve email management in the BP context. We mainly focus on recommending useful BP knowledge and email templates when responding to an incoming email. These BP knowledge are about the set of activities to be expressed in the email responses, the intention from expressing them in the email (i.e. speech act) and the manipulated business data. Our work differentiate from existing works according to two fields: (1) In the field of process prediction, we consider non-structured textual data (i.e. emails) for recommending/predicting next activities knowing those that are in progress, and (2) In the field of email recommendation, we inject BP knowledge of incoming emails to provide BP oriented suggessions concerning the texual content of email responses.</p>

### Content of this repository

Our goal is to recommend email responses and business data values based on a received e-mail. The proposed approach shown in the following figure is divided into two main phases: (1) A learning phase where BP knowledge are discovered from emails and the recommender model is trained, (2) A recommendation phase where the discovered BP knowledge are used to provide suggestions to email users. In this repository, we presents the essential part of the recommendation phase implemented in this approach: (i) Recommend_email_responses_templates.ipynb, and (ii) BP_knowledge_recommender_learned_model.ipynb.

<div align="center">
  <a href="https://github.com/ralphbn1995/E-mail-Responses-Recommendation-from-Business-Process-Perspectives">
    <img src="https://github.com/ralphbn1995/E-mail-Responses-Recommendation-from-Business-Process-Perspectives/blob/main/approach-overview.png?raw=true" alt="Logo" >
  </a></div>

### Prerequisite: Structured event log

<div align="center">
  <a href="https://github.com/ralphbn1995/E-mail-Responses-Recommendation-from-Business-Process-Perspectives">
    <img src="https://github.com/ralphbn1995/E-mail-Responses-Recommendation-from-Business-Process-Perspectives/blob/main/IMG.PNG?raw=true" alt="Logo" >
  </a></div>

<p align="justify">To learn from the previously received emails useful BP knowledge enabling the generation of BP oriented recommendations concerning email responses, we converted the email log obtained from the Enron dataset into a structure called event log to associate with each email all the useful BP knowledge. To do so, we were based on the work of Elleuch et al. [1] </p>
  
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

