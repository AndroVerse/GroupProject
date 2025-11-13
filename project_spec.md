# **CourseMatch**

## Table of Contents

1. [App Overview](#App-Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
1. [Build Notes](#Build-Notes)

## App Overview

### Description 

** Is an academic planning tool that empowers students to discover valid course substitutions aligned with their degree requirements. By streamlining discovering and integrating institutional curriculum data, reduces advising bottlenecks, and improves graduation outcomes.**

### App Evaluation

<!-- Evaluation of your app across the following attributes -->

**Gia's 3 App Ideas**

**WellPet**

- **Category: Lifestyle / Social **
- **Mobile: Used to log pet activities, vet visits, and share cute moments**
- **Story: Owners track health, behavior, and milestones while connecting with other pet lovers**
- **Market: Pet owners, vets, pet product brands**
- **Habit: Weekly logging and sharing**
- **Scope: V1: Pet profile and journal → V2: Health reminders → V3: Social feed → V4: Vet integration**

**MoodMusic**
- **Category: Wellness / Entertainment **
- **Mobile: Used to log moods and receive music recommendations**
- **Story: Users reflect on their emotions and get curated playlists to boost or balance their mood**
- **Market: Teens, young adults, mental health advocates**
- **Habit: Daily check-ins and listening**
- **Scope: V1: Mood logging → V2: Music integration → V3: Journaling → V4: Therapist dashboard**

**CourseMatch**
- **Category: Education / Academic Planning **
- **Mobile: Mobile is essential for quick access during advising sessions, registration periods, and on-the-go curriculum checks. Students can instantly search for course substitutions and view details from their phones.**
- **Story: Helps students stay on track for graduation by identifying valid substitution courses when their preferred or required courses are unavailable. Empowers students to make informed decisions and reduces advising bottlenecks.**
- **Market: College and university students, academic advisors, and registrar offices. Institutions can license the app for integration with their curriculum systems or offer it as a student support tool.**
- **Habit: Students use the app during course registration, advising appointments, and when planning their semester schedules. Advisors may use it daily during peak advising seasons**
- **Scope: V1 allows students to input a course name/code and view dummy substitution data. V2 adds filtering by department, credit hours, and semester availability. V3 integrates with real curriculum databases or APIs. V4 introduces advisor-facing tools and multi-campus support.**

## Product Spec

### 1. User Features (Required and Optional)

**Required Features:**

- Course Input: Allow students to input a course name or code.

- Substitution Search: Instantly find and display valid substitution courses.

- View Basic Course Details: Show the substitution's course code, name, credits, and any relevant notes.

- Local Dummy Data: The app will run on a local "dummy" database (per V1 and the provided code) for initial functionality and testing.

**Stretch Features:**

- Live Curriculum Integration: Connect to real university APIs or databases to fetch real-time course offerings, substitution rules, and availability (V3).

- Advanced Filtering: Allow students to filter substitution results by department, credit hours, semester availability, and course level (100-400) (V2).

- Student Profile & Personalization: Enable students to create profiles with their major, minor, and completed courses to receive personalized suggestions aligned with their degree audit (V3).

- Advisor Collaboration Tools: Create an advisor-facing dashboard where they can add custom notes, "endorse" substitutions, approve student choices, and chat with students in-app (V2/V3).

- Expanded Course Details: Add more comprehensive fields to the course details view, including prerequisites, full course descriptions, instructor names, and delivery mode (online/hybrid) (V2).

- Multi-Campus/Institution Support: Add a campus/institution selector to filter substitutions based on campus-specific offerings and rules (V2/V3).

- Smart Search: Enhance the search functionality with autocomplete for course names, fuzzy matching for typos, and a "recent searches" history (V2).

- AI-Powered Suggestions: Use machine learning to recommend substitutions based on past student choices and predict course demand (V3).

- Analytics Dashboard: Provide a backend dashboard for advisors and registrars to track usage trends, most-searched courses, and common substitutions (V2).

- Mobile Notifications: Send push notifications and reminders for registration deadlines, advisor approvals, or new substitution options (V3).

### 2. Chosen API(s)

Find Substitution: User can search for a course by its code or name.

User enters a course code (e.g., "CS101") OR a course name (e.g., "Intro to Programming")

=> Results display the matching substitution ("CS105 - Python Fundamentals").

User enters a course code that has no match (e.g., "BIO999")

=> Results display "No substitution found."

Find Substitution (V2): User can filter substitution results by department, credits, semester, or course level.

User enters a course code (e.g., "MATH201")

=> Results display all valid substitutions.

Find Substitution (V2): User can sort substitution results.

User searches for a course and gets multiple results

=> Results are displayed by default (e.g., by best match).

User chooses sort by "Course Level"

=> Results are re-ordered to show 100-level, then 200-level courses, etc.

View Departments (V2): User can search for all courses/substitutions within a specific academic department.

User selects "Computer Science" from a department list or dropdown

=> A list of all CS courses and their known substitutions is displayed.

Save Substitution (V3): User can save favorite or potential substitutions.

User finds a substitution they are interested in

=> User taps a "Save" or "Favorite" icon.

=> The course information ("CS105 - Python Fundamentals") is added to a "Saved Courses" list for later review.

### 3. User Interaction

Required Feature

- Student searches for a valid course

  - Student enters "CS101" or "Intro to Programming" into the input fields and taps "Find Substitution".

  - The app displays the substitution details: "Substitute Course: CS105 - Python Fundamentals\nNotes: Same credit, different language".

- Student searches for an invalid course

  - Student enters "BIO999" into the input fields and taps "Find Substitution".

  - The app displays the message: "No substitution found."

## Wireframes

<!-- Add picture of your hand sketched wireframes in this section -->
<img src="YOUR_WIREFRAME_IMAGE_URL" width=600>

### [BONUS] Digital Wireframes & Mockups

Screen 1: Search (Default State)

+--------------------------------------+
| =  CourseMatch                        |
+--------------------------------------+
|                                      |
|   [ Enter Course Code ]              |
|                                      |
|   [ Enter Course Name ]              |
|                                      |
|                                      |
|        [ Find Substitution ]         |
|                                      |
|                                      |
|                                      |
|                                      |
|                                      |
|                                      |
+--------------------------------------+


Screen 2: Search (Result State)

+--------------------------------------+
| =  CourseMatch                        |
+--------------------------------------+
|                                      |
|   [ CS101           ]              |
|                                      |
|   [ Intro to Programming ]           |
|                                      |
|                                      |
|        [ Find Substitution ]         |
|                                      |
|   ---------------------------------- |
|                                      |
|    Substitute Course:                |
|    CS105 - Python Fundamentals       |
|                                      |
|    Notes: Same credit, different     |
|    language.                         |
|                                      |
+--------------------------------------+


### [BONUS] Interactive Prototype

For V1, the interaction is very straightforward:

User Action: Taps on the "Enter Course Code" or "Enter Course Name" fields.

Result: The keyboard appears, and the user can type.

User Action: Taps the "Find Substitution" button.

Result (if match): The resultView TextView (the area below the button) is populated with the substitute course code, name, and notes.

Result (if no match): The resultView TextView is populated with the text "No substitution found."

## Build Notes

Here's a place for any other notes on the app, it's creation 
process, or what you learned this unit!  

For Milestone 2, include **2+ Videos/GIFs** of the build process here!

## License

Copyright **2025** **Gasenia Caraballo**

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
