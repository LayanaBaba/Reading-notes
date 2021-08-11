# Room

## Save data in a local database using Room
- The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. Room provides the following benefits: 
1. Compile-time verification of SQL queries.
2. Convenience annotations that minimize repetitive and error-prone boilerplate code.
3. Streamlined database migration paths.

To use Room in your app, add the following dependencies to your app's build.gradle file:

    dependencies {
    def room_version = "2.3.0"

    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"

    // optional - RxJava2 support for Room
    implementation "androidx.room:room-rxjava2:$room_version"

    // optional - RxJava3 support for Room
    implementation "androidx.room:room-rxjava3:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // optional - Test helpers
    testImplementation "androidx.room:room-testing:$room_version"

    // optional - Paging 3 Integration
    implementation "androidx.room:room-paging:2.4.0-alpha04"
    }

**Primary components**    
There are three major components in Room:

* The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
* Data entities that represent tables in your app's database.
* Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

## Defining data using Room entities
**Anatomy of an entity**
- You define each Room entity as a class that is annotated with `@Entity`.
**Define a primary key**
- Each Room entity must define a primary key that uniquely identifies each row in the corresponding database table. The most straightforward way of doing this is to annotate a single column with `@PrimaryKey`. 
**Define a composite primary key**
- You can define a composite primary key by listing those columns in the `primaryKeys` property of `@Entity`.

## Define relationships between objects
**Create embedded objects**
You'd like to express an entity or data object as a cohesive whole in your database logic, even if the object contains several fields. In these situations, you can use the `@Embedded` annotation to represent an object that you'd like to decompose into its subfields within a table. 

**Define one-to-one relationships**
A one-to-one relationship between two entities is a relationship where each instance of the parent entity corresponds to exactly one instance of the child entity, and vice-versa.
You should add a method to the DAO class that returns all instances of the data class that pairs the parent entity and the child entity. This method requires Room to run two queries, so add the @Transaction annotation to this method to ensure that the whole operation is performed atomically.

## Accessing data using Room DAOs
**Anatomy of a DAO**
You must always annotate your DAOs with `@Dao`. DAOs don't have properties, but they do define one or more methods for interacting with the data in your app's database.
There are two types of DAO methods that define database interactions:

- Convenience methods that let you insert, update, and delete rows in your database without writing any SQL code.
- Query methods that let you write your own SQL query to interact with the database.