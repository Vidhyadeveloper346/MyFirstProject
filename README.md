<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Form</title>
    <link rel ="icon" href="images/icon for form.png">
    <style>
        body{
            background-color: powderblue;
        }
        p,table,tr,td {
            color: black;
            font-family: Verdana, sans-serif;
            font-size: 20px;
            padding: 10px;
        }
        table,tr,td{
            background-color: lightgray;
        }
        select, option{
            font-size: 18px;
        }
        button{
            
            width: 100px;         
            padding: 15px;       
            
            color: white;      
            border: none;
            border-radius: 5px;  
            cursor: pointer;
            font-size: 18px;   
            font-weight: bold;  

        }
        #output {
            margin-top: 20px;
            padding: 10px;
            background: #fff;
            border-radius: 5px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            display: none;
        }
    </style>
  

</head>
<body>
    <center>
        <h2>Registration forms 📝</h2>
        <h3>Fill in yours details caution don't make any mistakes!!</h3>
    </center>
    <p >This is my first attempt to create a webpage and done right . Here you can share your personal details .I have used a simple HTML elements to create this simple registeration form.</p>
    <hr>
    <form id="registrationForm" >
        <center>
            <table>
                <tr> 
                    <td><label for="name">Name:</label> </td>
                    <td><input type="text" id="name" name="name"></td>
                </tr>
    
                <tr>
                   <td> <label for="age">Age:</label> </td>
                    <td><input type="text" id="age" age="age"></td>
                </tr>
                <tr>
                    <td> Gender: </td>
                     <td><input type="radio" name="Gender" value="Male">Male</td>
                     <td><input type="radio" name="Gender" value="Female">Female</td>
                 </tr>
                 
                <tr>
                    <td><label for="phone_no">Phone number:</label> </td>
                    <td><input type="text" id="phone_no" phone_no="phone_no"></td>
                </tr>
                <tr>
                    <td><label for="date_of_birth">Date of Birth:</label></td>
                    <td width="30px" height="10px"><input type="date" id="date_of_birth" date_of_birth="date_of_birth" ></td>
    
                </tr>
                <tr>
                    <td><label for="email">Email:</label></td>
                    <td><input type="email" id="email" name="email" required></td>
                </tr>

                <tr>
                    <td><label for="username">UserName:</label></td>
                    <td><input type="text" id="username" name="username" required></td>
                </tr>
                
                
                <tr>
                    <td><label for="password">Password:</label></td>
                    <td><input type="password" id="password"></td>
                </tr>
                <tr>
                <td> Select the course: </td>
                <td>
                    <select>
                        <option>Python Programming</option>
                        <option>Java Programming</option>
                        <option>C Programming</option>  
                        <option>C++ Programming</option>
                    </select>
                </td>
            </tr>
               <td>Upload your Resume:</td> 
              <td><input type="file" id="resume"></td>  
 
            </table>

            <button type="reset" style="background-color: red;">Reset</button>
            <button style="background-color: green;" type="submit">Submit</button>
        </center>
    </form>
    <div id="output"></div>
    <script>
    document.getElementById("registrationForm").addEventListener("submit", function(event) {
        event.preventDefault(); 
    
        
        let name = document.getElementById("name").value;
        let age = document.getElementById("age").value;
        let phone_no = document.getElementById("phone_no").value;
        let date_of_birth = document.getElementById("date_of_birth").value;
        let email = document.getElementById("email").value;
        let username = document.getElementById("username").value;
        let password = document.getElementById("password").value;
        let resume = document.getElementById("resume").value;
    
      
        let genderField = document.querySelector('input[name="Gender"]:checked');
        let gender = genderField ? genderField.value : "Not selected";
    
     
        let outputDiv = document.getElementById("output");
        outputDiv.style.display = "block";
        outputDiv.innerHTML = `
            <h3>Submitted Data:</h3>
            <p><strong>Name:</strong> ${name}</p>
            <p><strong>Email:</strong> ${email}</p>
            <p><strong>Age:</strong> ${age}</p>
            <p><strong>Phone:</strong> ${phone_no}</p>
            <p><strong>Date of Birth:</strong> ${date_of_birth}</p>
            <p><strong>Username:</strong> ${username}</p>
            <p><strong>Password:</strong> ${password}</p>
            <p><strong>Resume:</strong> ${resume ? resume : "No file selected"}</p>
            <p><strong>Gender:</strong> ${gender}</p>
        `;
    });
    
</script>
            

     
        
  

</body>
</html>
