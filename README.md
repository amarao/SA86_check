This ansible playbook helps to check if host is vulnerable to Intel-SA-00086.

It covers following CVEs:

* Intel® Management Engine (ME) 11.x: CVE-2017-5705 , CVE-2017-5708, CVE-2017-5711, CVE-2017-5712
* Intel® Server Platform Service 4.0.x.x : CVE-2017-5706 , CVE-2017-5709
* Intel® Trusted Execution Engine (TXE) 3.0 : CVE-2017-5707 , CVE-2017-5710

How to run
----------

```
ansible-playbook -i host1,host2,host3, sa86_check.yaml
```
(note: if you are using one host, use is with coma at end: `-i host,`)

Or, if you have your inventory:
```
ansible-playbook -i your_inventory sa86_check.yaml
```

Result: output to stdout of check result. Green is not vulnerable, yellow if vulnerable or
unknown.
