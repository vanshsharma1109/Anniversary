<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>I'm Sorry Aanya</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ffe5ec, #ffc1cc);
      color: #2e2e2e;
      text-align: center;
      padding: 2rem;
      overflow-x: hidden; /* Prevent horizontal scroll */
    }

    .container {
      max-width: 600px;
      margin: auto;
    }

    h1, h2 {
      animation: popIn 1s ease-in-out;
      color: #ff4f81;
    }

    .fade-in {
      opacity: 0;
      animation: fadeIn 2s ease-in-out forwards;
    }

    .fade-in-delay {
      opacity: 0;
      animation: fadeIn 3s ease-in-out 1s forwards;
    }

    .photo {
      width: 80%;
      max-width: 300px;
      margin: 1rem auto;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
    }

    .hidden {
      display: none;
    }

    .btn {
      display: inline-block;
      margin: 1rem 0.5rem;
      background-color: #ff4f81;
      color: white;
      padding: 0.8rem 1.5rem;
      text-decoration: none;
      font-weight: bold;
      border-radius: 8px;
      box-shadow: 0 5px 10px rgba(0,0,0,0.2);
      transition: background 0.3s;
      cursor: pointer;
    }

    .btn:hover {
      background-color: #e04573;
    }

    video {
      margin-top: 1rem;
      max-width: 100%;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }

    .memories-container {
      margin-top: 2rem;
    }

    @keyframes fadeIn {
      to { opacity: 1; }
    }

    @keyframes popIn {
      0% {
        transform: scale(0.7);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <!-- Page 1: Apology -->
  <div class="container" id="page1">
    <h1 class="fade-in">SORRY</h1>
    <p class="fade-in-delay">
      I know I made choices that hurt you, and I deeply regret them. <br>
      Not a day goes by without thinking about how I could've been better — for us. <br><br>
      Aanya, from the bottom of my heart, I’m truly sorry. <br>
      If there's even the smallest place left in your heart for me... <br>
      I wish to return, to make things right, and hold onto the love we once shared. <br><br>
      Happy Anniversary for 20th May — the date my heart will never forget. 💛
    </p>
    <button class="btn" onclick="goToLovePage()">Next ➜</button>
  </div>

  <!-- Page 2: Love + Memories -->
  <div class="container hidden" id="lovePage">
    <h1>I really love you ❤️</h1>
    <p style="font-size: 1.2rem; margin-top: 1rem;">
      You are the one I want to laugh with, cry with, and grow old with. <br>
      Always have, always will. 💖
    </p>

    <button class="btn" onclick="goToPage1()">⬅ Back</button>
    <button class="btn" onclick="goToProposalPage()">Next ➜</button>

    <!-- Memories shown below on the same page -->
    <div class="memories-container">
      <h2 style="margin-top: 3rem;">Some memories... 💛</h2>
      <img src="WhatsApp Image 2025-05-13 at 4.14.32 PM.jpeg" alt="Rose" class="photo"/>
      <img src="Screenshot_2024-05-03-00-33-32-022_com.whatsapp.jpg" alt="Us together" class="photo"/>
      <video controls>
        <source src="WhatsApp Video 2025-05-13 at 4.14.30 PM.mp4" type="video/mp4" />
        Your browser does not support the video tag.
      </video>
    </div>
  </div>

  <!-- Page 3: Proposal -->
  <div class="container hidden" id="proposalPage">
    <h1 style="color: #d6336c;">One More Question... 💍</h1>
    <p style="font-size: 1.2rem; margin-top: 1rem;">
      On this anniversary of ours, I propose again to you — with the same love, deeper understanding, and stronger heart. <br>
      Will you take this journey with me again?
    </p>
    <video controls class="fade-in-delay">
      <source src="WhatsApp Video 2025-05-13 at 4.25.38 PM.mp4" type="video/mp4" />
      Your browser does not support the video tag.
    </video>
    <br>
    <button class="btn" onclick="goToLovePage()">⬅ Back</button>
  </div>

  <!-- JavaScript -->
  <script>
    function goToPage1() {
      document.getElementById("lovePage").classList.add("hidden");
      document.getElementById("proposalPage").classList.add("hidden");
      document.getElementById("page1").classList.remove("hidden");
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    function goToLovePage() {
      document.getElementById("page1").classList.add("hidden");
      document.getElementById("proposalPage").classList.add("hidden");
      document.getElementById("lovePage").classList.remove("hidden");
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    function goToProposalPage() {
      document.getElementById("lovePage").classList.add("hidden");
      document.getElementById("proposalPage").classList.remove("hidden");
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>
</body>
</html>
