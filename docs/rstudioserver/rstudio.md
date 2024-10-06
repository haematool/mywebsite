# R Studio Server Access

You can access the R Studio server using the following link:

<div style="text-align: center; margin: 20px 0;">
  <a href="http://134.209.84.93:8787/" target="_blank" style="padding: 10px 20px; background-color: #607D8B; color: white; text-decoration: none; border-radius: 5px; font-family: Arial, sans-serif; font-size: 16px;">Access R Studio Server</a>
</div>

<div style="text-align: center; margin-bottom: 20px;">
  <span id="status-indicator" style="display: inline-block; width: 10px; height: 10px; background-color: grey; border-radius: 50%; margin-right: 8px;"></span>
  <span id="status-text" style="font-family: Arial, sans-serif; color: grey;">Checking server status...</span>
</div>

The server is set up to assist with statistical analyses on medical data. If you need help or further information, feel free to contact me via email or LinkedIn.

## Request Access

If you'd like to request the ID and password for the R Studio server, please fill out the form below:

<div style="width: 100%; max-width: 700px; margin: 20px auto; padding: 20px; background-color: #f9f9f9; border-radius: 15px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);">
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSd2rWo541S8NnbbWnRoslqktEKN7Tu3F5P7-Ax5a_skCvip9A/viewform?embedded=true" 
            width="100%" 
            height="500" 
            frameborder="0" 
            style="border-radius: 15px; overflow: hidden; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);">
    </iframe>
</div>

<script>
  function checkServerStatus() {
    // Ping the Nginx server to check if it's online
    fetch('http://134.209.84.93/', {
        method: 'GET',
        mode: 'cors'  // Allow CORS (Cross-Origin Resource Sharing)
      })
      .then(response => {
        if (response.ok) {
          // Server is online, update the status to green
          document.getElementById('status-indicator').style.backgroundColor = '#4CAF50';
          document.getElementById('status-text').innerText = 'Nginx server is online';
          document.getElementById('status-text').style.color = '#4CAF50';
        } else {
          // Server is unreachable, update the status to red
          document.getElementById('status-indicator').style.backgroundColor = 'red';
          document.getElementById('status-text').innerText = 'Nginx server is offline';
          document.getElementById('status-text').style.color = 'red';
        }
      })
      .catch(() => {
        // If the request fails, the server is offline
        document.getElementById('status-indicator').style.backgroundColor = 'red';
        document.getElementById('status-text').innerText = 'Nginx server is offline';
        document.getElementById('status-text').style.color = 'red';
      });
  }

  // Check server status every 30 seconds
  setInterval(checkServerStatus, 30000);

  // Initial check when the page loads
  checkServerStatus();
</script>

