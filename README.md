# Instagram Automation for blogging

## 1) Overview :

The project aims to automate the blogging activities for any blogger. The aim of a blogger is to reach out to the interested public, which can in turn help the blogger to grow their own community. Moreover, to have a good amount of followers and appropriate handles to follow and to monitor hashtags closely related for their blogging activities is the main tasks a blogger needs to achieve.

The problem being that the human speed to achieve the same tasks will take a lot of time, so the idea is to automate all these generic activities which will be simuated with webdriver, so the user can have a look over every activity the blogger wants to achieve, while saving a lot of their own time.

## 2) Technical Details :

### 2.1) Libraries used :

* selenium(need to be installed excplicitly if not installed. In any command line type the command **pip install selenium**)
* numpy
* pandas
* time
* random
* Counter (import from collections library)
* matplotlib

### 2.2) Pre-requisites :

1. Instagram *Username* and *Password* has to be fed to **credentials.txt** in the specified format. Then only the code is to be executed using the python notebook **InstaBot.ipynb**.
2. Need to have selenium webdriver (preferrably for Firefox(geckodriver)). Even though I am including this in my repository.

### 2.3) Functionalities :

There are 3 types of generalised activities. These are :

#### 1. General Activities :

These activities are the most general, almost every instagram user*(not just bloggers)* does these activities. These are :

1. To get the first *n* search handles according to an input query(hashtags and locations will be excluded from this result; for example, if the query is *"food"* then then *#food* will be excluded).
2. To follow an insta handle, given that the **handle input is correct** and the **case-sensitivity** is also correct.
3. To unfollow an instagram handle with the **correct handle name** with the correct **case-sensitivity**.
4. To check the story of a given handle. Again the handle should be **exactly correct** with **correct case-sensitivity**.

#### 2. Blogging Activities :

These blogging activities are again categorised in 2 more categories. These are :

**i) Handle Related Activities :**

1. To goto a valid instagram handle and like their recent n posts.
2. To goto a valid instagram handle and unlike their recent n posts.

**ii) Hashtag Related Activities :**

1. To find some top hashtags according to the search results around an input hashtags. For example if we searched *#food* and the search shows *#food*, *#foodporn*, *#tasty*, *#foodie*, *#yummy*, then these are the search results for the query *#food* and hence the answer for our query.
2. To follow a hashtag.
3. To unfollow a hashtag.
4. To like some continous n recent posts according to a hashtag query.
5. To follow n random instagram handles according to hashtag query.

#### 3. Statistics and Analytics Activities :

These activities will guve a visualization of the account related data. There are two functionalities in these activities. These are :

1. View current number of followers and following.
2. To take a hashtag query and then traverse through n posts and find the top k hashtags around it. Then the pie chart of these k hashtags will be showed and at last the user gets to update these hashtags in a local file name **hashtags_logs.csv** if the user wants to update it. For example, if we want to extract top 3**(k)** hashtags around *#food***(hashtag query)** by traversing 10**(n)** recent posts, then the output will be a pie chart of those 3 hashtags that appeared in most recent 10 posts, at last the user will be asked to update their hashtags log file with this result for future reference.

### 2.4) Code Execution :

First complete the pre-requisites and then simply execute all the cells. Now, the user will be asked to navigate through the type of activity the user desires, automatically.

## 3) Future Developments :

1. To track the exact users who follows or unfollows to analyze fake users over time.
2. To create a log file which keeps track of every activity done by the user through this script.
3. To create one functionality which can comment a positive comment according to a hashtag query.
4. To extract important followers from a given handle, also to track these followers activities to check their engagement for the users' blogging activities.
