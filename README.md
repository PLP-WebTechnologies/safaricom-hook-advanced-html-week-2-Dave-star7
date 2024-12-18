### Assignment: Building a Multimedia Webpage and a Registration Form  

#### Objective: 
The goal of this assignment is to create a multimedia-rich webpage featuring audio and video elements and design a simple registration form with built-in HTML validation.  

---

### Part 1: Multimedia Webpage 
Create an HTML webpage that includes the following:  
1. **Audio Element**:  
   - Add an audio file using the `<audio>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Use at least one source format (e.g., `.mp3` or `.ogg`).  

2. **Video Element**:  
   - Add a video file using the `<video>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Include at least two source formats for compatibility (e.g., `.mp4` and `.webm`).  
   - Add a poster image that displays before the video plays.  

**Example Output:**  
A webpage where users can play an audio track and watch a video.  

---

### **Part 2: Registration Form **  
Design a user registration form with the following requirements:  

1. **Form Elements**:  
   - Full Name (Text input)  
   - Email Address (Input of type `email`)  
   - Password (Input of type `password`)  
   - Age (Input of type `number`, with a minimum value of 18)  
   - Gender (Radio buttons for Male, Female, Other)  
   - Terms and Conditions (Checkbox to agree before submitting)  

2. **Validation**:  
   - Use HTML5 validation attributes such as `required`, `min`, `maxlength`, etc.  
   - Ensure the email field has proper validation for email format.  
   - Make the password field require at least 8 characters.  

3. **Submit Button**:  
   - Include a "Register" button to submit the form.  

**Example Output:**  
A user-friendly registration form that prevents submission if required fields are not filled correctly.  






<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multimedia Webpage and Registration Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      background-color: #f4f4f9;
      color: #333;
    }
    h1, h2 {
      color: #444;
    }
    .container {
      width: 90%;
      max-width: 800px;
      margin: 20px auto;
      padding: 20px;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }
    .form-group {
      margin-bottom: 15px;
    }
    label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }
    input, button {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1rem;
    }
    button {
      background-color: #5cb85c;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: #4cae4c;
    }
    .form-group-inline {
      display: flex;
      align-items: center;
    }
    .form-group-inline label {
      margin-right: 10px;
    }
    .terms {
      display: flex;
      align-items: center;
    }
    .terms input {
      margin-right: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Multimedia Webpage</h1>
    
    <h2>Audio</h2>
    <audio controls>
      <source src="audio-file.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>

    <h2>Video</h2>
    <video controls poster="poster-image.jpg">
      <source src="video-file.mp4" type="video/mp4">
      <source src="video-file.webm" type="video/webm">
      Your browser does not support the video element.
    </video>
  </div>

  <div class="container">
    <h1>Registration Form</h1>
    <form action="#" method="post">
      <div class="form-group">
        <label for="full-name">Full Name</label>
        <input type="text" id="full-name" name="full-name" required maxlength="50">
      </div>

      <div class="form-group">
        <label for="email">Email Address</label>
        <input type="email" id="email" name="email" required>
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" name="password" required minlength="8">
      </div>

      <div class="form-group">
        <label for="age">Age</label>
        <input type="number" id="age" name="age" min="18" required>
      </div>

      <div class="form-group">
        <label>Gender</label>
        <div class="form-group-inline">
          <input type="radio" id="male" name="gender" value="male" required>
          <label for="male">Male</label>
          
          <input type="radio" id="female" name="gender" value="female">
          <label for="female">Female</label>
          
          <input type="radio" id="other" name="gender" value="other">
          <label for="other">Other</label>
        </div>
      </div>

      <div class="form-group terms">
        <input type="checkbox" id="terms" name="terms" required>
        <label for="terms">I agree to the Terms and Conditions</label>
      </div>

      <button type="submit">Register</button>
    </form>
  </div>
</body>
</html>









---
