<p align="center">
<img src="https://i.imgur.com/9Ab7VoK.png" height="80%" width="80%" alt="Patriot CTF"/>
<p/>
<h1>PatriotCTF 2023: Rouge Access Point (OSINT)</h1>
PatriotCTF 2023 is a Jeopardy-style CTF competition organized by the MasonCC (Mason Competitive Cyber) club at George Mason University.
<br/>
<br/>
<h2>Challenge Description:</h2> 
<p align="center">
"We've received a notice from our companies EDR software that a laptop was attacked while they were on WFH. The employee says they were at home when it happened, but we suspect they were using public wifi. Our EDR software managed to capture the BSSID of the wifi (46:D1:FA:63:BC:66) network before it got disconnected, but not the SSID. Can you still find the network they were connected to?"
<br/>
<br/>
Flag format: <strong>PCTF{SSID}</strong>
<br/>
<br/>
<h2>Solution:</h2> 
<p align="center">
The prompt provides a BSSID of the Wi-Fi network, which is suspected to be a public Wi-Fi network. To start, I navigated to https://wigle.net/, a website that provides wireless network information and allows users to search and map wireless network locations globally. I created an account, and then clicked 'View' and 'Basic Search.' Without creating an account the website features are limited, and the 'Basic Search' functionality would not be available. I entered in the provided BSSID (46:D1:FA:63:BC:66), and cleared all the other fields. 
<br />
<br />
<img src="https://i.imgur.com/x60OEsr.png" height="35%" width="35%" alt="Basic Search"/> 
<br />
<br />
After querying for results, the site returned the following information: 
<br />
<br />
<img src="https://i.imgur.com/mR3djOM.png" height="50%" width="50%" alt="Map"/> 
<br />
<br />
<img src="https://i.imgur.com/PNyYTFR.png" height="50%" width="50%" alt="Latitude Longitude Values"/> 
<br />
<br />
<img src="https://i.imgur.com/WkwXUkc.png" height="50%" width="50%" alt="SSID Information"/> 
<br />
<br />
Running this search provided the location of the WiFi network, as well as the SSID: @Red's Table Free Wifi. 
<br />
<br />
The flag value is <strong>PCTF{@Red's Table Free Wifi}</strong>!
<h2>Key takeaways:</h2>
<p align="center">
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
