# Product Evaluation

## Task 1: Introduction

In the Week 8 lecture, we talked about product evaluation. We talked about two different but complementary approaches to evaluation: qualitative and quantitative evaluation. Both of these involve writing questions, so we discussed writing good questions. We emphasised that this is not an easy thing to do well: you need to be careful and thoughtful at each stage. 

If you need a refresher, or missed the lecture, that information will be essential for this week's material (and essential to get good marks for evaluation on your project!) All that information is in [Workbook 8](https://github.com/spe-uob/SEP2025/tree/main/Weekly%20Workbooks/08%20Product%20Evaluation).

One thing we said was that questionnaires are hard to write in a valid way, and that for some things, it is better to use questionnaires which have been prepared and validated by people trained in psychology. 

This week we will look at some questionnaires like that. We'll also some planning tasks for Testing Day next week.  

## Task 2: What is Testing Day?

Testing Day is an opportunity to test out your project on each other, and get feedback to help you improve your Beta Release and your Final Release.  

**Testing will take place on Monday 2nd February, 15:00-18:00 in MVB 2.11 and the Upper Atrium.**  

At any given time, half your team should be testing your product on other students, and half should be going around the space testing other students' project.  Feel free to try out projects similar to yours - for example, if you are making a game, test out other students' games!  But ideally, try to test projects from students you don't know so well, rather than just your friends' work.  


**You don't need to test your full product** - you can choose to check just some aspects of it, and it doesn't even need to be the live version - tests could be run on Figma diagrams or paper prototypes.  

**Make sure any tests are covered by the blanket ethics agreement** - this means that any tests should not include:

* sensitive or personal data, or data that can identify the participants, for example people's contact details.  If your system needs a log in, use a standard one!
* lying to, tricking or misleading participants
* sensitive or distressing images or topics
* anything that could cause physical or emotional harm
* data from vulnerable participants - this is very unlikely, but you can't, for example, ask if anyone is neurodiverse and then ask them to complete a test
* taking photos or videos of participants

If this will cause you problems, come and ask!  If you need a reminder of the Ethics rules for the unit, they're in the [Week 2 Workbook](https://github.com/spe-uob/SEP2025/tree/main/Weekly%20Workbooks/02%20Software%20Processes#task-8-ethical-issues).


> [!NOTE]
> Testing Day is just for system testing!  You can't use any data from these tests in any published work including your final dissertation!
> If you wanted to use it in published work, you would need to provide consent forms and information sheets about how you would use the data in those publications.  


> [!IMPORTANT]
> **Testing day is the bare minimum testing you should do!**
> If you want the extra marks good user testing brings, you'll need to do more. 

> [!IMPORTANT] 
> Every time you test, you must make sure participants have been given a Participant Information Sheet and have signed a Consent Form.  You can find examples [in this repo](https://github.com/spe-uob/SEP2025/tree/main/Weekly%20Workbooks/08%20Product%20Evaluation) - download and edit them.  


#

## Task 3:  Surveys you can use:  NASA Task Load Index (TLX),  System Usability Survey (SUS) 

 <a href='03%20Surveys%20you%20can%20use/slides/segment-1.pdf' target='_blank'> ![](../../resources/icons/slides.png) </a>

As we said in the previous lecture, it is hard to write good survey questions!  The best way round this is to use surveys that someone else has written, and had validated.  When it comes to your final dissertation, for example, you might find an academic paper that has done something similar to what you want to do, that has been validated via publication, and use the same questions they asked, citing your sources, of course!

Remember - not all evaluation needs to use questionnaires: Think Aloud and other methods can give you more detailed results which can help you diagnose problems you don't expect. Look back at week 8 and think about the best way to test your product.

Two commonly used surveys in Computer Science are the [NASA Task Load Index (TLX)](https://humansystems.arc.nasa.gov/groups/TLX/index.php) and the [System Usability Scale (SUS)](https://en.wikipedia.org/wiki/System_usability_scale). You can download them at the links, and the slides linked above (from Jon Bird) explain how to use them.

Here's a quick overview

### **NASA-TLX**

This is viewed as the gold-standard for measuring "subjective workload" - how much "load" the user feels under when using the system: This includes mental demands, physical demands, time pressure, frustration, the feeling of effort, and the user's sense of their own performance. This can be used as a simple measure of *some aspects* of usability. Remember from Week 8: usability has many aspects. You need to decide if this is the right thing to measure to understand the issues around your product. Maybe other things are more important?   

Note that there are two ways of using the NASA-TLX, the "raw" method and the "weighted" method. The raw method is easier to administer and takes up less user time. Read the slides to understand both approaches. If you use NASA-TLX, decide which you will use, and in your project write-up state which version you used.

### **SUS** 

SUS is a rough but reliable measure of **usability** which has become an industry standard. It contains more items than NASA-TLX, and takes a little longer to answer, but it addresses

### Administering and Analysing these Questionnaires

As described in the slides there are particular procedures for administering these questionnaires, and for analysing the results. In broad terms both involve adding up numbers from each "item" (or question) in a particular way, to get an overall score for workload or usability. 

The slides also describe how you might design your testing to use these questionnaires. What do you want to know, or compare - do you want to see which of two designs is preferred? Do you want to compare scores for different parts of your system, or for different kinds of users, or tasks? The slides explain how to statistically compare scores in these kinds of comparisons.

Finally, for both questionnaires it is worth looking beyond the overall scores - also look at the average scores for individual items (e.g. questions). Each item measures something different (e.g. frustration, physical load, inconsistency, etc.). Are some of these consistently high for your product, or for one design? If so this might point to a particular problem (e.g. frustration, inconsistency, etc.).

**Please note**: You don't have to use all the TLX or SUS questions, or any of them at all!  The important thing about user testing is you know what you are testing for and you so you are asking questions/running tests to elicit this information. 

**If you are making a game**, the industry-standard is the [Player Experience Inventory (PXI)](https://playerexperienceinventory.org/) - the website is great and includes off-the-shelf surveys.

# 

## Task 4:  Microsoft Forms

When you're planning a questionnaire, one option is to use a paper survey.  If you use this, you will need to make sure that you have the capacity to write up the responses later, and there are risks you might not be able to understand handwriting.  A very popular alternative is to use Microsoft Forms, which is free as part of Microsoft 365.

Forms enables you to write questionnaires quickly and easily, with options for people to choose options, rank answers, use a likert scale and write free text.  You can also add branching, so that the questions people see are tailored to their answer, and you can set who is allowed to complete the form, how many times they can answer, and when the form closes. 

When people complete a form, you can save the responses as an Excel document, so you can easily analyse the data you collected.  

[Microsoft have a guide to creating forms](https://support.microsoft.com/en-gb/office/create-a-form-with-microsoft-forms-4ffb64cc-7d5d-402f-b82e-b1d49418fd9d#PickTab=Web) - ignore how they get into it, because you can access it through you standard University 365/Outlook etc (click on the dots in the top right corner of the window to get the 365 apps)

**If you use MS Forms, remember to go into Settings and untick 'record name' so you are not collecting personal information!**


# 

## Task 5: Workshop

In your teams, start planning for the testing day.  You don't need to complete all of these in this session, but you need to work on them before the testing day.  

1. What do you want to find out from testing?  Think about your User Stories!

2. What part of your systems(s) will you test?

3. What methods do you want to use? ThinkAloud, observation, surveys (paper, digital, questions you ask and record the answers etc)

4. What questions do you want to ask?  What kind of answers will you collect?

5. How will you demo your product and ask the questions?  For example, will you bring your own laptop, or log onto a lab machine?  How many people can test it at the same time?  What kind of introduction will you have to the project?  

6. Ideally, which space will you want to test in (we have 2.11 and the Upper Atrium, but each has a maximum capacity, so we can't guarantee you'll be where you want).  
**If any of your team members have sensitivity issues, and would find it easier to be in a specific space, [get in touch with Sarah](mailto:sarah.connolly@bristol.ac.uk)**.  

7. How will you attract people to test your product?  For example, will you put a nice image on the screen at the end of the bank of desks?  We'll bring a standard 'please test my product' sign, but do you want more - especially if you want to sit in the Atrium. 

8. How will the session work?  Who will be running tests at what time during the 3 hours, and who will be testing other people's projects? Make a rota, and include times to touch base as a team to see how it's going.

Please also download and edit the [Participant Information Sheet](https://github.com/spe-uob/SEP2025/blob/main/Weekly%20Workbooks/14%20Product%20Evaluation%20Part%202%20-%20user%20testing/Participant%20information%20sheet.docx) and the [Consent Form](https://github.com/spe-uob/SEP2025/blob/main/Weekly%20Workbooks/14%20Product%20Evaluation%20Part%202%20-%20user%20testing/Consent%20form%20for%20an%20adult%20participant.docx), so you can print them out and bring them with you. 

# 
