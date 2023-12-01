# Note-Taking-App2
This a Note-Taking App 2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Note-Taking App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        #notes-container {
            width: 80%;
            max-width: 600px;
            margin: 20px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        #notes-container textarea {
            width: calc(100% - 40px);
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
            resize: vertical;
        }
        #notes-container button {
            padding: 8px 15px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 3px;
        }
        #notes-container button:hover {
            background-color: #0056b3;
        }
        .note {
            margin-bottom: 10px;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 3px;
            background-color: #f9f9f9;
        }
    </style>
</head>
<body>

<div id="notes-container">
    <textarea id="noteInput" placeholder="Enter your note here..."></textarea>
    <button onclick="addNote()">Add Note</button>
    <div id="notesList"></div>
</div>

<script>
    function addNote() {
        const noteInput = document.getElementById('noteInput');
        const note = noteInput.value.trim();

        if (note !== '') {
            const notesList = document.getElementById('notesList');
            const newNote = document.createElement('div');
            newNote.classList.add('note');
            newNote.textContent = note;
            notesList.appendChild(newNote);

            noteInput.value = '';
        } else {
            alert('Please enter a note.');
        }
    }
</script>

</body>
</html>
