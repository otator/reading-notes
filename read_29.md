# Room 

In case of saving persistent data, you can use the shared preferences which store *key-value* data but you also have another option, using a database.

Android offers a lite version of SQL called SQL lite to save data locally, this local database can store the online database data invorder to use the application in offline mode so that the user can still see the data need in the application.

To create a database you definately need to start from creating the database and its tables, adding the SQL statements that query, delete or update the data, and you will need alot of code to to convert between SQL queries and data objects. doing it this way is time-consuming and error-prone.

Android offers a library called **Room** to work will the database without the need to do all the above stuff.

To create a persistent database with tables and data access objects you need to do the following: 

1. Add the dependencies for the room library in `gradle.build` file

```groovy
  dependencies {
    def room_version = "2.3.0"
    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"
  }
```

2. create the table/entity class
the entity class must be annotated with `@Entity` annotation, and for the primary key column use the `@PrimaryKey`annotation, while `@ColumnInfo()` is for other tables to change their information.

```java
  @Entity
  public class Book {
      @PrimaryKey
      public int bid;

      @ColumnInfo(name = "author_name")
      public String authorName;

      @ColumnInfo(name = "book_title")
      public String bookTitle;
  }
```

3. Create the methods to do the CRUD operations.

this class must be an `interface` that marked with `@Dao` annotation (DAO: *Data Access Object*)

the abstract methods must be annotated with CRUD operation annotations such as `@Insert`, `@Delete`, and `Query` where you can pass any SQL statement.

```java
  @Dao
  public interface BookDao {
    @Query("SELECT * FROM book")
    List<Book> getAll();

    @Query("SELECT * FROM Book WHERE bid IN (:authorIds)")
    List<Book> loadAllByIds(int[] authorIds);

    @Query("SELECT * FROM book WHERE author_name LIKE :author AND " +
           "book_title LIKE :title LIMIT 1")
    Book findByName(String author, String title);

    @Insert
    void insertAll(Book... books);

    @Delete
    void delete(Book book);
  }
```

4. Create the Database Class

This class must be annotated with `@Database` annotation and passing all the entities as an array for this annotation.

This class must be `abstract` and extend the `RoomDataBase` class.

Each entity/table must be written as an abstract method of type Dao inside this class


```java
  @Database(entities = {Book.class}, version = 1)
  public abstract class AppDatabase extends RoomDatabase {
      public abstract BookDao bookDao();
  }
```

**Now run the following code to create the database**

```java
  AppDatabase db = Room.databaseBuilder(getApplicationContext(),
        AppDatabase.class, "library").build();
```

now you are able to perform the CRUD operations on the database

```java
  BookDao bookDao = db.bookDao();
  List<Book> allLibraryBooks = bookDaoDao.getAll();
```