
- chapter 4️⃣
    
    # Enhanced Entity Relationship (EER) Modeling
    
    ## Concepts:
    
    - Subclasses / Superclasses
    - Specialization / Generalization
    - Categories ( UNION types )
    - Attribute and relationship inheritance
    
    ## Subclasses / Superclasses :
    
       in many cases an entity type has different subgroupings of its entities that are  
    
          meaninigful and need to be represented explicity
    
    - Subclass ⇒ Subgrouping
    - Superclass ⇒ Entity
    - Local Atrribute ⇒ attribute for one of subclasses
    
    ## Specialization
    
    is the process of defining subclasses of a superclass
    
    - **Reasons to specialize:**
        1. some attributes may not allow to all superclass
        2. some relationship may allow to some of subclass
    
    ## Generalization
    
    - Generalization is the process of extracting common properties from a set of entities and creating a generalized entity from it. It is a bottom-up approach
    - collect attributes which common in subclasses to superclass
    
    ## Constraints on specialization and generalization
    
    - **Disjointness**
        - entity member at one subclass only ( d ) character
        
        Overlapping ⇒ entity member at more than one subclass ( O ) character
        
     ![disjoint](https://github.com/user-attachments/assets/c22ac257-8780-47e6-9ad8-e844847941f3)
        
    - **Competeness**
        - the superclass must be a member of some subclasses.
        - show in EER by a double line
    
    Hierarchy ⇒ every subclass has one superclass ( single inheritance )
    
    Lattice ⇒ Subclass may have more than one superclass ( multiple inheritance )
    
   ![complete](https://github.com/user-attachments/assets/ec30382f-70f7-4c90-8f49-1381e53081fb)
    
    ## Categories (Union of super-classes)
    
    - It is a method to collect super-classes in entity to connect it with other relationship and entities
    - show in EER diagram by ( U )
    
    shared class ⇒ intersection between superclasses
    
  

![cat](https://github.com/user-attachments/assets/a34551ba-8a51-46d5-b0a7-11e4ee7890af)

    
