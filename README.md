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

In the "Enrollment List" for each student, a list of unregistered courses and a list of registered/passed courses divided by semester (depending on the student's status) are displayed.

The appearance and functionalities of the enrollment list are the same for students and administrators (except for the menu at the top of the page). The menu for students will have only the "logout" item and will display only the corresponding enrollment list. The menu for administrators will include "logout," "subjects," "students," and "professors," which will provide access to other views.

Professors in the top menu will have the "subjects" (showing the courses they are responsible for) and "logout" items. By selecting each individual course, they can view the students who have enrolled in it and their statuses.

The code must be developed within the Django framework. Implement and organize the code according to the MVC (MVT) architecture. It is mandatory to have a structure that can be relatively easily extended with minor additional functionalities (e.g., adding and displaying the total number of enrolled ECTS credits).

Functionality and security are key aspects, but usability of the interface and code organization will also be evaluated.

![Capture](https://github.com/user-attachments/assets/49995c4d-555f-43d7-95d9-835d85c168d4)

![Capture1](https://github.com/user-attachments/assets/2ca60921-ce5c-407c-b452-9530696f9119)

![Capture3](https://github.com/user-attachments/assets/5d8fc03f-4a46-49ce-a9cd-cc80f2aa2b51)

![Capture33](https://github.com/user-attachments/assets/1a082ace-9b9c-4c17-a95c-3209b1b81929)

![Capture4](https://github.com/user-attachments/assets/3e838e3f-2790-4fb6-919f-7952ea2d550e)

![Capture](https://github.com/user-attachments/assets/e795c1c9-231b-41cb-9733-d4e393cebde6)

![Capture1](https://github.com/user-attachments/assets/157b938b-15ad-44b8-903e-593c93f390ae)

![Capture2](https://github.com/user-attachments/assets/24b5c6cc-3339-4262-9873-4ca3ea5befea)

![Capture4](https://github.com/user-attachments/assets/7d81dc1f-61f5-4107-8a8a-3be3f22b0b92)

![Capture5](https://github.com/user-attachments/assets/3aaf43fc-46fa-4aa1-a08b-dabcb274f00e)
