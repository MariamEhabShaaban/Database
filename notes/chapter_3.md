<h1>Entity Relationship Diagram (ERD)</h1>
<b>ER Model Concept </b>:<p> It is a simple draw to describe the database structure The First step</p>
<h2>It consists of :</h2>
<ul>
  <li>Entity : the real object which I can describe it with some properties like student, project
    <ul>
      <li>weak entity: like order dependent on strong entity take the same code from strong entity (don’t has key) <p><img src="https://github.com/user-attachments/assets/21e3646b-1549-466f-b217-d46146e4714c"></p></li>
      <li>strong entity : independent on him self has primary key (it is a code to differ entity from another one) 
        <p><img src="https://github.com/user-attachments/assets/4f8c930b-ec28-4028-82ac-844e97f8d649"></p></li>
      <p> <img src="https://github.com/user-attachments/assets/2c71d7f3-90fc-41e6-86ef-71ac272915c9"></p>
    </ul>
  </li>
  <li>Attributes : are properties used to describe an entity
    <b>types:</b>
    <ul>
      <li>simple : has one value    <img src="https://github.com/user-attachments/assets/a04d3a2f-dde3-4eb5-9fe6-182c57bcff80"></li>
      <li>composite :attribute of attributes  <img src="https://github.com/user-attachments/assets/56eeca4d-13d9-4c1c-957b-cb254a42f71a">  </li>
      <li>multivalued :has more than one value <img src="https://github.com/user-attachments/assets/7e0bac3c-c97d-41f1-8c46-132d8170dea2"></li>
      <li>derived : like age if you calculate it from birth date   <img src="https://github.com/user-attachments/assets/782fe332-e0af-40ba-87a4-27d5052e9ee9"></li>
      <li>complex : multivalued + composite </li>
    </ul>
  
  
  </li>
  <li>Relationships: relate two or more distinct entities with a specific meaning </li>
  <b>Types</b>
  <p><img src="https://github.com/user-attachments/assets/0a5b91a6-157c-4fe9-830d-1402795c439e"></p>
   <b>Degree of relationship : </b>
   <ul>
     <li>binary : between two entities</li>
     <li>ternary : between three entities</li>
     <li>recursive :between the entity and itself</li>
   </ul>
   
</ul>
