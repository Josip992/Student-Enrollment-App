# Student-Enrollment-App
Python/Django full stack seminar task from the 'Web Development' course at University Department of Professional Studies 

Project Task
Develop a system for student enrollment. The system will consist of three roles: student, professor, and administrator.



Administrator Role:

Authentication

View and modify the list of subjects

Add new subjects

Assign subjects to professors

View the list of students

Add and edit students

Create/modify enrollment records for any student

View the list of professors

Add and edit professors

View the list of students for each individual subject (add a link “View Student List” for each subject)

The Django admin system cannot be used for the administrator role


Professor Role:

Authentication

View the list of subjects for the logged-in professor

View the list of students for each subject (where the logged-in professor is the course leader)

Change the status of subjects (by default, the status is "enrolled" and can be changed to "passed" or "lost signature". The subject can be removed as long as its status is not changed to "passed" or "lost signature")

View students for each subject based on the following criteria:
Students who have lost the signature

Students who have obtained the signature but have not yet passed the subject

Students who have passed the subject


Student Role:

Authentication

Enroll/unenroll from subjects

All database changes should be performed through POST requests. Pay attention to application security (password encryption, SQL injection, and XSS). The database structure shown in the image below needs to be adapted to the requirements of this task.

You need to add a new table “roles” where the roles “admin”, “professor”, and “student” will be defined (modify the "role" column in the "users" table from "enum" type to a relation to the "roles" table). The "users" table differs from Django’s User table and needs to be adapted (see the lectures). Also, expand the "subjects" table with a column defining the course leader. This column will be a foreign key linked to the "users" table. On the application level, ensure that only users with the professor role can be set as course leaders.
