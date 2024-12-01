<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile Editor</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f3f3f3;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        label {
            font-weight: bold;
            display: block;
            margin: 10px 0 5px;
        }
        input[type="text"], textarea, select {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .preview {
            margin-top: 20px;
            background: #e9ecef;
            padding: 10px;
            border-radius: 5px;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Profile Editor</h1>
        <form id="profileForm">
            <label for="name">Name</label>
            <input type="text" id="name" placeholder="Enter your name">
            
            <label for="bio">Bio</label>
            <textarea id="bio" rows="4" placeholder="Write a short bio..."></textarea>
            
            <label for="color">Favorite Color</label>
            <input type="color" id="color">
            
            <label for="avatar">Upload Avatar</label>
            <input type="file" id="avatar" accept="image/*">
            
            <button type="button" onclick="previewProfile()">Preview Profile</button>
        </form>

        <div class="preview" id="preview">
            <h2>Preview</h2>
            <p><strong>Name:</strong> <span id="previewName">[Your Name]</span></p>
            <p><strong>Bio:</strong> <span id="previewBio">[Your Bio]</span></p>
            <p><strong>Color:</strong> <span id="previewColor">[Your Favorite Color]</span></p>
        </div>
    </div>

    <script>
        function previewProfile() {
            document.getElementById('previewName').textContent = document.getElementById('name').value || "[Your Name]";
            document.getElementById('previewBio').textContent = document.getElementById('bio').value || "[Your Bio]";
            const color = document.getElementById('color').value;
            document.getElementById('previewColor').textContent = color;
            document.getElementById('previewColor').style.color = color;
        }
    </script>
</body>
</html>
