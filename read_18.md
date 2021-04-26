# Web App Security

## Many to Many

many to many relationships between two tables, like a student and a course, where the student can have many courses and each course can have many students

for this type of relationships a new table is created, this table holds the primary key of the course and the primary key of the student and it is used as a reference

### Database 

```sql
CREATE TABLE student  (
  `student_id` int(11) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(50) DEFAULT NULL,
  `last_name` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`student_id`)
);

CREATE TABLE `course` (
  `course_id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`course_id`)
);

CREATE TABLE `student_course` (
  `student_id` int(11) NOT NULL,
  `course_id` int(11) NOT NULL,
  PRIMARY KEY (`student_id`,`course_id`),
  KEY `course_id` (`course_id`),
  CONSTRAINT `student_course_ibfk_1` 
   FOREIGN KEY (`student_id`) REFERENCES `student` (`student_id`),
  CONSTRAINT `student_course_ibfk_2` 
   FOREIGN KEY (`course_id`) REFERENCES `course` (`course_id`)
);
```

### The model in Spring

**Student**

```java
@Entity
@Table(name = "Student")
public class Student { 
    // ...
 
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Student_Course", 
        joinColumns = { @JoinColumn(name = "student_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "course_id") }
    )
    Set<Course> courses = new HashSet<>();
   
    // standard constructor/getters/setters
}
```
**Course**

```java
@Entity
@Table(name = "Course")
public class Course {    

    @ManyToMany(mappedBy = "courses")
    private Set<Student> students = new HashSet<>();
    
    // standard constructors/getters/setters   
}
```

