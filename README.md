# Web-Eng
labs of web Engineering
<!DOCTYPE html>
<html>
	<head>
		<title>Lab#2</title>   
        <style>
             h1 {
  color: #04AA6D;
}
            h2 {
  color: blueviolet;
}
            * {box-sizing: border-box}
body {font-family: Arial, Helvetica, sans-serif;}
.navbar {
  width: 100%;
  background-color:purple;
  overflow: auto;
}
.navbar a {
  float: left;
  padding: 12px;
  color: white;
  text-decoration: none;
  font-size: 17px;
  width: 25%; /* Four links of equal widths */
  text-align: center;
}
.navbar a:hover {
  background-color:#04AA6D;
}
.navbar a.active {
  background-color: #04AA6D;
}
@media screen and (max-width: 500px) {
  .navbar a {
    float: none;
    display: block;
    width: 100%;
    text-align: left;
  }
}
        </style>   
	</head>
	<body>
        <div class="navbar">
        <a href="https://www.ssuet.edu.pk/">Home Page</a>
        <a href="https://www.ssuet.edu.pk/wp-content/uploads/2021/05/Student-Profile.pdf">Students</a>
        <a href="https://www.ssuet.edu.pk/wp-content/uploads/2021/09/Application-of-Scholarship.pdf">
            Scholarship Notice Page</a>
        <a href="https://www.ssuet.edu.pk/news-events/?__cf_chl_jschl_tk__=Q0Alusq1.uIE9pV0EhEbS1as1a
        Gqf5Txn0MfulU87KY-1636392350-0-gaNycGzNCmU">News & Events</a>
 </div>
			<div class="header">
				<h1><center>Welcome to Sir Syed University of Engineering and Technology</center></h1>	
			</div>
			<div class="content">		
					<h2><center><u>Student's Profile</u></center></h2>
					<p class="introduction">    
						<img id=”uni-logo” class="university-logopicture" src="download.jfif"
                         alt="SSUET" width="100" height="100"/>
                Sir Syed University of Engineering and Technology, is one of the best universities 
                operating in Pakistan and is known for its outstanding contribution towards polishing 
                the students as to be ready for serving in the IT industry and at the same time focus 
                on the new and emerging technology to be at the disposal of the students acquiring
                 the expertise to be used in the IT sector.
					</p>				
			</div>
            <style>
                .button-style {
                    border: 1px solid blue;
                    border-radius: 25px;
                    background-color: red;
                    color: white;
                    display: inline-block;
                    width: 150px;
                }
            </style>    
            <table id="CoursesTaken" class="courses">
                <thead>
                    <tr>
                        <th>Course ID</th>
                        <th>Course Name</th>
                        <th>Credit hours</th>
                        <th>Year Taken</th>
                    </tr>
                </thead>
                <tbody>
                    <tr id="row1" class="row">
                        <td>Course 1</td>
                        <td>Javascript</td>
                        <td>2+1</td>
                        <td>2021</td>
                    </tr>
                    <tr id="row2" class="row">
                        <td>Course 2</td>
                        <td>Compilar Construction</td>
                        <td>3+0</td>
                        <td>2021</td>
                    </tr>
                    <tr id="row3" class="row">
                        <td>Course 3</td>
                        <td>Pakistan Studies</td>
                        <td>2+0</td>
                        <td>2019</td>
                    </tr>
                    <tr id="row4" class="row">
                        <td>Course 4</td>
                        <td>Artificial Intelligence</td>
                        <td>2+1</td>
                        <td>2020</td>
                    </tr>
                </tbody>
            </table>       
            </br>
            <input id="addRowColor" type="button" value="Add Row Color" />          
<input type="button" value="Add New Course" onclick="addNewCourse();" />
		<input type="button" value="Remove Course" onclick="removeCourse();" />
		<input type="button" value="Update Course" onclick="updateCourse();" />
            <script>             
			function addNewCourse(){
				const body = document.querySelector('tbody');
				const row = document.createElement('tr');			//Create 'tr' element
				const tdCourseID = document.createElement('td');	//Create 'td' element
				const tdCourseName = document.createElement('td');	//Create 'td' element
				const tdYearTaken = document.createElement('td');	//Create 'td' element				
				const courseId = ((Math.round(Math.random() * 100)) + 4);
                const courseName = ((Math.round(Math.random() * 500)) + 50);
				const yearTaken = (Math.round(Math.random() * 2020)) + 2020;
				row.id = 'row' + courseId;
				
				tdCourseID.innerHTML = 'Course ' + courseId;
				tdCourseName.innerHTML = 'Course - DOM - ' + courseName;
				tdYearTaken.innerHTML = yearTaken;
				
				row.appendChild(tdCourseID);
				row.appendChild(tdCourseName);
				row.appendChild(tdYearTaken);				
				body.appendChild(row);
			}			
			function removeCourse(){
				
				const courseId = prompt('Please enter course#');				
				if(courseId){				
					const row = document.getElementById('row' + courseId);
					if(row){				
						const body = document.querySelector('tbody');		
						body.removeChild(row);
					}}}
			function updateCourse(){ 
const newCourseYear = prompt('Please enter course# and new year delimited by comma');
				if(newCourseYear){
					
					const courseId = newCourseYear.split(',')[0];
					const courseYear = newCourseYear.split(',')[1];
					
					//Find the row containing the 'course #' entered by the user
					const row = document.getElementById('row' + courseId);
					if(row){
						//Find the 'year taken' td element within the 'row' entered by the user
						const tdYearTaken = row.querySelector('#row' + courseId + ' > td:nth-child(3)');
						
						//Finally update the new 'year taken' entered by the user using 'innerHTML' property of element
						tdYearTaken.innerHTML = courseYear;
					}
				}	
			}
                const btnRowColor = document.getElementById('addRowColor');
                         
			btnRowColor.addEventListener('click', function(event) {
				//Find the 'row' element
				const row = document.querySelector('#row2');
//Update its 'background-color' and 'color' style
row.style.backgroundColor = 'pink';
				row.style.color = 'brown';
			});
</script>
</div>    
          </body>
        </html>
	
