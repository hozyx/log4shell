# log4shell
Python Script to scan server file system for log4j jars that are vulnerable to CVE-2021-44228 and CVE-2021-45046. The script recursively goes through the file system (including zip, ear, war) to find log4j versions 2.* to 2.15 with org/apache/logging/log4j/core/lookup/JndiLookup.class.  

The script takes the file system path to scan as input and lists down the vulnerable jar File Path, Bundle Version and Bundle Name. The values are colon ":" separated. This output format is useful if the script is executed by an orchestration tool like Ansible and needs to be machine readable. 

The scripts supports additional options --Summary and --UnprocessedFiles to print more details of the scan

