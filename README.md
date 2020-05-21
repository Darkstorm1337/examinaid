# CITS3403 Project 2 - ExaminAid
*Semester 1, 2020*

## Overview

**ExaminAid** is a UWA Computer Science assessment preparation application containing various resources in the form of test questions and answers. The application is accessible to anyone who creates an account on the server where ExaminAid is running and contains all the question sets available to users. ExaminAid is completely free and has an intuitive and simple-to-use user interface for everyone, both students and teachers. The creators of ExaminAid welcome any feedback via the contact form on the ExaminAid website.

## Design and Development

Every question set supported by our application has a different combination of question types; the 3 main question types supported by our application include **multiple choice**, **short answer**, and **open answer** questions. Each question set is represented by a JSON file which contains information about the unit, including the unit code, and unit name, as well as the total number of marks, alongside the actual questions themselves. For the question sets that are supported by default, **immediate feedback** is available for most multiple choice and short answer questions, and the option for **custom feedback** is available on open answer questions. More information about this is provided in the paragraph on accounts.

There are 2 types of accounts users can have. By default, upon signing up to our application, users are granted a **student** account, which can view question sets, take tests and view the results of past tests. However, **administrators** are not only able to view question sets, but are also able to mark open answer questions, as well as manage, add and delete users. User accounts are switched between administrator and student permission levels via the command line; no account is able to make this change in the main application interface for security reasons. The **USEFUL.md** document outlines the commands available to developers wishing to explore this functionality. Similarly, any pages that require administrator-level access will redirect when a user who is not an administrator attempts to access the page; this includes student accounts and logged-out users. ExaminAid does **not** store passwords in plain text. Rather, the backend database stores salted and hashed strings that represent these passwords. When a user log into our application, the password they enter is checked against this string.

Administrators also have the ability to add new question sets.

ExaminAid also has a contact form, as mentioned above. This form is a HTML form which sends data to Google Sheets; the sheet which receives this data is available [here](https://docs.google.com/spreadsheets/d/1tRqt7958lMhJuw4GvrrazpACogWdf6A6B2dD_zZ_HmE/edit?usp=sharing).

## Features


## Authors
- [Bruce How](https://github.com/brucehow)
- [Lachlan D Whang](https://github.com/ForsakenIdol)
- [Paul O'Sullivan](https://www.github.com/paulosllvn)
- [Bryan Yeo](https://github.com/Darkstorm1337)