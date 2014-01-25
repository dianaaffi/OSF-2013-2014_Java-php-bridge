OSF-2013-2014_Java-php-bridge
=============================

Comparing Java/Php Bridge using RMI performance and web services calls from PHP to a JAVA web application.


<h1>PHP/JAVA Bridge</h1>
<p>PHP/JAVA Bridge is a framework used to enable the communication from a php script to java webservices via RMI. This project is built to show a brief comparison between performance results of simple REST requests and RMI reauests using PHP/JAVA Bridge from a PHP script to a JAVA web application.</p>

<h1>Documentation</h1>
The official documentation of this framework can be found on the <a href="http://php-java-bridge.sourceforge.net/pjb/">web</a>.
Our documentation can be found in this repository under the name presentation. It also contains a guide for the installation of the project environment and the test cases and results.
All necessary source codes for running tests are also found in this repository.

<h1>Test setup</h1>
Follow these steps to perform a test comparing the REST calls to RMI calls between PHP and JAVA:
<ol>
<li>Run 2 application servers, on for the client PHP application and the other for the JAVA web application.
<li>Deploy the JavaBridge.war provided in this repository in your client side server (server hosting your php application). This web archive contains:
<ul>
<li>all the files necessary to establish a bridge between JAVA and PHP application</li>
<li>a php script that calls 4 REST web services on our JAVA web application "RESTCalls.php"</li>
<li>a php script that calls the same methods via IIOP "RMICalls.php"</li>
</ul>
</li>
<li>Change in the RMI call script mentioned before, the address of your java web application server from where to fetch the NamingContext.</li>
<li>Deploy the Java web application "GamificationRMI.jar" on the second application server</li>
<li>Open the test case "PHPJAVABridgeTest.jmx" in JMeter and set the destination base url to your first application server base url</li>
<li>Launch the test</li>
<li>Check the response time differences in the resulting graphs</li>
</ol>



<h1>Authors</h1>
<ul>
<li>Diana AFFI</li>
<li>Joseph EL MALLAH</li>
<li>Ahmed HACHMi</li>


