
**Course**

A course is content provided in sequence, broken down in modules, open for enrolment and completion for a duration. You can attach prerequisites for a course, and it may contain assessments. It is an illustration of content that comprises of the contextual information like the duration of course, type of delivery, organization offering the course, faculty, etc. The course becomes available for Sunbird users based on above contextual information.
 
**Course Management**

An organization or a user, with course creation privileges, creates and launches a course in Sunbird. 
The course content, structure, information and metadata of the course are stored in Sunbird platform. The platform empowers vast flexibility in course creation, delivery and consumption. Information like the start & end dates of the course, type of the course, user & organization who created the course, etc., is stored in the course entity at Sunbird layer. A course is visible to users only when the course is in Live state. The course creator change the status. There is no versioning of courses in Sunbird. Versioning is prime function of Sunbird platform itself.
The course entity in Sunbird is designed around the following objects and attributes.
- Course Id,Content Id,Version,Created By,Organization Id,Faculty Id, Tutors,Course Type, etc.

**User Courses** 

Users in Sunbird can explore and subscribe for the Live courses. Once subscribed, the user’s progress and activity within the course is stored in user courses entities. User courses contains the subscription data, progress, grade & current position of the user in a course. User Content State and User Assessment Items, data gets populated by listening to the telemetry events generated by the client applications. Asynchronous back-end jobs listening for updates on User Assessment Items and User Content State updates the progress, grade and last position in the course for each user’s course subscription.
User courses entity in Sunbird is designed around the following objects and attributes:
- User Id,Course Id,Delta-TOC,Progress,Grade,Last Content Id.

**User Content State**

It contains the consumption details of content (inside or outside a course) by a user. User Content State entity in Sunbird is designed around the following objects and attributes: 
- User Id,Content Id,Course Id, Consumption Status,Score,Result,Grade,View Count,Completion Count,etc.