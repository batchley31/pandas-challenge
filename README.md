# pandas-challenge

  I labeled the "schools_complete.csv under school_data_to_load, and did the same for "students_complete.csv" named student_data_to_load and used those to read the CSV Path. For each path I had it read into a Pandas Data Frame, then used those Pandas Data Frames and merged them on the column school name sicne that was a column that they each had in common and named that "school_data_complete."

# District Summary

  I first counted the amount of schools and students in the complete set by looking at the unique set of columns under "school_name" since I only wanted to counted them once and not duplicate them and used jsut a reqular count on "student_ID" since each student should already have their own unique ID number.  Then using sum I added all of the amounts in the "budget" column form teh "school_data" csv so I had the total amount all schools had to spend.  Looking at the math score and reading score columns I used .mean to get the average without having to add all the scores together and divide by the total. 
  Looking in the school_data_complete I wanted looked into the math and reading score columns, but only wanted to pull the students that had over a 70 or better and named those passing math and reading respectively.  Using the passing counts I divided them by the total student count as float so it would bring the decimals, and multipled it by 100 to get the percentage passing of students for math and reading through all schools. To be even more precise I looked for the total students passing both math and reading and did the same calculations to find the percentage of students passing both math and reading. I used all this data that I jsut calculated and labeled it and cretaed a DataFrame to make all the date look nice and you can see the calculations in total all together.

# School Summary

  I did all of the same things I did above but looked seperatley by school and what type of school it was.  So now there is a Data Frame that shows the totals for each school individually. The main difference I did to seperate it by school is I set the Index to look for school name and the type of school it was and then looked for the value counts of each school by the school name. 

# Highest Performing Schools (by % Overall Passing)

  To pull the school with the highest overall passsing percentage I sorted the values of the % Overall Passing Column and set it to ascending False so it woudl count down and start with the highest overall percentage instead of the lowest. 

# Bottom Performing Schools (by % Overall Passing)

  I did the same thing for the bottom performing schools but instead of having the asceding equal False, I had it equal True so it woudl start with the lowest percentage and count up from there.

# Math Scores by Grade

  For each grade I created a variable that was equal to each grade and looked through the grade column so I could pull the students and sperate them by grade.  To see the average math scores by grade in each school I used the groupby with each vairable per grade to look in the school name and math score column and used the .mean to calculate it for me.  Then I took all that data and put it into a data frame showing each schools average math score by grade and removed the index numbers on the left to make it look nice.

# Reading Scores by Grade

  I did the same exact thing for reading scores as I did for the math scores, the only difference is I am looking in the reading score column instead of the math score column.

# Scores by School Spending

  I established the ranges for each bin so that when we look at budget per student we can know with bin they fall into. I then cut the per student capita so it would seperate the Per Student Budget into the seperate bins so that way it would show which bin the school falls into, in the new column "spending ranges."  Then looking into the spending ranges column I calculated the average math score, reading score, percent passing math and reading, and the percent passing both. That way I could print a data frame showing the average scores and percent passing for each range of school spending per student. 

# Scores by School Size 

  I did the same exact thing I did for spending excpet I established the bins by popluation of schools, and labeled each bin small, medium, and large that would correlate with the bins. Also instead of Spending Ranges I am looking by school size instead.

# Scores by School Type

To create the Data Frame by School Type I used the groupby to group the average math and reading scores and percents passing math, reading, and both by relating them to the types of schools column.  This way when the data frame displayed it will show the scores and passing percentages by what type of school it is.

# Conclusion and Copmarison

  The first conclusion that I made about this data is that Charter Schools tend to have the best passing rates compared to district schools and they are usually on the smaller side. The reason for this could be that the teachers have less students to focus on and can be more detlaied in their teaching approach.  

  My second conclusion that I made about this data is that jsut becuase your school has a big budget can spend more money per student does not mean that their gardes and passing rates will be higher.  Now this could be again releated to more students per teacher so the teachers do not have enough time to focus on all their students and be intricate with them. In that case it would go back to the more students you have does not make it better to pass reading and math. 

To conclude, according to the data, charter schools with less students have a better passing rate than bigger schools that are in a district.  It does not matter how much money you spend on youre students but the smaller the amount the more chance you have of them succeeding and passing math and reading. 
