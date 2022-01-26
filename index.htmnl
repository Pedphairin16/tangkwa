<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Virtual Drum Kit</title>

    <link rel="stylesheet" href="style.css">
</head>
<style type="text/css">
    * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial;
}

.wrapper {
    padding: 5em 8em;
    width: 100%;
    height: 100vh;
    background: url('https://images.unsplash.com/photo-1553406624-739b610cf5c8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1500&q=80') no-repeat;
    background-size: cover;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
}

.wrapper .text {
    font-size: 1.5em;
    margin-bottom: 5em;
}

.wrapper .text h1, .wrapper .text p {
    color: white;
    text-align: center;
    margin: 0;
    text-shadow: 3px 3px 10px #000;
    letter-spacing: 2px;
}

.wrapper .text p {
    font-size: 1em;
    font-weight: 300;
}

.keyboard {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    flex-direction: row;
    -webkit-box-pack: justify;
    justify-content: space-between;
}
.keyboard .row {
    display: -webkit-box;
    display: flex;
    flex-direction: row;
    position: relative;
}

.keyboard .key {
    color: #161415;
    text-align: center;
    width: 5em;
    height: 5em;
    background: rgba(255, 255, 255, 0.8);
    border-radius: 10px;
    box-shadow: 0 0 15px rgba( 0, 0, 0, 0.5);
    margin: .5em;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    -webkit-box-pack: center;
    justify-content: center;
    -webkit-transition: .05s linear;
    transition: .05s linear;
}

.keyboard .key p {
    margin: 0 0 .3em 0;
    font-weight: 700;
}

.keyboard .key p:first-child {
    font-size: 2em;
}

.keyboard .key p:last-child {
    font-size: .8em;
    color: blue;
}

.playing {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
    box-shadow: 0 0 5px blue !important;
    border: 2px solid blue;
}
</style>
<script type="text/javascript">
    (function() {

    window.addEventListener('keydown', function(e) {
        const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
        const key = document.querySelector(`.key[data-key="${e.keyCode}"]`);
        console.log(e.keyCode);
        console.log(audio);
        if (!audio) return;
        
        audio.currentTime = 0;
        audio.play();
        key.classList.add('playing');
    });

    function removeTransition(e) {
        if (e.propertyName !== 'transform') return;
        this.classList.remove('playing');
    }

    const keys = document.querySelectorAll('.key');
    keys.forEach(key => key.addEventListener('transitionend', removeTransition));

}());
</script>
<body>

    <div class="wrapper">
        <div class="text">
            <h1>Virtual Drum Kit</h1>
        </div>

        <div class="keyboard">
            <div class="left">
                    <div class="row">
                        <div data-key="81" class="key">
                            <p>Q</p>
                            <p>hi-hat</p>
                        </div>
                        <div data-key="87" class="key">
                            <p>W</p>
                            <p>kick</p>
                        </div>
                        <div data-key="69" class="key">
                            <p>E</p>
                            <p>openhat</p>
                        </div>
                    </div>
                    <div class="row">
                        <div data-key="65" class="key">
                            <p>A</p>
                            <p>boom</p>
                        </div>
                        <div data-key="83" class="key">
                            <p>S</p>
                            <p>snare</p>
                        </div>
                        <div data-key="68" class="key">
                            <p>D</p>
                            <p>clap</p>
                        </div>
                    </div>
                    <div class="row">
                        <div data-key="90" class="key">
                            <p>Z</p>
                            <p>ride</p>
                        </div>
                        <div data-key="88" class="key">
                            <p>X</p>
                            <p>tom</p>
                        </div>
                        <div data-key="67" class="key">
                            <p>C</p>
                            <p>tink</p>
                        </div>
                    </div>
                </div>


                <div class="right">
                    <div class="row">
                        <div data-key="73" class="key">
                            <p>I</p>
                            <p>openhat</p>
                        </div>
                        <div data-key="79" class="key">
                            <p>O</p>
                            <p>snare</p>
                        </div>
                        <div data-key="80" class="key">
                            <p>P</p>
                            <p>hi-hat</p>
                        </div>
                    </div>
                    <div class="row">
                        <div data-key="74" class="key">
                            <p>J</p>
                            <p>boom</p>
                        </div>
                        <div data-key="75" class="key">
                            <p>K</p>
                            <p>kick</p>
                        </div>
                        <div data-key="76" class="key">
                            <p>L</p>
                            <p>clap</p>
                        </div>
                    </div>
                    <div class="row">
                        <div data-key="78" class="key">
                            <p>N</p>
                            <p>ride</p>
                        </div>
                        <div data-key="77" class="key">
                            <p>M</p>
                            <p>tom</p>
                        </div>
                        <div data-key="188" class="key">
                            <p>&#60;</p>
                            <p>tink</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <audio data-key="68" src="http://avclark.com/js-experiments/js-drum-kit/sounds/clap.wav"></audio>
    <audio data-key="81" src="http://avclark.com/js-experiments/js-drum-kit/sounds/hihat.wav"></audio>
    <audio data-key="87" src="http://avclark.com/js-experiments/js-drum-kit/sounds/kick.wav"></audio>
    <audio data-key="69" src="http://avclark.com/js-experiments/js-drum-kit/sounds/openhat.wav"></audio>
    <audio data-key="65" src="http://avclark.com/js-experiments/js-drum-kit/sounds/boom.wav"></audio>
    <audio data-key="90" src="http://avclark.com/js-experiments/js-drum-kit/sounds/ride.wav"></audio>
    <audio data-key="83" src="http://avclark.com/js-experiments/js-drum-kit/sounds/snare.wav"></audio>
    <audio data-key="88" src="http://avclark.com/js-experiments/js-drum-kit/sounds/tom.wav"></audio>
    <audio data-key="67" src="http://avclark.com/js-experiments/js-drum-kit/sounds/tink.wav"></audio>


    <audio data-key="76" src="http://avclark.com/js-experiments/js-drum-kit/sounds/clap.wav"></audio>
    <audio data-key="80" src="http://avclark.com/js-experiments/js-drum-kit/sounds/hihat.wav"></audio>
    <audio data-key="75" src="http://avclark.com/js-experiments/js-drum-kit/sounds/kick.wav"></audio>
    <audio data-key="73" src="http://avclark.com/js-experiments/js-drum-kit/sounds/openhat.wav"></audio>
    <audio data-key="74" src="http://avclark.com/js-experiments/js-drum-kit/sounds/boom.wav"></audio>
    <audio data-key="78" src="http://avclark.com/js-experiments/js-drum-kit/sounds/ride.wav"></audio>
    <audio data-key="79" src="http://avclark.com/js-experiments/js-drum-kit/sounds/snare.wav"></audio>
    <audio data-key="77" src="http://avclark.com/js-experiments/js-drum-kit/sounds/tom.wav"></audio>
    <audio data-key="188" src="http://avclark.com/js-experiments/js-drum-kit/sounds/tink.wav"></audio>

    <script src="script.js"></script>
</body>
</html>
