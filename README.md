<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Fieldwork & Fiction Masterclass III</title>

<style>
:root {
    --bg: #f8f7f3;
    --text: #222;
    --accent: #b44a2b;
    --border: #ddd;
}

body {
    margin: 0;
    font-family: Georgia, serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
}

.container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 40px 20px;
}

h1 {
    font-size: clamp(2rem, 5vw, 3.5rem);
    line-height: 1.1;
    margin-bottom: 20px;
}

h2 {
    margin-top: 80px;
    border-bottom: 1px solid var(--border);
    padding-bottom: 10px;
}

.intro {
    max-width: 800px;
    font-size: 1.1rem;
}

.collage-wrapper {
    position: relative;
    margin-top: 30px;
}

.collage {
    width: 100%;
    display: block;
    border-radius: 8px;
}

.hotspot {
    position: absolute;
    width: 48px;
    height: 48px;
    border: none;
    border-radius: 50%;
    background: var(--accent);
    color: white;
    font-size: 20px;
    cursor: pointer;
    transform: translate(-50%, -50%);
    transition: 0.2s;
}

.hotspot:hover {
    transform: translate(-50%, -50%) scale(1.1);
}

.label {
    position: absolute;
    transform: translate(-50%, -50%);
    background: rgba(255,255,255,0.95);
    padding: 6px 10px;
    border-radius: 6px;
    font-size: 0.85rem;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    gap: 20px;
    margin-top: 30px;
}

.gallery img {
    width: 100%;
    display: block;
    border-radius: 8px;
}

footer {
    margin-top: 80px;
    padding: 40px 0;
    border-top: 1px solid var(--border);
    color: #666;
    font-size: 0.95rem;
}
</style>
</head>

<body>

<div class="container">

    <h1>
        Fieldwork & Fiction Masterclass III:<br>
        Drawing, Mapping and Recording Wounded Urban Landscapes
    </h1>

    <div class="intro">
        <p>
            How can we listen to a landscape? How can drawing, mapping and
            sound recording reveal overlooked traces of urban transformation?
        </p>

        <p>
            During this masterclass, participants explored the city through
            a combination of fieldwork and creative practice. Through walking,
            listening, drawing and mapping, they documented sites marked by
            change, neglect, memory and repair.
        </p>

        <p>
            The resulting sketches, maps and recordings have been brought
            together here as a collective archive of observations and
            encounters, inviting visitors to navigate the landscape through
            both image and sound.
        </p>
    </div>

    <h2>Collective Collage</h2>

    <p>
        Click on the listening points to hear recordings collected during
        the field excursion.
    </p>

    <div class="collage-wrapper">

        <!-- Replace with your collage image -->
        <img src="collage.jpg"
             alt="Collective collage"
             class="collage">

        <!-- SOUND POINT 1 -->
        <button
            class="hotspot"
            style="left:30%; top:25%;"
            onclick="playAudio('audio1')">
            🎧
        </button>

        <div
            class="label"
            style="left:30%; top:18%;">
            Recording 01
        </div>

        <!-- SOUND POINT 2 -->
        <button
            class="hotspot"
            style="left:60%; top:45%;"
            onclick="playAudio('audio2')">
            🎧
        </button>

        <div
            class="label"
            style="left:60%; top:38%;">
            Recording 02
        </div>

        <!-- SOUND POINT 3 -->
        <button
            class="hotspot"
            style="left:22%; top:70%;"
            onclick="playAudio('audio3')">
            🎧
        </button>

        <div
            class="label"
            style="left:22%; top:63%;">
            Recording 03
        </div>

    </div>

    <h2>Drawings & Maps</h2>

    <div class="gallery">

        <img src="drawing1.jpg" alt="Drawing 1">
        <img src="drawing2.jpg" alt="Drawing 2">
        <img src="map1.jpg" alt="Map 1">
        <img src="map2.jpg" alt="Map 2">

    </div>

    <h2>About the Workshop</h2>

    <p>
        Fieldwork & Fiction Masterclass III brought together methods of
        observation, listening, drawing and mapping to investigate wounded
        urban landscapes through collective fieldwork.
    </p>

    <footer>
        Fieldwork & Fiction Masterclass III · Drawings, Maps and Sound Recordings
    </footer>

</div>

<!-- AUDIO FILES -->
<audio id="audio1" src="sound1.mp3"></audio>
<audio id="audio2" src="sound2.mp3"></audio>
<audio id="audio3" src="sound3.mp3"></audio>

<script>
function playAudio(id) {

    document.querySelectorAll("audio").forEach(audio => {
        if (audio.id !== id) {
            audio.pause();
            audio.currentTime = 0;
        }
    });

    const selected = document.getElementById(id);

    if (selected.paused) {
        selected.play();
    } else {
        selected.pause();
    }
}
</script>

</body>
</html>
