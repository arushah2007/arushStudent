# Cookie Clicker Game
Click the cookie to earn points! Buy upgrades to increase your earnings, but beware of the random fire event!
<div style="text-align:center;">
  <h1>Cookie Clicker</h1>
  <p>Points: <span id="points">0</span></p>
  <!-- Cookie button -->
  <button id="cookie" style="font-size: 200px; background: none; border: 0px; filter: drop-shadow(5px 5px 5px gray);">🍪</button>
  <h2>Upgrades</h2>
  <!-- Click Multiplier Upgrades -->
  <div>
    <p>Click Multiplier (x2) - Cost: 50 Points</p>
    <button id="click-upgrade-1" disabled>Buy 1 Click Multiplier</button>
    <button id="click-upgrade-10" disabled>Buy 10 Click Multipliers</button>
  </div>
  <div>
    <p>Click Multiplier (x5) - Cost: 200 Points</p>
    <button id="click-upgrade-5-1" disabled>Buy 1 Click Multiplier x5</button>
    <button id="click-upgrade-5-10" disabled>Buy 10 Click Multipliers x5</button>
  </div>
  <div>
    <p>Click Multiplier (x10) - Cost: 1000 Points</p>
    <button id="click-upgrade-10-1" disabled>Buy 1 Click Multiplier x10</button>
    <button id="click-upgrade-10-10" disabled>Buy 10 Click Multipliers x10</button>
  </div>
  <!-- Auto-clicker Upgrades -->
  <div>
    <p>Auto-Clicker (1 point/sec) - Cost: 100 Points</p>
    <button id="auto-upgrade-1" disabled>Buy 1 Auto-Clicker</button>
    <button id="auto-upgrade-10" disabled>Buy 10 Auto-Clickers</button>
  </div>
  <div>
    <p>Auto-Clicker (5 points/sec) - Cost: 500 Points</p>
    <button id="auto-upgrade-5-1" disabled>Buy 1 Auto-Clicker x5</button>
    <button id="auto-upgrade-5-10" disabled>Buy 10 Auto-Clickers x5</button>
  </div>
  <div>
    <p>Auto-Clicker (10 points/sec) - Cost: 2000 Points</p>
    <button id="auto-upgrade-10-1" disabled>Buy 1 Auto-Clicker x10</button>
    <button id="auto-upgrade-10-10" disabled>Buy 10 Auto-Clickers x10</button>
  </div>
</div>
<script>
  let points = 0;
  let pointsPerClick = 1;
  let autoClicker = 0;
  let clickMultipliers = 1;
  let autoClickMultiplier = 0;
  // Function to update the points display
  function updatePoints() {
    points += pointsPerClick * clickMultipliers;
    document.getElementById('points').textContent = points;
    checkUpgrades();
  }
  // Function to check if upgrades can be purchased
  function checkUpgrades() {
    // Enable or disable upgrade buttons based on points
    document.getElementById('click-upgrade-1').disabled = points < 50;
    document.getElementById('click-upgrade-10').disabled = points < 500;
    document.getElementById('click-upgrade-5-1').disabled = points < 200;
    document.getElementById('click-upgrade-5-10').disabled = points < 2000;
    document.getElementById('click-upgrade-10-1').disabled = points < 1000;
    document.getElementById('click-upgrade-10-10').disabled = points < 10000;
    document.getElementById('auto-upgrade-1').disabled = points < 100;
    document.getElementById('auto-upgrade-10').disabled = points < 1000;
    document.getElementById('auto-upgrade-5-1').disabled = points < 500;
    document.getElementById('auto-upgrade-5-10').disabled = points < 5000;
    document.getElementById('auto-upgrade-10-1').disabled = points < 2000;
    document.getElementById('auto-upgrade-10-10').disabled = points < 20000;
  }
  // Click multiplier upgrade
  function buyClickMultiplier(multiplier, cost, amount) {
    if (points >= cost * amount) {
      points -= cost * amount;
      clickMultipliers += multiplier * amount;
      document.getElementById('points').textContent = points;
      checkUpgrades();
    }
  }
  // Auto-clicker upgrade
  function buyAutoClicker(multiplier, cost, amount) {
    if (points >= cost * amount) {
      points -= cost * amount;
      autoClickMultiplier += multiplier * amount;
      document.getElementById('points').textContent = points;
      checkUpgrades();
    }
  }
  // Random fire event
  function randomFireEvent() {
    setTimeout(function() {
      document.getElementById('cookie').textContent = '🔥';
      points = 0;
      document.getElementById('points').textContent = points;
      checkUpgrades();
      setTimeout(function() {
        document.getElementById('cookie').textContent = '🍪';
      }, 3000); // Change back to a cookie after 3 seconds
    }, Math.random() * 60000); // Random time between 0 and 60 seconds
  }
  // Start the fire event at a random time
  randomFireEvent();
  // Adding event listener to the cookie button
  document.getElementById('cookie').addEventListener('click', updatePoints);
  // Upgrading click multipliers
  document.getElementById('click-upgrade-1').addEventListener('click', function() { buyClickMultiplier(1, 50, 1); });
  document.getElementById('click-upgrade-10').addEventListener('click', function() { buyClickMultiplier(1, 50, 10); });
  document.getElementById('click-upgrade-5-1').addEventListener('click', function() { buyClickMultiplier(5, 200, 1); });
  document.getElementById('click-upgrade-5-10').addEventListener('click', function() { buyClickMultiplier(5, 200, 10); });
  document.getElementById('click-upgrade-10-1').addEventListener('click', function() { buyClickMultiplier(10, 1000, 1); });
  document.getElementById('click-upgrade-10-10').addEventListener('click', function() { buyClickMultiplier(10, 1000, 10); });
  // Upgrading auto-clickers
  document.getElementById('auto-upgrade-1').addEventListener('click', function() { buyAutoClicker(1, 100, 1); });
  document.getElementById('auto-upgrade-10').addEventListener('click', function() { buyAutoClicker(1, 100, 10); });
  document.getElementById('auto-upgrade-5-1').addEventListener('click', function() { buyAutoClicker(5, 500, 1); });
  document.getElementById('auto-upgrade-5-10').addEventListener('click', function() { buyAutoClicker(5, 500, 10); });
  document.getElementById('auto-upgrade-10-1').addEventListener('click', function() { buyAutoClicker(10, 2000, 1); });
  document.getElementById('auto-upgrade-10-10').addEventListener('click', function() { buyAutoClicker(10, 2000, 10); });
  // Auto-clicker logic (adds points every second based on auto-click multiplier)
  setInterval(function() {
    points += autoClickMultiplier;
    document.getElementById('points').textContent = points;
    checkUpgrades();
  }, 1000);
</script>
