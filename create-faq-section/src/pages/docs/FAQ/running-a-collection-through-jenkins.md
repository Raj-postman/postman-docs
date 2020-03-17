---
title: "Running a collection through Jenkins"
order: 360036847714
page_id: "Running-a-collection-through-Jenkins"
warning: false
---

Newman and Jenkins are a perfect match to run the collection and if you want to schedule a collection to run at specific time intervals. Below steps should help you achieve the same:

**Step 1:** Download and install Jenkins - [https://jenkins.io/download](https://jenkins.io/download)

**Step 2:** Install NodeJS and npm. Newman is written in NodeJS and we distribute the official copy through npm. Install - [https://docs.npmjs.com/downloading-and-installing-node-js-and-npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) 

**Step 3:** After Jenkins is installed and ready, browse this link - [http://localhost:8080](http://localhost:8080) and login to your Jenkins with credentials. Please note, Jenkins by default start on port 8080.

**Step 4:** Create a new job by clicking on the “New Item” link on the left sidebar > Select a “Freestyle Project” from the options > Name your project. 

![Screenshot_2019-10-14_at_1.18.49_PM.png](https://support.getpostman.com/hc/article_attachments/360048223274/Screenshot_2019-10-14_at_1.18.49_PM.png)

![Screenshot_2019-10-15_at_11.47.47_AM.png](https://support.getpostman.com/hc/article_attachments/360048223334/Screenshot_2019-10-15_at_11.47.47_AM.png)

 **Step 5**: Goto build section of the Jenkins job created- add build step ->execute shell and add your "Newman command to run a collection in execute shell command section. (for e.g. - # newman run test_collection.json) and apply and save.

![Screenshot_2019-10-15_at_11.52.49_AM.png](https://support.getpostman.com/hc/article_attachments/360049088633/Screenshot_2019-10-15_at_11.52.49_AM.png)

![Screenshot_2019-10-15_at_11.55.18_AM.png](https://support.getpostman.com/hc/article_attachments/360048223374/Screenshot_2019-10-15_at_11.55.18_AM.png)

**Step 6**: Click on Build Now to run the collection.

![Screenshot_2019-10-15_at_11.58.09_AM.png](https://support.getpostman.com/hc/article_attachments/360049088713/Screenshot_2019-10-15_at_11.58.09_AM.png)

 **Step 7**:  Now go to the Build History section and click on the recent build, to check the console output for the latest collection run results.
 
![Screenshot_2019-10-15_at_5.34.32_PM.png](https://support.getpostman.com/hc/article_attachments/360049107393/Screenshot_2019-10-15_at_5.34.32_PM.png)

![Screenshot_2019-10-15_at_5.27.24_PM.png](https://support.getpostman.com/hc/article_attachments/360048238494/Screenshot_2019-10-15_at_5.27.24_PM.png)
