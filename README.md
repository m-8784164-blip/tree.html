<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grow Your Tree</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #eafbe7;
      padding: 40px;
    }
    h1 {
      color: #2d6a4f;
    }
    #tree {
      width: 300px;
      height: auto;
      margin: 20px auto;
      display: block;
      transition: transform 0.5s ease-in-out;
    }
    button {
      padding: 12px 24px;
      background-color: #40916c;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover {
      background-color: #1b4332;
    }
  </style>
</head>
<body>
  <h1>🌱 Grow Your Virtual Tree 🌳</h1>
  <p>Click the button to water your tree and help it grow!</p>
  
  <img id="tree" src="https://i.ibb.co/0F6s3S8/tree1.png" alt="Tree Growth">
  <br>
  <button onclick="growTree()">💧 Water Tree</button>

  <script>
    // Tree growth images (stable links hosted on i.ibb.co)
    const treeStages = [
      "https://i.ibb.co/0F6s3S8/tree1.png", // stage 1: sprout
      "https://i.ibb.co/p0h1P1s/tree2.png", // stage 2: small tree
      "https://i.ibb.co/fFvJPtK/tree3.png", // stage 3: medium tree
      "https://i.ibb.co/3Nc3RzH/tree4.png"  // stage 4: full tree
    ];
    
    let currentStage = 0;

    function growTree() {
      if (currentStage < treeStages.length - 1) {
        currentStage++;
      } else {
        alert("🌳 Your tree is fully grown! Starting again from sprout.");
        currentStage = 0;
      }
      const tree = document.getElementById("tree");
      tree.src = treeStages[currentStage];
      tree.style.transform = "scale(1.05)";
      setTimeout(() => {
        tree.style.transform = "scale(1)";
      }, 300);
    }
  </script>
</body>
</html>
