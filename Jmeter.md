- Site

http://jmeter.apache.org/

- Download

http://jmeter.apache.org/download_jmeter.cgi

- Require

java 1.8+

- Load test cmd

jmeter -n -t [jmx file] -l [results file] -e -o [Path to output folder]

At the end of the test, an HTML report will be generated and available in [Path to output folder] used in command line.

- Generate report from an existing sample CSV log file

jmeter -g [log file] -o [Path to output folder]
