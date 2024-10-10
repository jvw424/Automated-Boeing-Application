# Automated-Boeing-Application

## Intro

- Automates the application process for applying direct to Boeing
- Uses [seleniumbase](https://seleniumbase.com/) to achieve undetectable automation
- Implements a decision tree to answer personal history questions
- Can apply to multiple listings in one run

## Disclaimer

I do not recommend spamming applications through use of this type of technology. To put your best foot forward in the application process I would personally verify all form fields of an application. That being said, some companies don't have an intuitive application process. Boeing's for example, fails to store prior responses even for yes or no questions they ask on every application. Thus, I have designed this program to take the monotony out of answering questions like: "do you have family members working for Boeing", "Have you held political office", etc.


## Instructions

All the logic is contained in the [apply.ipynb](https://github.com/jvw424/Automated-Boeing-Application/blob/main/apply.ipynb) file.

There are a few things that need to be taken care of before the application is ready to be run.
1. This program starts by using the information from the last application you submitted to Boeing, thus the first thing it needs is for you to manually submit an application. Make sure you record the email and password associated with this submission.
2. In the [apply.ipynb](https://github.com/jvw424/Automated-Boeing-Application/blob/main/apply.ipynb) file there are `TODO` comments left where the login information for your account should be input
3. The section denoted by ##### Page 3 ###### in the apply function contains the monotonous questions about boeing specific eligibility questions. These questions by default are set to "No" or "NA" and to personalize simply change the response element of `sb.type("element-tag", "response")`  to your desired input.
4. The last personalization involves the decision tree that is defined at the start of the application. The logic flow for this is pretty straight forward any you can edit it with your personal experience record. Admittedly, this part of the application process is hit or miss. That is intentional though as it is set to stop at this point because I like to manually verify my application reads correctly. 
5. After the personal experience section is completed, manually submit the application. This involves filling out one or two demographic questions.
6. In order to run the program go to the last cell block and populate the list `links` with the urls of the jobs you would like to apply to.

```
links = []

for link in links:
    apply(link)
```



