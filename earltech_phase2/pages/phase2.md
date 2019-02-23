---
layout: default
title:  "Phase 2"
date:   2019-02-23 09:00:00 -0800
categories: phase2
---

# Phase 2: Design

&nbsp;&nbsp;&nbsp;&nbsp;Welcome to the design portion of the CalendarCompanion application. Here we will discuss the design details surrounding a mobile implementation of Calendar Companion. We will provide design decisions, details, and prototypes.

&nbsp;&nbsp;&nbsp;&nbsp;This document serves to provide an overview of the design phase of the CalendarCompanion application. We will first provide a high level hierarchical overview and short description of each component in our design proposal. Next, each component will be be described in detail; each section will include a short component description, rationale for the design decisions of the component (interface metaphors, widget choices, etc), plus how that portion of the design fulfills a requirement based on data gathered in Phase 1. Finally, each component section will include a low fidelity prototype, and a detailed description of the behavior of each component widget.

&nbsp;&nbsp;&nbsp;&nbsp;Using this document, a developer should be provided with enough detail that the application could be made with little to no additional guidance from the designers of the application. The Earl Technologies team is please to present the CalendarCompanion prototype and design document.

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
                <li><a href = "#link_bank_account">Link Bank Account</a></li>
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
<div id = "high_level_overview">
<div markdown = "1">
# Hierarchical overview
</div>
<ol>
    <li><a href = "#login_page">Login Page</a>
        <br>This is a standard login page that will display a CalendarCompanion logo. This page is allows a user to enter a netlink (or similar) ID, and their password. This page will display standard options typical in a mobile application login page; options such as forgot password, forgot account name, remember me, signup, etc. A successful sign in here will direct the user the application home page that contains links to course schedule, study assistant, map, school events, find my prof, student finances, user account, and help. All interaction in this application is done via touch screen interaction.
    </li>
    &nbsp;<br>
    <li><a href = "#course_schedule">Course Schedule</a>
        <br>This page acts as a parent to other sections related to scheduling. This page will be home to four submenus. Underneath each submenu will be a subtitle which explains what it's use is. In addition, students may scroll down to see to see all submenus in cases where they menus do not fit on the device screen.
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
            <br>
            &nbsp;<br>
            </li>
        </ol>
    <li><a href = "#details">Study Assistant</a>
    <br>
    <br>sdas
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#assignment_alarm">Assignment Alarm</a>
            <br>
            </li>
            &nbsp;<br>
            <li><a href = "#study_tips_and_tricks">Study Tips and Tricks</a>
            <br>
            </li>
            &nbsp;<br>
            <li><a href = "#test_reminders">Test Reminder</a>
            <br>
            </li>
            &nbsp;<br>
            <li><a href = "#todo_check_list">Todo/Check List</a>
            <br>
            </li>
            &nbsp;<br>
        </ol>
    <li><a href = "#map">Map</a>
    <br>
    </li>
    &nbsp;<br>
    <li><a href = "#school_events">School Events</a>
    <br>
    </li>
    &nbsp;<br>
    <li><a href = "#find_my_prof">Find My Prof</a>
    <br>
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#contact_info_and_office_hours">Contact Info and Office Hours</a>
            <br>
            </li>
            &nbsp;<br>
            <li><a href = "#professor_ratings">Professor Ratings</a>
            <br>
            </li>
            &nbsp;<br>
        </ol>
    <li><a href = "#student_finances">Student Finances</a>
    <br>
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#link_bank_account">Link Bank Account</a>
            <br>
            </li>
            &nbsp;<br>
        </ol>
    <li><a href = "#user_account">User Account</a>
    <br>
    </li>
    &nbsp;<br>
    <li><a href = "#help">Help</a>
    <br>
    </li>
    &nbsp;<br>
        <ol style = "list-style-type: upper-alpha">
            <li><a href = "#calendar_companion_tutorial">CalendarCompanion Tutorial</a>
            <br>
            </li>
            &nbsp;<br>
        </ol>
</ol>
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "login_page">
login page
Integer eu tellus ut leo pellentesque tincidunt. Vivamus viverra pharetra congue. Nunc non ornare purus, vel mattis justo. Interdum et malesuada fames ac ante ipsum primis in faucibus. Fusce imperdiet mi eget maximus cursus. Donec tempor eros hendrerit risus venenatis, non consequat enim sodales. Nullam at rutrum massa.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "details">
details
Fusce euismod felis at leo vehicula malesuada. Vivamus convallis nisi ac lectus suscipit pellentesque sit amet sit amet lectus. Nulla facilisi. Morbi viverra leo lacus, non egestas ipsum placerat ut. Vivamus hendrerit elementum commodo. Aenean consectetur elit tellus, ut consectetur leo varius id. Suspendisse egestas justo ut lacinia dignissim.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "course_schedule">
course_schedule
In ac sapien posuere, hendrerit metus nec, vehicula ipsum. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nullam in fringilla mi. Pellentesque vestibulum ligula eget tortor hendrerit, et luctus augue ullamcorper. Aliquam at laoreet neque. Proin vel nisl nisi. Quisque et erat eu metus tempus tempus a convallis erat. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis molestie velit a lacinia placerat. Sed congue lectus magna, faucibus tincidunt turpis congue ut. Donec a magna a felis bibendum dictum sed nec lorem.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "future_courses">
future_courses
Ut elementum urna metus, ac condimentum sapien elementum at. Quisque eget posuere metus, id elementum ligula. Quisque eget maximus ipsum. Fusce facilisis at risus eget placerat. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Fusce a turpis sed risus efficitur ornare aliquam ac metus. Vestibulum ac feugiat purus. Vivamus scelerisque nisi vel purus hendrerit egestas. In ut nisi pretium eros facilisis posuere et ut felis. In faucibus, ipsum at malesuada tincidunt, quam justo condimentum nunc, at fringilla nulla elit in magna. Nullam viverra velit vitae neque volutpat, elementum feugiat justo scelerisque. Nullam laoreet felis metus, ut consequat odio posuere ac. Nullam ac mi elit.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "weekly_timetable">
weekly_timetable
Cras a urna vel purus varius condimentum. In maximus condimentum auctor. Sed aliquam ante ut hendrerit placerat. Nulla a gravida ante. Pellentesque non cursus lectus, eget rutrum dolor. Sed imperdiet felis eu pellentesque sodales. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Praesent mollis, ligula eu pellentesque volutpat, enim eros molestie ipsum, non aliquam ante felis in ipsum. Quisque vulputate risus orci, in consectetur libero ullamcorper et. Duis tristique ex enim, ac dignissim lectus facilisis vitae.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "create_a_degree_map">
create_a_degree_map
Integer eu tellus ut leo pellentesque tincidunt. Vivamus viverra pharetra congue. Nunc non ornare purus, vel mattis justo. Interdum et malesuada fames ac ante ipsum primis in faucibus. Fusce imperdiet mi eget maximus cursus. Donec tempor eros hendrerit risus venenatis, non consequat enim sodales. Nullam at rutrum massa.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "my_degree_maps">
my_degree_maps
Proin convallis ex et sapien rhoncus eleifend. Donec dignissim elit ut orci convallis molestie. Vestibulum ultrices malesuada leo, a tristique elit auctor non. Aliquam commodo rhoncus tellus sed dictum. Nunc eget neque vitae magna rutrum tincidunt at sit amet arcu. Ut facilisis ex a ultrices consectetur. Mauris et eros varius massa semper commodo ut eget est. Duis turpis augue, fermentum ut pharetra in, consequat eu ipsum. Maecenas mollis nec nibh non auctor. In at metus vitae mauris ultricies semper. Vivamus sapien dolor, fringilla ut convallis sit amet, venenatis nec turpis. Maecenas mattis mattis tellus a mattis. Phasellus risus libero, malesuada rutrum dui non, lacinia accumsan nulla.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "study_assistant">
study_assistant
Integer vel placerat enim. Maecenas a tortor vel eros efficitur lobortis. Nulla laoreet eros vel nisl eleifend, sit amet vehicula sem pretium. Phasellus iaculis, dui in semper scelerisque, velit risus laoreet arcu, a efficitur ante nisi fringilla libero. Vestibulum pulvinar hendrerit erat eu maximus. Etiam venenatis sit amet dolor eget posuere. Morbi pellentesque arcu fermentum sem tincidunt, id porttitor quam pellentesque. Donec rutrum lobortis enim, sit amet lobortis dolor laoreet vel. Maecenas rhoncus porttitor lacus, eu fermentum turpis varius sed. In hac habitasse platea dictumst. Morbi eu massa risus.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "assignment_alarm">
assignment_alarm
Fusce massa leo, aliquam non magna at, maximus elementum felis. Integer sit amet erat lectus. Mauris id vehicula arcu, a fermentum ante. Pellentesque ut velit at nulla hendrerit tempor. Maecenas ornare, mi eu eleifend tincidunt, elit turpis commodo augue, ut interdum ligula ante ut risus. Ut eget suscipit justo. Aliquam pharetra neque vitae placerat euismod. Nullam malesuada ultricies dignissim. Proin elementum nulla ipsum, eu viverra elit lacinia maximus. Nulla nulla ante, consequat cursus semper in, facilisis vitae felis. Cras id dui et nulla posuere tincidunt. Nullam faucibus est et tristique auctor. Integer rutrum accumsan lacus suscipit luctus. Cras dictum eros vel efficitur faucibus. Proin sollicitudin lacus nec hendrerit accumsan. Cras semper quis erat ac malesuada.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "study_tips_and_tricks">
study_tips_and_tricks
Quisque blandit varius tellus, ut gravida lorem. Aliquam eget nisi ac nulla rutrum feugiat. Sed eget accumsan ligula. Sed porta maximus augue non vulputate. Vestibulum fermentum eros justo, in sagittis tellus scelerisque in. Interdum et malesuada fames ac ante ipsum primis in faucibus. Donec erat felis, commodo vel consequat ac, finibus in mi. Sed volutpat fringilla lacinia. Sed consequat eget justo eget pulvinar. Aliquam accumsan scelerisque auctor. Mauris suscipit faucibus sem facilisis rhoncus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Quisque dui nulla, scelerisque sed sagittis eu, elementum id nulla. Fusce felis orci, posuere id mattis quis, maximus vehicula lectus. Cras sit amet sem sit amet ligula pretium ornare. Aliquam egestas felis quis nibh tempor, non aliquet lectus tristique.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "test_reminders">
test_reminders
In elit risus, mollis ac faucibus vel, faucibus ut sem. Nullam fringilla aliquam ex id bibendum. Aenean malesuada nibh ac nulla lobortis venenatis. Curabitur orci nibh, interdum non enim nec, rhoncus consectetur tortor. Aliquam a dolor non lorem fringilla euismod. Aenean eleifend urna sed purus scelerisque, ac ullamcorper dui faucibus. Proin imperdiet elementum metus. Praesent consectetur arcu ipsum, sed pellentesque urna malesuada sed. In pharetra ante ut sem faucibus vestibulum. Aenean at cursus metus. Phasellus nunc orci, aliquam vel consequat ut, commodo quis ipsum. Cras non diam lobortis, tristique risus non, facilisis erat. Suspendisse eu placerat ex, non scelerisque mi. Donec tincidunt, velit sed fermentum tincidunt, justo nunc porttitor dui, a facilisis est arcu sit amet lacus. Donec condimentum risus id quam pharetra, vel consectetur nisi vulputate. Vestibulum lacus metus, maximus fermentum ornare cursus, commodo eu purus.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "todo_check_list">
todo_checklist
Morbi in arcu eget metus hendrerit laoreet. Proin et ante orci. Mauris id euismod lacus. Donec cursus mauris eros, congue ultrices nunc pulvinar in. Quisque vitae lectus vitae est imperdiet condimentum. Donec nisl est, lobortis eu felis sed, sodales varius odio. Cras id dolor accumsan, blandit orci a, semper ante. Vestibulum vulputate sapien in odio efficitur, nec laoreet orci tristique. Aenean sit amet felis vel odio gravida vestibulum eu nec velit. Proin scelerisque vel nunc et aliquet. Nulla consectetur scelerisque diam ut ultrices. Praesent posuere mi augue, sit amet auctor turpis eleifend faucibus. Nulla imperdiet, tellus at blandit suscipit, purus odio feugiat justo, sed sollicitudin augue lacus a purus.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "map">
maps
Integer eget efficitur magna. Integer luctus magna velit, eu imperdiet tortor porttitor quis. Morbi non dui massa. Fusce cursus eros et ex mollis molestie. Duis interdum facilisis lorem ac condimentum. Nulla ut enim a urna luctus consectetur quis eu neque. Quisque lorem nisi, pulvinar id tortor et, euismod aliquet felis. Sed tincidunt sagittis magna, non molestie est pulvinar vitae. Praesent at nulla sapien. Quisque rutrum lacus sed nulla fringilla viverra. Donec eu tempus diam, vel sollicitudin purus. Nam aliquet ex a lectus pulvinar, ut gravida eros lobortis. Donec viverra felis nec est tincidunt tincidunt.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "school_events">
school_events
Vivamus auctor ultrices ex, ut efficitur magna sodales eu. In pretium accumsan eleifend. Maecenas blandit ligula sed ligula volutpat, nec placerat ante vulputate. Quisque quis diam vel tortor tempus ultricies et id purus. Integer bibendum risus vitae pulvinar volutpat. Pellentesque at accumsan elit. Nam pretium elit sit amet sollicitudin pharetra. In ornare eleifend sapien id vehicula. Vestibulum arcu nunc, dignissim ac porttitor vitae, tincidunt a odio. Donec dictum tellus eu tincidunt consequat.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "find_my_prof">
find_my_prof
Integer vitae orci ligula. Donec quis erat nisi. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Fusce a placerat est. Morbi egestas id sapien ut cursus. Phasellus mattis lorem turpis, et ullamcorper augue varius at. Vivamus cursus ultricies feugiat. Duis lobortis massa in posuere accumsan. Morbi volutpat suscipit interdum. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris est lacus, accumsan ut hendrerit ac, aliquet sit amet risus. Mauris in hendrerit magna. Sed luctus ligula eu nulla luctus, ut feugiat mauris hendrerit.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "contact_info_and_office_hours">
contact_info_and_office_hours
Sed eleifend tortor non quam suscipit pellentesque. Maecenas lacus velit, suscipit ac urna consectetur, volutpat suscipit dolor. Donec vulputate ante nec leo posuere convallis. Aenean vulputate consequat dui ac accumsan. Nam eu tristique nisi. Vivamus bibendum, lectus tincidunt pretium hendrerit, massa magna commodo massa, a mattis eros mauris sit amet neque. Integer rhoncus, lorem ac efficitur consectetur, massa elit auctor turpis, at egestas lorem est ac dolor. Etiam placerat nisl ac ante rutrum porta. Donec eu purus eleifend, accumsan libero a, suscipit ante. Donec dignissim fermentum fringilla. Fusce non tristique nulla. Donec massa diam, ullamcorper eu felis in, aliquam interdum ante. Duis id arcu vel orci fermentum tempor. Morbi orci sem, congue quis ultricies ut, laoreet eu tortor. Quisque at malesuada metus. Ut tempus congue est nec congue.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "professor_ratings">
professor_ratings
Nullam dapibus elit at imperdiet pretium. Aenean lorem tellus, fringilla vitae posuere eu, dictum pretium turpis. Fusce erat enim, ultrices vitae arcu sit amet, luctus ullamcorper nulla. Vestibulum porta magna suscipit ligula sodales, non vestibulum leo imperdiet. Nunc vestibulum dolor tortor, dapibus volutpat sem pretium at. Aenean interdum turpis non ante scelerisque condimentum. Pellentesque semper enim orci, nec convallis magna ultricies ut. Sed feugiat, nibh in tincidunt gravida, mi erat molestie elit, vel tempus nisl lacus id arcu.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "student_finances">
student_finances
Ut mollis turpis non fringilla mollis. Donec tincidunt est ut magna sodales imperdiet. Aliquam et facilisis neque. Cras sagittis magna nec augue fringilla, nec cursus arcu dictum. Phasellus pellentesque est ultrices turpis mattis convallis. Duis at luctus ante, id dictum urna. Aliquam et commodo dui. Integer quis tellus condimentum, luctus lectus rhoncus, tincidunt risus. Sed blandit risus ex, sed ornare massa dignissim sed. Suspendisse posuere sodales enim dignissim dictum. Fusce eget aliquam sem. Cras pulvinar non ligula et tincidunt. Vivamus rhoncus vel erat sed malesuada.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "link_bank_account">
link_bank_account
Vivamus eu tempus sem. In dictum hendrerit risus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus eget orci mi. Suspendisse fringilla dui tincidunt turpis volutpat laoreet. Sed volutpat odio non odio suscipit posuere. Donec at lorem mauris. Praesent volutpat pellentesque sem in consectetur. Donec at volutpat dui, convallis rhoncus tortor. Integer viverra ante tincidunt, rutrum neque a, ultrices nunc. Nulla ut hendrerit mauris.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "user_account">
user_account
Phasellus commodo neque ac aliquam interdum. Nulla non risus semper, rhoncus ipsum et, scelerisque lectus. Aenean euismod sed velit in fringilla. Cras convallis metus vitae dui maximus pulvinar. Suspendisse sed quam velit. Proin sit amet lacinia risus. Quisque pretium laoreet ipsum, nec porta diam pellentesque eget. Vivamus in ante ante. Nullam pharetra vestibulum ligula a rutrum. Morbi vitae diam pellentesque, fringilla lacus sit amet, tincidunt nunc. Donec ac dignissim lectus. Mauris volutpat gravida nunc. Curabitur consequat velit posuere augue euismod commodo.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "help">
help
Phasellus sed quam in arcu cursus rutrum id ut arcu. Aenean ac nisi eget ante lacinia volutpat. Ut maximus diam non accumsan consequat. Vivamus quis dapibus orci. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut fermentum ligula quis libero vulputate, et porta lorem placerat. Suspendisse vitae magna ullamcorper, accumsan neque vel, feugiat odio. Morbi congue tempus dui, quis egestas augue dignissim a. Donec efficitur convallis quam, at elementum orci varius vitae. Nam vitae odio lorem. Etiam ultricies quam ligula, sollicitudin aliquam lorem ornare vel. Morbi viverra massa leo, sed luctus augue egestas eu. In hac habitasse platea dictumst. Proin justo arcu, varius congue orci sit amet, ornare elementum lorem. Fusce lorem ligula, placerat nec luctus non, cursus ac dolor. Etiam mi justo, congue non commodo at, tempor quis orci.
<a href = "#top">[top]</a>
</div>
&nbsp;<br>
<div id = "calendar_companion_tutorial">
calendar_companion_tutorial
Donec ullamcorper nunc ac nisl auctor, et bibendum odio vulputate. Proin ac mauris commodo, semper turpis at, dictum erat. Donec sodales, augue suscipit pulvinar lacinia, urna ante finibus nisl, eget placerat ex nunc ut neque. In rhoncus ac est eget elementum. Sed ut pretium lacus. Etiam ut metus nec leo tincidunt pulvinar at vitae nibh. Pellentesque eget orci et lacus ornare suscipit eget vel tellus. Fusce arcu ligula, tincidunt non tellus pulvinar, tempus suscipit massa. Mauris a imperdiet nisi. Fusce id urna turpis. Cras bibendum ipsum sed pretium pulvinar. Suspendisse id diam diam. Quisque varius nisi lacus, sed egestas elit volutpat quis. Fusce id eleifend mi. Mauris in risus vel nisi viverra volutpat.
<a href = "#top">[top]</a>
</div>