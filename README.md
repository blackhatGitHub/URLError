#!/usr/bin/python
# -*- coding: UTF-8 -*-

import urllib2
 request = urllib2.Request('http://www.xxxxx.com')
try:
    urllib2.urlopen(request)
except urllib2.URLError, e:
    print e.reason
===================== RESTART: D:/wangluo163/URLError.py =====================
[Errno 10060] 
>>> 
import urllib2
 
req = urllib2.Request('http://blog.csdn.net/cqcre1')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
    print e.reason
===================== RESTART: D:/wangluo163/URLError.py =====================
403
Forbidden
>>> 
import urllib2
 
req = urllib2.Request('http://blog.csdn1.net/cqcre1')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
    print e.reason
===================== RESTART: D:/wangluo163/URLError.py =====================

Traceback (most recent call last):
  File "D:/wangluo163/URLError.py", line 5, in <module>
    urllib2.urlopen(req)
  File "C:\Python27\lib\urllib2.py", line 154, in urlopen
    return opener.open(url, data, timeout)
  File "C:\Python27\lib\urllib2.py", line 429, in open
    response = self._open(req, data)
  File "C:\Python27\lib\urllib2.py", line 447, in _open
    '_open', req)
  File "C:\Python27\lib\urllib2.py", line 407, in _call_chain
    result = func(*args)
  File "C:\Python27\lib\urllib2.py", line 1228, in http_open
    return self.do_open(httplib.HTTPConnection, req)
  File "C:\Python27\lib\urllib2.py", line 1198, in do_open
    raise URLError(err)
URLError: <urlopen error [Errno 11004] getaddrinfo failed>
>>> 
  import urllib2
 
req = urllib2.Request('http://blog.csdn.net/cqcre1')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
except urllib2.URLError, e:
    print e.reason
else:
    print "OK"
    
===================== RESTART: D:/wangluo163/URLError.py =====================
403
>>> 
import urllib2
 
req = urllib2.Request('http://blog.csdn.net1/cqcre')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
except urllib2.URLError, e:
    print e.reason
else:
    print "OK"
    
===================== RESTART: D:/wangluo163/URLError.py =====================
[Errno 11004] getaddrinfo failed
>>> 
import urllib2
 
req = urllib2.Request('http://blog.csdn.net/cqcre')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
except urllib2.URLError, e:
    print e.reason
else:
    print "OK"
    
===================== RESTART: D:/wangluo163/URLError.py =====================
OK
>>> 
