# music-player-project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Music Player</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #f4f4f4;
            font-family: Arial, sans-serif;
        }
        #player {
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        audio {
            width: 100%;
            margin-top: 10px;
        }
        button {
            margin: 5px;
            padding: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div id="player">
        <h2>Simple Music Player</h2>
        <audio id="audio" controls>
            <source id="audioSource" src="" type="audio/mpeg">
            Your browser does not support the audio tag.
        </audio>
        <div>
            <button onclick="playSong('song1.mp3')">Song 1</button>
            <button onclick="playSong('song2.mp3')">Song 2</button>
        </div>
    </div>

    <script>
        function playSong(song) {
            const audio = document.getElementById('audio');
            const audioSource = document.getElementById('audioSource');
            audioSource.src = `/music/${song}`;
            audio.load();
            audio.play();
        }
    </script>
</body>
</html>
