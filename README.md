# SB-SSL
<p>Enable HTTPS / SSL in Spring Boot Application</p>

<table>
  <tbody>
    <tr>
      <th>Acronym</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>SB</td>
      <td>Spring Boot</td>
    </tr>
    <tr>
      <td>HTTPS</td>
      <td>HyperText Transfer Protocol Secure</td>
    </tr>
    <tr>
      <td>SSL</td>
      <td>Secure Sockets Layer</td>
    </tr>
  </tbody>
</table>


<strong>Open Command Prompt:</strong>
<p>Go to Project Location:</p>
<li>C:\Users\XXXX\Desktop\SB-SSL-Project></li>
<p>Type:</p>
<p>keytool -genkey -alias chocolate -storetype PKCS12 -keyalg RSA -keysize 2048 -keystore chocolate.p12 -validity 365</p>
<p>Press Enter>/p>

<p>Enter keystore password: XXXX</p>

<p>Re-enter new password: XXXX</p>

<p>What is your first and last name?</p>
<li>FN LN</li>

<p>What is the name of your organizational unit?</p>
<li>OU</li>

<p>What is the name of your organization?</p>
<li>O</li>

<p>What is the name of your City or Locality?</p>
<li>C</li>

<p>What is the name of your State or Provice?</p>
<li>S</li>

<p>What is the two-letter country code for this unit?</p>
<li>PK</li>

<p>Is CN=FN LN, OU=OU, O=O, L=C, ST=S, C=PK correct?</p>
<li>[no]: yes</li>

<strong>Refresh you Project in IDE</strong>
<p>move chocolate.p12 to src\main\resource folder</p>

<strong>Modify application.properties files to bind self-signed certificate with server</strong>

<li>server.port=8443</li>
<li>server.ssl.key-alias=chocolate</li>
<li>server.ssl.key-store-password=chocolate</li>
<li>server.ssl.key-store=classpath:chocolate.p12</li>
<li>server.ssl.key-store-type=PKCS12</li>
