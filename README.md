
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adubia JHS SRC E-Voting System</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f0f5f2;
            color: #243047;
            text-align: center;
            margin: 0;
            padding: 20px;
        }

        h1 {
            background-color: #075b3c;
            color: white;
            padding: 25px;
            border-radius: 10px;
        }

        h2 {
            color: #075b3c;
        }

        p {
            font-size: 16px;
            line-height: 1.6;
        }

        nav {
            background-color: #06452f;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            margin: 5px 10px;
            display: inline-block;
        }

        nav a:hover {
            color: #f2c94c;
        }

        section {
            scroll-margin-top: 15px;
        }

        .welcome {
            background-color: #e3f4eb;
            padding: 30px 15px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .welcome h2 {
            margin-bottom: 15px;
        }

        .btn {
            display: inline-block;
            background-color: #075b3c;
            color: white;
            padding: 12px 22px;
            margin-top: 15px;
            border: none;
            border-radius: 6px;
            text-decoration: none;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #043d29;
        }

        #candidates,
        .vote-section,
        .results-section {
            background-color: white;
            padding: 25px 15px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .candidate-container {
            display: grid;
            grid-template-columns:
                repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .candidate-card {
            background-color: #f0f5f2;
            border: 1px solid #cbded2;
            padding: 20px;
            border-radius: 8px;
        }

        .candidate-card h3,
        .result-card h3 {
            color: #075b3c;
        }

        .vote-section form {
            max-width: 450px;
            margin: 20px auto 0;
            text-align: left;
        }

        .vote-section label {
            display: block;
            margin-top: 15px;
            font-weight: bold;
        }

        .vote-section input,
        .vote-section select {
            display: block;
            width: 100%;
            padding: 12px;
            margin-top: 6px;
            border: 1px solid #bdc9c1;
            border-radius: 6px;
            font-size: 16px;
        }

        .vote-section button {
            width: 100%;
        }

        #voteMessage {
            text-align: center;
            margin-top: 15px;
            padding: 10px;
            border-radius: 6px;
            font-weight: bold;
        }

        .result-card {
            background-color: #f0f5f2;
            border-left: 5px solid #075b3c;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
        }

        #totalVotes {
            font-weight: bold;
            margin-top: 20px;
        }

        footer {
            background-color: #06452f;
            color: white;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            font-size: 14px;
        }

        footer p {
            margin: 5px;
        }

        @media (max-width: 480px) {
            body {
                padding: 10px;
            }

            h1 {
                padding: 20px 10px;
                font-size: 25px;
            }

            nav a {
                margin: 5px;
            }
        }
    </style>
</head>

<body>

    <h1>ADUBIA JHS</h1>
    <h2>SRC ELECTION 2026</h2>
    <p>Welcome to the Electronic Voting System.</p>
    <p>Your vote, your voice, your future!</p>

    <nav>
        <a href="#home">Home</a>
        <a href="#candidates">Candidates</a>
        <a href="#vote">Vote</a>
        <a href="#results">Results</a>
    </nav>

    <section id="home" class="welcome">
        <h2>Welcome to the SRC Election</h2>

        <p>
            Welcome to the Adubia JHS Electronic Voting System.
        </p>

        <p>Your vote, your voice, your future!</p>

        <a href="#vote" class="btn">Vote Now</a>
    </section>

    <section id="candidates">
        <h2>Meet the Candidates</h2>
        <p>Choose the leader you believe in.</p>

        <div class="candidate-container">

            <div class="candidate-card">
                <h3>Candidate One</h3>
                <p>Position: SRC President</p>
                <p>Slogan: Leadership Through Service</p>
            </div>

            <div class="candidate-card">
                <h3>Candidate Two</h3>
                <p>Position: SRC President</p>
                <p>Slogan: Together We Can</p>
            </div>

            <div class="candidate-card">
                <h3>Candidate Three</h3>
                <p>Position: SRC President</p>
                <p>Slogan: A Better School for All</p>
            </div>

        </div>
    </section>

    <section id="vote" class="vote-section">
        <h2>Cast Your Vote</h2>

        <p>
            Enter your student ID and select your preferred candidate.
        </p>

        <form id="voteForm">

            <label for="studentId">Student ID:</label>
            <input
                type="text"
                id="studentId"
                placeholder="Enter your student ID"
                required
            >

            <label for="candidate">Choose your candidate:</label>
            <select id="candidate" required>
                <option value="">-- Select a candidate --</option>
                <option value="Candidate One">Candidate One</option>
                <option value="Candidate Two">Candidate Two</option>
                <option value="Candidate Three">Candidate Three</option>
            </select>

            <button type="submit" class="btn">
                Submit Vote
            </button>

            <p id="voteMessage" aria-live="polite"></p>

        </form>
    </section>

    <section id="results" class="results-section">
        <h2>Election Results</h2>

        <p>See the votes received by each candidate.</p>

        <div class="result-card">
            <h3>Candidate One</h3>
            <p>Votes: <span id="votesOne">0</span></p>
        </div>

        <div class="result-card">
            <h3>Candidate Two</h3>
            <p>Votes: <span id="votesTwo">0</span></p>
        </div>

        <div class="result-card">
            <h3>Candidate Three</h3>
            <p>Votes: <span id="votesThree">0</span></p>
        </div>

        <p id="totalVotes">Total votes cast: 0</p>
    </section>

    <footer>
        <p>&copy; 2026 Adubia JHS SRC E-Voting System</p>
        <p>Designed to promote fair and responsible student elections.</p>
    </footer>

    <script>
        const voteForm = document.getElementById("voteForm");
        const voteMessage = document.getElementById("voteMessage");

        const votesOneDisplay = document.getElementById("votesOne");
        const votesTwoDisplay = document.getElementById("votesTwo");
        const votesThreeDisplay = document.getElementById("votesThree");
        const totalVotesDisplay = document.getElementById("totalVotes");

        let votesOne = 0;
        let votesTwo = 0;
        let votesThree = 0;
        let totalVotes = 0;

        const votedStudentIds = new Set();

        function updateResults() {
            votesOneDisplay.textContent = votesOne;
            votesTwoDisplay.textContent = votesTwo;
            votesThreeDisplay.textContent = votesThree;

            totalVotesDisplay.textContent =
                "Total votes cast: " + totalVotes;
        }

        voteForm.addEventListener("submit", function(event) {
            event.preventDefault();

            const studentId = document
                .getElementById("studentId")
                .value.trim()
                .toUpperCase();

            const selectedCandidate =
                document.getElementById("candidate").value;

            if (votedStudentIds.has(studentId)) {
                voteMessage.textContent =
                    "This student ID has already voted.";
                voteMessage.style.color = "red";
                return;
            }

            if (
                selectedCandidate !== "Candidate One" &&
                selectedCandidate !== "Candidate Two" &&
                selectedCandidate !== "Candidate Three"
            ) {
                voteMessage.textContent =
                    "Please select a candidate.";
                voteMessage.style.color = "red";
                return;
            }

            votedStudentIds.add(studentId);

            if (selectedCandidate === "Candidate One") {
                votesOne++;
            } else if (selectedCandidate === "Candidate Two") {
                votesTwo++;
            } else if (selectedCandidate === "Candidate Three") {
                votesThree++;
            }

            totalVotes++;

            updateResults();

            voteMessage.textContent =
                "Your vote has been submitted successfully!";
            voteMessage.style.color = "#075b3c";

            voteForm.reset();
        });
    </script>

</body>
</html>
