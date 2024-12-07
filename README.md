Project Description:
This is a Menu driven application that allows users to select a project such as  " door installation " and will be given
the time a project will take to accomplish , The difficulty of the project , & Notes on the project.

Technologies Used:
* Java
* Eclipse
* DBeaver
* Draw.io
* MySQL

Key Code:
*This code showcases the menu for the application users will be able to type a corresponding number and access the 
option given.

private List<String> operations = List.of(
      "1) Add a project",
      "2) List projects",
      "3) Select a project",
      "4) Update project details",
      "5) Delete a project"
  );

  * This code showcases the input given by the application when a certain option is selected.

private void createProject() {
    String projectName = getStringInput("Enter the project name");
    BigDecimal estimatedHours = getDecimalInput("Enter the estimated hours");
    BigDecimal actualHours = getDecimalInput("Enter the actual hours");
    Integer difficulty = getIntInput("Enter the project difficulty (1-5)");
    String notes = getStringInput("Enter the project notes");

Many challeneges when executing this project especially with the outcomes in the menu when using decimal numbers. Fixable 
by using the correct imports for the code for example " import java.math.BigDecimal; " helped with the random decimal outcomes 
in the application.

Installation:
Clone Project: https://github.com/RafyPerez95/MenuDrivenApplication.git

Project Directory: cd mysql_java

Contributions:
* All contributions are welcomed!

Favorite Feature:
* My personal favorite feature for the application is also allowing there to be errors if a user selected an invalid
selection and being able to go back and choose a correct one.

private void processUserSelections() {
    boolean done = false;

    while(!done) {
      try {
        int selection = getUserSelection();

        switch(selection) {
          case -1:
            done = exitMenu();
            break;
            
          case 1:
            createProject();
            break;
            
          case 2:
            listProjects();
            break;
            
          case 3: 
            selectProject ();
            break;
            
          case 4:
            updateProjectDetails();
            break;
            
          case 5:
            deleteProject();
            break;

          default:
            System.out.println("\n" + selection + " is not a valid selection. Try again.");
           
        }
      }
      catch(Exception e) {
        System.out.println("\nError: " + e + " Try again.");
      

Contect Info:
Project Link: https://github.com/RafyPerez95/MenuDrivenApplication.git
Email: Rafantperez1@gmail.com
