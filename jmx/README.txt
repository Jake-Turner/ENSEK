Welcome to the automated tools I've developed to help me test the ENSEK Energy Corp. web application.

Included are two tools:
1) A configurable account creator.
2) A configurable stress test for the /Energy/Buy endpoint.

# The Account Creator

Although accounts are not currently functioning, they are a critical part of the application. Testing user accounts is always easier if you can automate the creation of the accounts.
Navigate to "jmx/config/accounts.config", and define accounts by adding a map to the list, with an email and password.
Then, run "jmx/Create Accounts Launcher.bat".
This will run JMeter with the GUI so you can explore the tool, but it can be launched without the GUI to speed up the process.

# The Stress Testing

This tool will randomly order energy, and the tester can ramp up the concurrent thread count to probe what will happen over a two minute exposure.
The tester can also edit the request to specify different order values.
Run "jmx/Buy Energy Stress Test.bat", which will launch the GUI.
It is not advised to run this through the GUI, so edit the values, close the GUI, and add the "-n" flag to run it in headless mode.
In my experience though, you can comfortably run over 100 threads in the GUI with no issue on a reasonably powerful PC.