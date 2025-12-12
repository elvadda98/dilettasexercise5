<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ESL Vocabulary Exercise</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 20px;
            color: #333;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            color: #008080;
        }
        .nav-buttons {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }
        button {
            background: linear-gradient(135deg, #4CAF90, #008080);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s;
        }
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .score {
            font-size: 18px;
            font-weight: bold;
            color: #008080;
            margin-left: auto;
        }
        .section {
            display: none;
        }
        .section.active {
            display: block;
        }
        .vocab-item {
            background: linear-gradient(135deg, #e6f7ff, #b3f0ff);
            border-left: 5px solid #008080;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 8px;
        }
        .word-bank {
            background: linear-gradient(135deg, #4CAF90, #008080);
            color: white;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .word-bank div {
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 12px;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.2s;
        }
        .word-bank div:hover {
            background: rgba(255, 255, 255, 0.3);
        }
        .sentence {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 4px solid #4CAF90;
        }
        input[type="text"] {
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            width: 150px;
        }
        .match-container {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
        }
        .match-column {
            width: 48%;
            background: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
        }
        .match-item {
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.2s;
        }
        .match-item:hover {
            background: #e6f7ff;
        }
        .correct {
            background-color: #d4edda !important;
            color: #155724;
        }
        .incorrect {
            background-color: #f8d7da !important;
            color: #721c24;
        }
        .selected {
            background-color: #d1ecf1 !important;
        }
        .feedback {
            margin-top: 5px;
            font-size: 14px;
            font-style: italic;
        }
        .microphone-btn {
            background: linear-gradient(135deg, #ff6b6b, #ee5a24);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-left: 10px;
        }
        .pronunciation-input {
            display: inline-flex;
            align-items: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="score">Score: 0 / 21</div>
        <div class="nav-buttons">
            <button onclick="showSection('vocabulary')">Vocabulary List</button>
            <button onclick="showSection('writing')">Fill in the Gaps (Writing)</button>
            <button onclick="showSection('matching')">Match Definitions</button>
            <button onclick="showSection('pronunciation')">Fill in the Gaps (Pronunciation)</button>
        </div>

        <!-- Vocabulary List Section -->
        <div id="vocabulary" class="section active">
            <h2>Vocabulary List</h2>
            <div class="vocab-item">
                <h3>short <button onclick="speak('short')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> not long in time, distance, or length</p>
                <p><strong>Meaning:</strong> measuring or lasting a small distance, time, or amount</p>
                <p><strong>Example:</strong> The meeting was short but very productive.</p>
            </div>
            <div class="vocab-item">
                <h3>co-living <button onclick="speak('co-living')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> as convivere (living together)</p>
                <p><strong>Meaning:</strong> a modern form of shared housing where residents with similar values live together</p>
                <p><strong>Example:</strong> Co-living spaces are becoming popular among young professionals in big cities.</p>
            </div>
            <div class="vocab-item">
                <h3>tasks <button onclick="speak('tasks')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> pieces of work to be done</p>
                <p><strong>Meaning:</strong> specific pieces of work required to be done as part of one's duties</p>
                <p><strong>Example:</strong> She completed all her tasks before the deadline.</p>
            </div>
            <div class="vocab-item">
                <h3>take-off <button onclick="speak('take-off')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> the moment when an aircraft leaves the ground</p>
                <p><strong>Meaning:</strong> the act or moment of an aircraft becoming airborne</p>
                <p><strong>Example:</strong> The take-off was delayed due to bad weather.</p>
            </div>
            <div class="vocab-item">
                <h3>land <button onclick="speak('land')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> as atterrare (to touch down)</p>
                <p><strong>Meaning:</strong> to come down through the air and settle on the ground</p>
                <p><strong>Example:</strong> The plane will land in Rome at 6 PM.</p>
            </div>
            <div class="vocab-item">
                <h3>runway <button onclick="speak('runway')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> the strip where planes take off and land</p>
                <p><strong>Meaning:</strong> a long, narrow strip at an airport where aircraft take off and land</p>
                <p><strong>Example:</strong> The runway is currently closed for maintenance.</p>
            </div>
            <div class="vocab-item">
                <h3>fruit market <button onclick="speak('fruit market')">▶️ Hear</button></h3>
                <p><strong>Context:</strong> a place where fruits are sold</p>
                <p><strong>Meaning:</strong> a market where various kinds of fruits are sold</p>
                <p><strong>Example:</strong> We bought fresh oranges at the fruit market this morning.</p>
            </div>
        </div>

        <!-- Fill in the Gaps (Writing) Section -->
        <div id="writing" class="section">
            <h2>Fill in the Gaps (Writing)</h2>
            <div class="word-bank" id="wordBank">
                <div onclick="selectWord('short')">short</div>
                <div onclick="selectWord('co-living')">co-living</div>
                <div onclick="selectWord('tasks')">tasks</div>
                <div onclick="selectWord('take-off')">take-off</div>
                <div onclick="selectWord('land')">land</div>
                <div onclick="selectWord('runway')">runway</div>
                <div onclick="selectWord('fruit market')">fruit market</div>
            </div>
            <div class="sentence" id="sentence3">
                <p>The pilot announced that the <input type="text" id="input3" placeholder="___"> would be in 10 minutes.</p>
                <div class="feedback" id="feedback3"></div>
            </div>
            <div class="sentence" id="sentence5">
                <p>We need to finish these <input type="text" id="input5" placeholder="___"> by Friday.</p>
                <div class="feedback" id="feedback5"></div>
            </div>
            <div class="sentence" id="sentence1">
                <p>He cut his hair <input type="text" id="input1" placeholder="___"> for the summer.</p>
                <div class="feedback" id="feedback1"></div>
            </div>
            <div class="sentence" id="sentence7">
                <p>She bought fresh strawberries at the <input type="text" id="input7" placeholder="___">.</p>
                <div class="feedback" id="feedback7"></div>
            </div>
            <div class="sentence" id="sentence2">
                <p>Many young professionals prefer <input type="text" id="input2" placeholder="___"> to save money.</p>
                <div class="feedback" id="feedback2"></div>
            </div>
            <div class="sentence" id="sentence6">
                <p>The plane is preparing for <input type="text" id="input6" placeholder="___"> on the main strip.</p>
                <div class="feedback" id="feedback6"></div>
            </div>
            <div class="sentence" id="sentence4">
                <p>Due to strong winds, the aircraft had to abort <input type="text" id="input4" placeholder="___">.</p>
                <div class="feedback" id="feedback4"></div>
            </div>
            <button onclick="checkWritingAnswers()">Check Answers</button>
            <button onclick="resetWriting()">Reset</button>
        </div>

        <!-- Match Definitions Section -->
        <div id="matching" class="section">
            <h2>Match Definitions</h2>
            <div class="match-container">
                <div class="match-column">
                    <h3>Words</h3>
                    <div class="match-item" onclick="selectWordMatch('short')">short</div>
                    <div class="match-item" onclick="selectWordMatch('co-living')">co-living</div>
                    <div class="match-item" onclick="selectWordMatch('tasks')">tasks</div>
                    <div class="match-item" onclick="selectWordMatch('take-off')">take-off</div>
                    <div class="match-item" onclick="selectWordMatch('land')">land</div>
                    <div class="match-item" onclick="selectWordMatch('runway')">runway</div>
                    <div class="match-item" onclick="selectWordMatch('fruit market')">fruit market</div>
                </div>
                <div class="match-column">
                    <h3>Definitions</h3>
                    <div class="match-item" onclick="selectDefinitionMatch('a market where various kinds of fruits are sold')">a market where various kinds of fruits are sold</div>
                    <div class="match-item" onclick="selectDefinitionMatch('a long, narrow strip at an airport where aircraft take off and land')">a long, narrow strip at an airport where aircraft take off and land</div>
                    <div class="match-item" onclick="selectDefinitionMatch('the act or moment of an aircraft becoming airborne')">the act or moment of an aircraft becoming airborne</div>
                    <div class="match-item" onclick="selectDefinitionMatch('a modern form of shared housing where residents with similar values live together')">a modern form of shared housing where residents with similar values live together</div>
                    <div class="match-item" onclick="selectDefinitionMatch('specific pieces of work required to be done as part of one\'s duties')">specific pieces of work required to be done as part of one's duties</div>
                    <div class="match-item" onclick="selectDefinitionMatch('measuring or lasting a small distance, time, or amount')">measuring or lasting a small distance, time, or amount</div>
                    <div class="match-item" onclick="selectDefinitionMatch('to come down through the air and settle on the ground')">to come down through the air and settle on the ground</div>
                </div>
            </div>
            <button onclick="checkMatchingAnswers()">Check Matches</button>
            <button onclick="resetMatching()">Reset</button>
        </div>

        <!-- Fill in the Gaps (Pronunciation) Section -->
        <div id="pronunciation" class="section">
            <h2>Fill in the Gaps (Pronunciation)</h2>
            <div class="word-bank" id="pronunciationWordBank">
                <div>short</div>
                <div>co-living</div>
                <div>tasks</div>
                <div>take-off</div>
                <div>land</div>
                <div>runway</div>
                <div>fruit market</div>
            </div>
            <div class="sentence">
                <p>He wore a <span class="pronunciation-input"><input type="text" id="pronunciationInput1" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('short', 'pronunciationInput1')">🎤</button></span> jacket.</p>
                <div class="feedback" id="pronunciationFeedback1"></div>
            </div>
            <div class="sentence">
                <p>The <span class="pronunciation-input"><input type="text" id="pronunciationInput4" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('take-off', 'pronunciationInput4')">🎤</button></span> was smooth.</p>
                <div class="feedback" id="pronunciationFeedback4"></div>
            </div>
            <div class="sentence">
                <p>We need to complete our daily <span class="pronunciation-input"><input type="text" id="pronunciationInput3" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('tasks', 'pronunciationInput3')">🎤</button></span>.</p>
                <div class="feedback" id="pronunciationFeedback3"></div>
            </div>
            <div class="sentence">
                <p>She loves visiting the <span class="pronunciation-input"><input type="text" id="pronunciationInput7" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('fruit market', 'pronunciationInput7')">🎤</button></span> on weekends.</p>
                <div class="feedback" id="pronunciationFeedback7"></div>
            </div>
            <div class="sentence">
                <p>The plane will <span class="pronunciation-input"><input type="text" id="pronunciationInput5" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('land', 'pronunciationInput5')">🎤</button></span> in 20 minutes.</p>
                <div class="feedback" id="pronunciationFeedback5"></div>
            </div>
            <div class="sentence">
                <p><span class="pronunciation-input"><input type="text" id="pronunciationInput2" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('co-living', 'pronunciationInput2')">🎤</button></span> is popular among digital nomads.</p>
                <div class="feedback" id="pronunciationFeedback2"></div>
            </div>
            <div class="sentence">
                <p>The <span class="pronunciation-input"><input type="text" id="pronunciationInput6" placeholder="___" readonly> <button class="microphone-btn" onclick="startRecognition('runway', 'pronunciationInput6')">🎤</button></span> is clear for departure.</p>
                <div class="feedback" id="pronunciationFeedback6"></div>
            </div>
        </div>
    </div>

    <script>
        let score = 0;
        const totalScore = 21;
        let selectedWord = null;
        let selectedDefinition = null;
        let selectedWordMatch = null;
        let selectedInput = null;
        let recognition = null;

        // Initialize speech recognition
        if ('webkitSpeechRecognition' in window) {
            recognition = new webkitSpeechRecognition();
        } else if ('SpeechRecognition' in window) {
            recognition = new SpeechRecognition();
        }

        if (recognition) {
            recognition.continuous = false;
            recognition.interimResults = false;
            recognition.lang = 'en-US';

            recognition.onresult = function(event) {
                const result = event.results[0][0].transcript.trim().toLowerCase();
                const expectedWord = selectedInput.dataset.expected.toLowerCase();
                const inputField = document.getElementById(selectedInput.id);

                if (result === expectedWord) {
                    inputField.value = selectedInput.dataset.expected;
                    inputField.className = 'correct';
                    document.getElementById('pronunciationFeedback' + selectedInput.id.slice(-1)).textContent = 'Correct!';
                    document.getElementById('pronunciationFeedback' + selectedInput.id.slice(-1)).style.color = 'green';
                    if (!selectedInput.dataset.scored) {
                        score++;
                        selectedInput.dataset.scored = 'true';
                        updateScore();
                    }
                } else {
                    inputField.className = 'incorrect';
                    document.getElementById('pronunciationFeedback' + selectedInput.id.slice(-1)).textContent = `Incorrect. You said: "${result}". Try again!`;
                    document.getElementById('pronunciationFeedback' + selectedInput.id.slice(-1)).style.color = 'red';
                }
            };

            recognition.onerror = function(event) {
                document.getElementById('pronunciationFeedback' + selectedInput.id.slice(-1)).textContent = 'Error occurred in recognition: ' + event.error;
                document.getElementById('pronunciationFeedback' + selectedInput.id.slice(-1)).style.color = 'red';
            };
        }

        function startRecognition(expectedWord, inputId) {
            selectedInput = document.getElementById(inputId);
            selectedInput.dataset.expected = expectedWord;
            if (recognition) {
                recognition.start();
            } else {
                alert('Speech recognition not supported in your browser.');
            }
        }

        function showSection(sectionId) {
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            document.getElementById(sectionId).classList.add('active');
        }

        function speak(word) {
            const u = new SpeechSynthesisUtterance(word);
            u.lang = "en-US";
            speechSynthesis.speak(u);
        }

        function selectWord(word) {
            selectedWord = word;
            document.querySelectorAll('#wordBank div').forEach(div => {
                div.style.backgroundColor = div.textContent === word ? '#a5d8ff' : 'rgba(255, 255, 255, 0.2)';
            });
        }

        function checkWritingAnswers() {
            // Check sentence 1
            const input1 = document.getElementById('input1').value.trim().toLowerCase();
            if (input1 === 'short') {
                document.getElementById('input1').className = 'correct';
                document.getElementById('feedback1').textContent = 'Correct!';
                document.getElementById('feedback1').style.color = 'green';
                if (!document.getElementById('input1').dataset.scored) {
                    score++;
                    document.getElementById('input1').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input1').className = 'incorrect';
                document.getElementById('feedback1').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback1').style.color = 'red';
            }

            // Check sentence 2
            const input2 = document.getElementById('input2').value.trim().toLowerCase();
            if (input2 === 'co-living') {
                document.getElementById('input2').className = 'correct';
                document.getElementById('feedback2').textContent = 'Correct!';
                document.getElementById('feedback2').style.color = 'green';
                if (!document.getElementById('input2').dataset.scored) {
                    score++;
                    document.getElementById('input2').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input2').className = 'incorrect';
                document.getElementById('feedback2').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback2').style.color = 'red';
            }

            // Check sentence 3
            const input3 = document.getElementById('input3').value.trim().toLowerCase();
            if (input3 === 'land') {
                document.getElementById('input3').className = 'correct';
                document.getElementById('feedback3').textContent = 'Correct!';
                document.getElementById('feedback3').style.color = 'green';
                if (!document.getElementById('input3').dataset.scored) {
                    score++;
                    document.getElementById('input3').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input3').className = 'incorrect';
                document.getElementById('feedback3').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback3').style.color = 'red';
            }

            // Check sentence 4
            const input4 = document.getElementById('input4').value.trim().toLowerCase();
            if (input4 === 'take-off') {
                document.getElementById('input4').className = 'correct';
                document.getElementById('feedback4').textContent = 'Correct!';
                document.getElementById('feedback4').style.color = 'green';
                if (!document.getElementById('input4').dataset.scored) {
                    score++;
                    document.getElementById('input4').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input4').className = 'incorrect';
                document.getElementById('feedback4').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback4').style.color = 'red';
            }

            // Check sentence 5
            const input5 = document.getElementById('input5').value.trim().toLowerCase();
            if (input5 === 'tasks') {
                document.getElementById('input5').className = 'correct';
                document.getElementById('feedback5').textContent = 'Correct!';
                document.getElementById('feedback5').style.color = 'green';
                if (!document.getElementById('input5').dataset.scored) {
                    score++;
                    document.getElementById('input5').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input5').className = 'incorrect';
                document.getElementById('feedback5').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback5').style.color = 'red';
            }

            // Check sentence 6
            const input6 = document.getElementById('input6').value.trim().toLowerCase();
            if (input6 === 'runway') {
                document.getElementById('input6').className = 'correct';
                document.getElementById('feedback6').textContent = 'Correct!';
                document.getElementById('feedback6').style.color = 'green';
                if (!document.getElementById('input6').dataset.scored) {
                    score++;
                    document.getElementById('input6').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input6').className = 'incorrect';
                document.getElementById('feedback6').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback6').style.color = 'red';
            }

            // Check sentence 7
            const input7 = document.getElementById('input7').value.trim().toLowerCase();
            if (input7 === 'fruit market') {
                document.getElementById('input7').className = 'correct';
                document.getElementById('feedback7').textContent = 'Correct!';
                document.getElementById('feedback7').style.color = 'green';
                if (!document.getElementById('input7').dataset.scored) {
                    score++;
                    document.getElementById('input7').dataset.scored = 'true';
                }
            } else {
                document.getElementById('input7').className = 'incorrect';
                document.getElementById('feedback7').textContent = 'Incorrect. Try again!';
                document.getElementById('feedback7').style.color = 'red';
            }

            updateScore();
        }

        function resetWriting() {
            document.querySelectorAll('#writing input[type="text"]').forEach(input => {
                input.value = '';
                input.className = '';
                input.dataset.scored = '';
            });
            document.querySelectorAll('#writing .feedback').forEach(feedback => {
                feedback.textContent = '';
            });
        }

        function selectWordMatch(word) {
            selectedWordMatch = word;
            document.querySelectorAll('.match-item').forEach(item => {
                if (item.textContent === word) {
                    item.classList.add('selected');
                } else {
                    item.classList.remove('selected');
                }
            });
        }

        function selectDefinitionMatch(definition) {
            if (selectedWordMatch) {
                const definitionElement = Array.from(document.querySelectorAll('.match-item')).find(el => el.textContent === definition);
                if (definitionElement) {
                    definitionElement.classList.add('selected');
                    checkMatch(selectedWordMatch, definition);
                }
            }
        }

        function checkMatch(word, definition) {
            const correctPairs = {
                'short': 'measuring or lasting a small distance, time, or amount',
                'co-living': 'a modern form of shared housing where residents with similar values live together',
                'tasks': 'specific pieces of work required to be done as part of one\'s duties',
                'take-off': 'the act or moment of an aircraft becoming airborne',
                'land': 'to come down through the air and settle on the ground',
                'runway': 'a long, narrow strip at an airport where aircraft take off and land',
                'fruit market': 'a market where various kinds of fruits are sold'
            };

            if (correctPairs[word] === definition) {
                document.querySelectorAll('.match-item').forEach(item => {
                    if (item.textContent === word || item.textContent === definition) {
                        item.classList.add('correct');
                        item.classList.remove('selected');
                    }
                });
                if (!document.querySelector(`.match-item:not(.correct):contains('${word}')`).dataset.scored) {
                    score++;
                    document.querySelector(`.match-item:not(.correct):contains('${word}')`).dataset.scored = 'true';
                    updateScore();
                }
            } else {
                alert('Incorrect match. Try again!');
            }
            selectedWordMatch = null;
        }

        function checkMatchingAnswers() {
            updateScore();
        }

        function resetMatching() {
            document.querySelectorAll('.match-item').forEach(item => {
                item.classList.remove('correct', 'selected');
                item.dataset.scored = '';
            });
        }

        function updateScore() {
            document.querySelector('.score').textContent = `Score: ${score} / ${totalScore}`;
        }
    </script>
</body>
</html>
