---
layout: default
title:  "Phase 2"
date:   2019-02-23 09:00:00 -0800
categories: phase2
---

<center><img src = "../../earllogo_alt.png" /></center>

# Phase 2: Design

&nbsp;&nbsp;&nbsp;&nbsp;Welcome to the design portion of the CalendarCompanion application. Here we will discuss the design details surrounding a mobile implementation of Calendar Companion. We will provide design decisions, details, and prototypes.

&nbsp;&nbsp;&nbsp;&nbsp;This document serves to provide an overview of the design phase of the CalendarCompanion application. We will first provide a high level hierarchical overview and short description of each component in our design proposal. Next, each component will be be described in detail; each section will include a design decision rationale for the component in question (interface metaphors, widget choices, etc), plus how that portion of the design fulfills a requirement based on data gathered in Phase 1. Finally, each component section will include a low fidelity prototype, and a detailed description of the behavior of each component widget.

&nbsp;&nbsp;&nbsp;&nbsp;Using this document, a developer should be provided with enough detail that the application could be made with little to no additional guidance from the designers of the application. The Earl Technologies team is please to present the CalendarCompanion prototype and design document.
<!-- Design Desicion and Rationale
Requirement from Phase 1
Low Fidelity Prototype
Behavior -->

&nbsp;<br>

---


&nbsp;<br>
&nbsp;<br>
&nbsp;<br>
<center>
    <b>University of Victoria<br>
    SENG 310 Winter 2019<br>
    Prof. G. Tzanetakis <br></b>
    &nbsp;<br>
    <b>Alex Nguyen:</b> V00894486<br>
    <b>Brendan Ciccone:</b> V00871008<br>
    <b>Daniel Dubichev:</b> V0877776<br>
    <b>Alex Deweert:</b> V00855767<br>
&nbsp;<br>
&nbsp;<br>
    <font size = "+3">
        <b>Phase 2: Design</b>
        <br>
        <b>Calendar Companion</b>
    </font>
</center>
&nbsp;<br>
&nbsp;<br>

<div markdown = "1" id = "top">

# Contents

</div>

<ol>
  <li><a href = "#high_level_overview">Hierarchical overview</a></li>
  <li><a href = "#details">Details</a></li>
    <ol>
        <li><a href = "#login_page">Login Page</a></li>
        <li><a href = "#course_schedule">Course Schedule</a></li>
            <ol style = "list-style-type: upper-alpha">
                <li><a href = "#future_courses">Future Courses</a></li>
                <li><a href = "#weekly_timetable">Weekly Timetable</a></li>
                <li><a href = "#create_a_degree_map">Create a Degree Map</a></li>
                <li><a href = "#my_degree_maps">My Degree Maps</a></li>
            </ol>
        <li><a href = "#details">Study Assistant</a></li>
            <ol style = "list-style-type: upper-alpha">
                <li><a href = "#assignment_alarm">Assignment Alarm</a></li>
                <li><a href = "#study_tips_and_tricks">Study Tips and Tricks</a></li>
                <li><a href = "#test_reminders">Test Reminder</a></li>
                <li><a href = "#todo_check_list">Todo/Check List</a></li>
            </ol>
        <li><a href = "#map">Map</a></li>
        <li><a href = "#school_events">School Events</a></li>
        <li><a href = "#find_my_prof">Find My Prof</a></li>
            <ol style = "list-style-type: upper-alpha">
                <li><a href = "#contact_info_and_office_hours">Contact Info and Office Hours</a></li>
                <li><a href = "#professor_ratings">Professor Ratings</a></li>
            </ol>
        <li><a href = "#student_finances">Student Finances</a></li>
            <ol style = "list-style-type: upper-alpha">
                <li><a href = "#tuition_and_account_balance">Tution and Bank Account</a></li>
                <li><a href = "#one_card_account">One Card Account</a></li>
                <li><a href = "#link_bank_account">Link Bank Account</a></li>
                <li><a href = "#make_payment">Make Payment</a></li>
            </ol>
        <li><a href = "#user_account">User Account</a></li>
        <li><a href = "#help">Help</a></li>
            <ol style = "list-style-type: upper-alpha">
                <li><a href = "#calendar_companion_tutorial">CalendarCompanion Tutorial</a></li>
            </ol>
    </ol>
</ol>
&nbsp;<br>
&nbsp;<br>

---

&nbsp;<br>
&nbsp;<br>

<div id = "high_level_overview">
<div markdown = "1">
# Hierarchical overview
</div>
<ol>
    <li><a href = "#login_page">Login Page</a>
        <br>This is a standard login page that will display a CalendarCompanion logo. This page is allows a user to enter a netlink (or similar) ID, and their password. This page will display standard options typical in a mobile application login page; options such as forgot password, forgot account name, remember me, signup, etc. A successful sign in here will direct the user the application home page that contains links to course schedule, study assistant, map, school events, find my prof, student finances, user account, and help. All interaction in this application is done via touch screen interaction. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
    <li><a href = "#course_schedule">Course Schedule</a>
        <br>This page acts as a parent to other sections related to scheduling. This page will be home to four submenus. Underneath each submenu will be a subtitle which explains what it's use is. In addition, students may scroll down to see to see all submenus in cases where they menus do not fit on the device screen. <a href = "#top">[top]</a>
        </li>
        &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#future_courses">Future Courses</a>
            <br>The Future Courses tool allows a student to view courses offered in a specific year and session (Fall, Spring, Summer). This is useful for the degree map creation, as one can quickly and easily view courses offered in the future.
            </li>
            &nbsp;<br>
            <li><a href = "#weekly_timetable">Weekly Timetable</a>
            <br>The Weekly Timetable tool allows the user to see the current semester weekly schedule. From Monday to Friday, the Weekly Timetable will import scheduled courses/labs for the user based on the UVic (or other) database, and will display all corresponding locations, times, and professors.
            </li>
            &nbsp;<br>
            <li><a href = "#create_a_degree_map">Create a Degree Map</a>
            <br>A user can create a degree map which helps the user to stay organized and in control of their University experience. The user may receive email or text notifications just prior to course registration openings. The user may also sign up for a course according to their degree map session and year, expediting their graduation time.
            </li>
            &nbsp;<br>
            <li><a href = "#my_degree_maps">My Degree Maps</a>
            <br>This section affords a user the ability to create and view a map of their degree. In other words, a map is a sequence of courses that a student must take in order to reach the desired degree graduation goal.
            &nbsp;<br>
            </li>
        </ol>
    <li><a href = "#details">Study Assistant</a>
    <br>The Study Assistant page is parent to all components that are related to what a user might expect to find in a typical study assistant application. Such components as alarms, tips an tricks, reminders, and checklists are submenus to this page. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#assignment_alarm">Assignment Alarm</a>
            <br> TODO: Brendan
            </li>
            &nbsp;<br>
            <li><a href = "#study_tips_and_tricks">Study Tips and Tricks</a>
            <br> TODO: Brendan
            </li>
            &nbsp;<br>
            <li><a href = "#test_reminders">Test Reminder</a>
            <br> TODO: Brendan
            </li>
            &nbsp;<br>
            <li><a href = "#todo_check_list">Todo/Check List</a>
            <br> TODO: Brendan
            </li>
            &nbsp;<br>
        </ol>
    <li><a href = "#map">Map</a>
    <br>One of the most significant features of the CalendarCompanion application is campus map navigation. This section is navigated to based on the main menu item “Map”. It can also be selected from “Find Class Room” in the “Course Schedule” section, or by requesting it from the Virutal Assistant. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
    <li><a href = "#school_events">School Events</a>
    <br>One of the factors that greatly affect a student's performance at university is their social life. Moreover, social development at this stage is a student's life is key to their success in the workplace. This part of the application keeps a student apprised of up-to-date news around campus. In this feature, all academic events, social events, and campus news are uploaded to the student's School Events feed everyday. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
    <li><a href = "#find_my_prof">Find My Prof</a>
    <br>Here we have the Find My Prof section which allows a student to search a professor by name and by institution. This section acts as a parent to two other sections. The results of a search on this page can be utilized in the child sections "Contact Info and Office Hours" and "Professor Ratings". <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#contact_info_and_office_hours">Contact Info and Office Hours</a>
            <br>Here we have the “Find Professor Contact Information and Office Hours” section of the application. This section is navigated to based on the main menu item “Find My Prof”. This section can also be gotten to based on a suggestion from the Virtual Assistant. This is basically the results page of a professor search based on the parent section, "Find My Prof".
            </li>
            &nbsp;<br>
            <li><a href = "#professor_ratings">Professor Ratings</a>
            <br>This is another child component under the "Find My Prof" section. This section allows a user to view all professor ratings based off of the search results from Find My Prof. A list of professor ratings are present in this section, and can be sorted by list entry detail. For example, if every list entry contains an entry-rating (other students can agree or disagree with the professor rating), a course number, a grade provided, a user can organize the list based on those details.
            </li>
            &nbsp;<br>
        </ol>
    <li><a href = "#student_finances">Student Finances</a>
    <br>For this portion of the application, the student may view financial information such as outstanding tuition payments, current personal account balance, linking a bank account to the personal CaldenarCompanion account, or depositing funds into the CalendarCompanion account with a credit card. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
    <ol style = "list-style-type: upper-alpha">
            <li><a href = "#tuition_and_account_balance">Tuition and Account Balance</a>
            <br> This component is a child to Student Finances, and it allows a user to view a quick summary of their tution account, included balances and recent payments. In addition, the student may view balances of linked bank accounts or ONECard (or similar) accounts.
            </li>
            &nbsp;<br>
            <li><a href = "#one_card_account">ONECard Account (or similar)</a>
            <br> Here is a detailed summary of a users ONECard account. This view allows a user to observe the current balance, the last tranasaction made including where and when, and also allows deposits to be made via linked bank account or a credit card.
            </li>
            &nbsp;<br>
            <li><a href = "#link_bank_account">Link Bank Account</a>
            <br> Here a user may link an outside financial institution to their CalendarCompanion account so that tuition payments can be made directly from the users bank. In addition, a linked bank account can be used to fund a ONECard account.
            </li>
            &nbsp;<br>
            <li><a href = "#make_payment">Make Payment</a>
            <br> In this component, we see an interface to a university's tuition payment system. This view shows current balance, last amount paid. It allows a user to choose to account from which to make a payment. Following a payment transaction, a user will observe a receipt which they can e-mail or print. <b>//TODO add e-mail & print button to payment mockup</b>
            </li>
            &nbsp;<br>
        </ol>
    <li><a href = "#user_account">User Account</a>
    <br>Here we have the CalendarCompanion user account component. This page is parent to four tabs, which are subcategories of the User Account: personal information, account information, and preferences. The User Account is a central location for CalendarCompanion account information, UVic (or other school) account information, and CalendarCompanion application preferences. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
    <li><a href = "#help">Help</a>
    <br>In case a user requires any assistance, CalendarCompanion has it covered. The help section is home to section definitions, frequently asked questions, reporting bugs, and parent to a tutorial section. <a href = "#top">[top]</a>
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#calendar_companion_tutorial">CalendarCompanion Tutorial</a>
            <br>In this section, a user can select from a list of tutorials for the most common sequence of actions that a user might take while utilizing CalendarCompanion. The tutorial section is based on a step-by-step walkthrough style approach where a user would tap buttons and complete actions along the way while a tutorial bubble or arrow system tells them what to do next and why.
            </li>
            &nbsp;<br>
        </ol>
</ol>
</div>
&nbsp;<br>
&nbsp;<br>

---

&nbsp;<br>
&nbsp;<br>


<!-- Design Decisions and Rationale
Requirement from Phase 1
Low Fidelity Prototype
Behavior -->


<div id = "design_details">
<div markdown = "1">
# Design Details and Specifics
</div>
</div>


<div id = "login_page">
<div markdown = "1">

## Login Page

### Design Decisions and Rationale
&nbsp;&nbsp;&nbsp;&nbsp;The design of the login page was fairly straightforward. It's best to take advantage of the most common login page layout since most people are familar with these kinds of pages given the influx of mobile applications that require accounts in recent years. The decision to include sections such as "forgot password", "remember me", "sign up" was an easy one. These design patterns are helpful and well known. 

### Requirement from Phase 1
&nbsp;&nbsp;&nbsp;&nbsp;This is an implicit requirement from Phase 1. For any users to interact with a mobile application that requires specific knowledge and recordkeeping for one student, the requirement for a login page was not a question. This requirement is met in our design.

### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>

### Behavior
The CalendarCompanion application is displayed as a splash screen while the applicaiton is loading. Once loaded, ”Welcome to CalendarCompanion, please log in!” is displayed to the user. The user is provided with two text boxes into which they will add their netlink id and password. This is done via software keyboard that pops up when a user clicks the field. A "Remember Me" checkbox below the id and password fields is available so that a user does not have to keep filling in the information after they log out or the session expires and the application is restarted.

One of two things will happen after a use attempts to log in with credntials. In both cases, a dialog box will pop up telling user either that "this device will be trusted so that future logins are not required" or "credentials not recognized, redirecting to account creation page" at which point the user will be directed to an external site, which will be the sign up page on the UVic (or similar) website.

This rederiction will open the preffered browser of your phone system. For example, Chrome or Safari.

A "Create Account" button will be visible at the bottom of the login screen, which will lead a user who clicks it to the the "Create Account" page. Once on the create account page, the user will have see the "Virtual Assistant" AI chat bot on a bottom portion of the screen. There will be a "forgot your password" link as well, which will lead them to a password recovery screen. 

Once logged in successfully, a user will be directed to the home screen which is a parent screen that displays all of the main options for the user. These options are available as buttons with descriptions, and are detailed in the following sections.

</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "course_schedule">
<div markdown = "1">
## Course Schedule
### Design Decisions and Rationale
This is simply a landing page that one is directed to after one had clicked the "Course Schedule" button or link from the home page, or was directed here with a link provided by the Virtual Assistant. There is no specific interface metaphor that was followed for this page. The widgets present are simply links to the child pages categorized under Course Schedule. These links are submenus with descriptions titled "Future Courses", "Weekly Timetable", "Create Degree Map", and "My Degree Map".

### Requirement from Phase 1
This component forms part of the design behavior that directly fulfills a requirement from Phase 1: <a href = "../content/phase1/2019-02-19-userreqs.html" target = "_blank">User Requirements, Student, Paragraph 3</a>; *"The student has the option to modify or fine tune the semesters in order to obtain the perfect schedule for each studying term..."*

### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>

### Behavior
The behavior of this component is quite simple. A user clicks one of the buttons and is directed to the appropriate link.

</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>



<div id = "future_courses">
<div markdown = "1">

## Future Courses

### Design Decisions and Rationale
This section was designed with question, answer, and response in mind. Once in this section, a user will be presented with two questions which will assist the application in narrowing down the correct response and routing. These questions follow an interface metaphor based on binary decision making model. While most users typically do not define their daily decisions as binary, such decisions are intuitive for most people to understand because we in fact make such decisions every day. In addition, it can be helpful to simply respond to questions that an application asks of a user and trust that it will respond in the correct way. This section will provide a user with the ability to browse the most up to date lists of future courses that UVic has to offer. This component will also provide the user with the ability to browse and look at the current online correspondence courses that UVic offers to students. 

### Requirement from Phase 1
This component forms part of the design behavior that directly fulfills a requirement from Phase 1: <a href = "../content/phase1/2019-02-19-userreqs.html" target = "_blank">User Requirements, Student, Paragraph 3</a>; *"The student has the option to modify or fine tune the semesters in order to obtain the perfect schedule for each studying term..."*

### Low Fidelity Prototype

<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>

### Behavior
During the process of browsing through future courses, CalendarCompanion will first query the user with two questions in order to narrow down search results resulting in less confusion due to refined results. By establishing available courses in specific sessions (Summer/Fall/Spring), and what year the user would like to take a course in, the application can rule out courses that would be otherwise unavailable. The questions are: <br>
1. What term (Summer/ Fall / Spring) are you interested in? This is done because not all courses are offered in every tearm.<br>
2. What year are you interested in? This is done because some courses are scheduled to be eliminated or replaced in future years. By specifying the year, the application can further narrow down the available courses to display.

Following the initial questioning, users will be prompted to click a “search courses” button. This button takes the user to the page of results.
		
**Note**: there is a left facing arrow in the uppermost left corner of the phone screen. When clicked, the arrow will navigate uesrs to the previous menu. 	In addition, there will be a small question mark in the top right of the screen which, when clicked, opens a pop up dialog that will tell users what the left facing arrow is for.

Next, the application will analyze selected queries and display a grid of faculties that students can tap on. Above the grid a message displayed will read, “Select a faculty to browse courses offered during *First query response** in the year *Second query response*.”

The question mark and left facing arrow will also be present, except the question mark will explain as well that this screen is the faculty navigator/selector and that the user may tap on a faculty to see offered courses.

Next, A list of courses ordered numerically from introductory to thesis level will appear alongside their respective course title. This list may be long and user will have the functionality to scroll down to browse the list. 

Above the list it says “*Faculty chosen*"  courses for “*Query 1 response* ” session in "*Query 2 response.*”

Again the question mark in the top right, and left facing arrow in the top left will be available. The left facing arrow will transport the user to the faculty navigator/selector. The question mark will expand to a message explaining that these are the following courses available for the faculty in the respective session and year chosen. As well, the question mark will advise the user that they can tap any course for more information.

The courses displayed will have a “tap” interactive option, where users may tap on any course to discover course information such as<br>
1. Course summary
2. Sessions and years course is offered.
3. Requirements (third year standing, etc)
4. Prerequisites 
5. Corequisites 
6. Notable professors to teach the course and their profiles. (hyperlinked)
7. Peer reviews of course experience. (hyperlinked)

Again, users may use the upper leftmost corner to navigate back towards the list of courses available for specific faculty/session/year. However the question mark will offer tons of support, so much so that a message will appear next to the question mark on this page. The message reads important information:

“This is the course of information page of *course chosen* for the *faculty chosen for *query 1* session(s) in *query 2*”
“Please keep in mind that courses will have specific requirements. Examples range from a minimum year standing to a certain minimum mark achieved in a prerequisite course. ”

After a user has tapped on a specific course, they will notice information about specific courses. Most notably, prerequisite and corequisites. 

At the bottom of the scrolling list users will encounter a button widget which returns them back to the main menu. This button is titled “return”


</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>




<div id = "weekly_timetable">
<div markdown = "1">
## Weekly Timetable
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "create_a_degree_map">
<div markdown = "1">
## Create a Degree Map
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "my_degree_maps">
<div markdown = "1">
## My Degree Maps
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "study_assistant">
<div markdown = "1">
## Study Assistant
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "assignment_alarm">
<div markdown = "1">
## Assignment Alarm
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "study_tips_and_tricks">
<div markdown = "1">
## Study Tips and Tricks
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "test_reminders">
<div markdown = "1">
## Test Reminders
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "todo_check_list">
<div markdown = "1">
## Checklists and Todolists
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "map">
<div markdown = "1">
## Maps
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "school_events">
<div markdown = "1">
## School Events
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "find_my_prof">
<div markdown = "1">
## Find My Prof
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "contact_info_and_office_hours">
<div markdown = "1">
## Professor Contact and Office Hours
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "professor_ratings">
<div markdown = "1">
## Professor Ratings
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "student_finances">
<div markdown = "1">
## Student Finances
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "tuition_and_account_balance">
<div markdown = "1">
## Tuition and Account Balance
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "one_card_account">
<div markdown = "1">
## ONECard Account (or similar)
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "link_bank_account">
<div markdown = "1">
## Link Bank Account
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "make_payment">
<div markdown = "1">
## Make Payment
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "user_account">
<div markdown = "1">
## User Account
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "help">
<div markdown = "1">
## Help
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>


<div id = "calendar_companion_tutorial">
<div markdown = "1">
## Calendar Companion Tutorial
### Design Decisions and Rationale
### Requirement from Phase 1
### Low Fidelity Prototype
<center><img src = "./images/LinkBankAccount.png" width = "35%" height = "35%"/></center>
### Behavior
</div>
<a href = "#top">[top]</a>
</div>