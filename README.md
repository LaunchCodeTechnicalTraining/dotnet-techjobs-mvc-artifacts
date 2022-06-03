# C# Graded Assignment #3 Rubric (TechJobs, MVC Edition)

This assignment asks the students to once again refactor a TechJobs application, this time using an MVC 
design pattern.

To grade this assignment, you will have the student demo their application again. Ask your students to 
show you the items below in the running application, as well as the code that is running the application.

## Score your students' work based on the following criteria:

### Appearance and Code Check:

1. Have the student start their application.

1. Test the search functionality of the project:

   a. Ask the student to initiate a search by location, using the search term "new york". Only 1 result should be returned on the page. The result may vary in appearance, but make sure it contains the job data organized similar to this image:

   ![Search result](searchByLocation.png "Search Result Sample")

   b. Ask them to initiate another search by location, this time using the search term "chicago". Check that no results are returned.

   c. Ask to a search by employer this time, using the search term "equifax". 1 job should be returned.

   d. Ask for one more search term, this time searching by ``all`` for the term "Ruby". 4 results should be returned.

   e. Search for the same term, "Ruby" with the "Skill" category checked. This time, only 3 results should be returned.

1. Ask your student to show you their method for displaying the search results tested above.

   a. Be sure they can point you to their method within ``SearchController``.

   b. Is that method posting to ``"results"``?

   c. Does it make use of ``findAll()`` and ``findByColumnAndValue()`` appropriately? Or are they manipulating
      ``JobData``?

   d. Ask them which strategy they have elected to use to display the jobs. Are they creating one table for all
   of the jobs displayed or one table per job?

1. Back in the running app, ask your student to navigate to the ``List`` view and have them select *View All*.

   a. A view of all 98 jobs should be returned. Ask them to scroll down to the end of the results to confirm.

1. Within the code, we give the students 2 options to accomplish the "View All" list. Be sure they can tell you which of these options they have chosen:
   
      a. An entry is added to ``tableChoices`` for the option to view all: ``tableChoices.put("all", "View All");``
      
      b. The ``list.html`` template contains another table cell with the parameters hard-coded into a ``th:href`` for the view all view: ``<a th:href="@{/list/jobs(column='All',value='View All')}">View All</a>``.


## Feedback and Grades:
    
Give your student a 1/1 score if they have met each of the requirements above. If, for some 
reason, they have not completed each item, offer some advice on how to complete the assignment
or probe them to find out more about what could be blocking their progress. Make a plan to 
have them demonstrate their work again when they have had time to make more progress.


<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Java Web Development TechJobs OO</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://www.launchcode.org/" property="cc:attributionName" rel="cc:attributionURL">The LaunchCode Foundation</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
