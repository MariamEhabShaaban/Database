
- chapter 6️⃣
    
    # The Relational Algebra and Calculus
    
    ## Relational Algebra
    
    - It is the basic set of operations for the relational model (schema)
    - These operation enable user to specify basic relatival request (Queries)
    - The output of every operation is a new relation!!!
        - We can use this new relation to do another operation on it
    - Relational Algebra Expression ⇒ sequence of relational algebra operations
    
    ### Relational Algebra Operation
    
    - Unary Relational Operations
        - Performed on one relation
        - Select ⇒ **σ**
            - Select subset of tuples (rows) from relation based on conditions (true || false, act as filter)
            - `σ c(R)`  c → condition, R → relation name
            
            ```
            σ (condition) (relation name)
            ```
            
            - EX:
                
                
                | **Name** | **Course** | **Grade** |
                | --- | --- | --- |
                | Alice | CS101 | A |
                | Bob | CS101 | B+ |
                | Alice | CS102 | A- |
                | Charlie | CS101 | A |
                | Bob | CS102 | B |
                
                **Input:**
                
                ```
                σ(Course = "CS101" AND Grade = "A")(Students)
                ```
                
                **Output:**
                
                | **Name** | **Course** | **Grade** |
                | --- | --- | --- |
                | Alice | CS101 | A |
                | Charlie | CS101 | A |
        - Project ⇒ π
            - It use to chose certain columns from relation
            - Vertical Partitioning
            - `πA (R)`
            
            ```
            π(attribute name, attribute name)(relation name)
            ```
            
            - A → attribute list, R → relation name
            - Delete repeated value R1 rows ≤ R rows
            - If we has an example of select and project → select first then project
            - EX:
                
                
                | **Name** | **Course** | **Grade** |
                | --- | --- | --- |
                | Alice | CS101 | A |
                | Bob | CS101 | B+ |
                | Alice | CS102 | A- |
                | Charlie | CS101 | A |
                | Bob | CS102 | B |
                
                **Input:**
                
                ```
                π(Name, Course)(Students)
                ```
                
                **Output:**
                
                | **Name** | **Course** |
                | --- | --- |
                | Alice | CS101 |
                | Bob | CS101 |
                | Alice | CS102 |
                | Charlie | CS101 |
                | Bob | CS102 |
        - Rename ⇒  **ρ**
            - It use to rename the output of a relation
            - **`ρ X (R)`**
            **`ρ StudentCourse (π course(Student))`**
            - EX:
                
                Student
                
                | **Name** | **Course** | **Grade** |
                | --- | --- | --- |
                | Alice | CS101 | A |
                | Bob | CS101 | B+ |
                | Alice | CS102 | A- |
                | Charlie | CS101 | A |
                | Bob | CS102 | B |
                
                **Input:**
                
                ```
                **ρ StudentCourse (π (Name,course) (Student))**
                ```
                
                **Output:**
                
                **StudentCourse**
                
                | **Name** | **Course** |
                | --- | --- |
                | Alice | CS101 |
                | Bob | CS101 |
                | Alice | CS102 |
                | Charlie | CS101 |
                | Bob | CS102 |
    - Relational Operations From set
        - Union ⇒ **∪**
            - Find the result set or combination of two or more tables.
            - R **∪ S**
            - R columns == S columns
            - The columns must have the same data types
            - The columns in each table must be in the same order.
            - No duplication
                
             ![image](https://github.com/user-attachments/assets/d9de8989-a25f-4be8-ade2-cb0c2c626558)

                
        - Intersection⇒  **∩**
            - Intersection between two relations
            - R **∩ S**
            - relation include all tuples are in R and S
            - The attribute name in R is the same in S
                
            ![image](https://github.com/user-attachments/assets/1848fdda-65db-414d-8b2a-f25477a7ed5b)
                
        - Difference ⇒ (minus) -
            - R - S ⇒ the Tuples in R but not in S
            
          ![image](https://github.com/user-attachments/assets/f457a9f3-5b77-4a90-8499-c2f187bff0b1)
            
        - Cartesian ⇒ Product X
            - R X S
            - Each tuple in R with all Tuples in S
            - R1 tuples  ⇒ R tuples * S tuples
            - R1 column ⇒ R column + S column
                
               ![image](https://github.com/user-attachments/assets/eb954d15-f339-451d-8b80-46eec78eada7)
    - Binary Relational Operations
        - Join ⇒ `⋈`
            - Performed on two relation with a condition
            - EquiJoin `⋈`
                - R1 ← R `⋈` (Dnumber == dno) S
                    - It called EquiJoin → two attributes have not the same name
                - It is combine related tuples from various relations
                - join == cartesian product operation + select operation
                - R1 columns = R columns + S columns
                
              ![image](https://github.com/user-attachments/assets/cfd9bcfb-aab1-4abe-9dec-1eebc6e1e85c)
                
                - In case no common attribute in two relation → try to find another relation has a common link between them
               
            - Natural Join *
                - In case the two attributes have the same name in tables
                - Don’t have to set a condition
                - R1 ← R * S
                
                - In case tables have more than one equal attribute
                    - Q ← R(A,B,C,D) * S(C,D,E)
                    - condition R.C == S.C && R.D == S.D
                    - Q(A,B,C,D,E) without repeat
        - Division ⇒ ÷
            - All
            - R ÷ S → S is the filter of my operation
                
               ![image](https://github.com/user-attachments/assets/20dae7b5-e088-4772-bd58-a09121d35a2a)
            - EX:
                
                **Table A: People**
                
                | PersonID | Name |
                | --- | --- |
                | 1 | Alice |
                | 2 | Bob |
                | 3 | Carol |
                | 4 | Dave |
                | 5 | Eve |
                
                **Table B: Hobbies**
                
                | PersonID | Hobby |
                | --- | --- |
                | 1 | Reading |
                | 1 | Swimming |
                | 2 | Reading |
                | 3 | Swimming |
                | 4 | Reading |
                | 4 | Swimming |
                | 5 | Reading |
                
                we want to find people who have all the listed hobbies (Reading and Swimming)
                
                **Result**
                
                | PersonID | Name |
                | --- | --- |
                | 1 | Alice |
                | 4 | Dave |
    - Additional Relational Operations
        - Outer Join
            
          ![image](https://github.com/user-attachments/assets/419e74d9-41c0-4059-9f32-de0c414a1472)
            
            - Left outer join **⟕**
                - All left relation even if it didn’t match with right relation
                
             ![image](https://github.com/user-attachments/assets/9f6d60c2-d810-479f-a63a-b1b26970f791)
            - Right outer join **⟖**
                - All right relation even if it didn’t match with left relation
                
            ![image](https://github.com/user-attachments/assets/7bb2bc53-40be-4f0f-bbad-44ad13008f70)
            - Full outer join **⟗**
                - All relation from right and left relation even if it did not match with each other
                
              ![image](https://github.com/user-attachments/assets/9765c3a3-9ae9-4aa6-9bd8-c9b9ac37959b)
        - Aggregate Functions (compute information such average, max, sum and count)
            - It summarize information from database
            - It use with one attribute (column)
            - return one value
                
              ![image](https://github.com/user-attachments/assets/a9845722-faa2-4823-b083-347d534e3b89)
            - Grouping
                - Each ⇒ indicate to use grouping
                
                ![image](https://github.com/user-attachments/assets/011d9917-ed68-4231-baa0-5e90293adae0)
              ![image](https://github.com/user-attachments/assets/86adafea-4217-419a-bbae-0a8c0ff0febb)
