




![](../../../../attachments/Pasted%20image%2020261105132039.png)



After inspecting the page this is what i found 

![](../../../../attachments/Pasted%20image%2020261105132159.png)



hahahha
this was me after opening bur suite and didn't know what the fuck to do with it 

![](../../../../attachments/Pasted%20image%2020261105132430.png)


After looking around this is what i think happening :


This is the URL 

```
https://0a53007a04b1a99c84b2271d00b900d7.web-security-academy.net/product?productId=1
```


And this is what the HTML is saying :

```
<img src="/image?filename=7.jpg">
```


So the product wish has the ID = 1 has the file name 7.jpg 

if we put the path traversall in the productid = and send it its going to execture what im thinking of lets try it 


I was right and i didn't copy what i was just talking about this is what i have in my notes 

```
https://insecure-website.com/loadImage?filename=../../../etc/passwd
```


Now i know what im going to use burp for wish is understanding what sort of encryption  happens when the request is sent 




For a while i was working on the wrong input filed 

![](../../../../attachments/Pasted%20image%2020261105134552.png)




![](../../../../attachments/Pasted%20image%2020261105134454.png)




This is what  i should focus on :

![](../../../../attachments/Pasted%20image%2020261105134702.png)



Well done 

![](../../../../attachments/Pasted%20image%2020261105134753.png)



![](../../../../attachments/Pasted%20image%2020261105134824.png)



