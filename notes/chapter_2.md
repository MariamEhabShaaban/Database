<h1>Database System Concepts 
and Architecture</h1>
<ul>
  <li>
    Data models , schemas , and instances
  </li>
   <li>
    Three-Schema architecture and data independence
  </li>
  <li>Database Languages and interfaces</li>
  <li>Database System Environment</li>
  <li>Architecture for DBMS</li>
</ul>
<hr>
<h2>Data Models</h2>
<p>a collection of concepts that can used to describe the structure of database to achieve abstraction .there are three types of data models :</p>
<ul>
  <li>High level or conceptual data model :
  <p>provides concepts that are close to the way many users preceive ,uses entities , attributes , relationships</p></li>
    <li>Low level or physical data model :
  <p>provides concepts that describes the details of how data is stored</p></li>
    <li>Representational data model :
  <p>provides concepts that may be easily understood by end users but are not too far from the way data is organized on computer ex:
   <ul>
      <li>relational data model</li>
      <li>hierarchical data model</li>
      <li>network data model</li>
   </ul>
     
    
  </p></li>
      
</ul>
<h2>Schemas and Intances Database state :</h2>
<p> <b>database schema :</b>is the description of database</p>
<p> <b>database state :</b>the data in the database at particular moment in time</p>
<hr>
<h2>Three Schema Architecture and data independence</h2>
<p><b>The goal of three-schema arch --->  is to separate the user applications from the physical database</b></p>
<h3>Schemas Types</h3>
<ul>
  <li>internal level : has physical model</li>
  <li>conceptual level : has representational model</li>
  <li>external or view level : describes the part of the database that aparticular user group is interested in and hides the rest of the database from that group  </li>
</ul>
<img src="https://github.com/user-attachments/assets/5289416f-3477-4134-ac45-add5a3c26c3b">

