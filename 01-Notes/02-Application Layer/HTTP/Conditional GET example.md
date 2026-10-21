#flashcards/http 
#review2

## 1.  Example when the client does **not** have the [[Web resource]] in its cache
### 1.1 Request message (**normal GET**)
> GET /picture/car.jpg HTTP/1.0
> User-agent: Mozilla/4.0

### 1.2 Response message to the previous request
> HTTP/1.0 <span style="color:red">200 OK </span>
> Date: Wed, 4 Aug 2023 16:21:22
> Server: Apache/1.3.0 (Unix)
> <span style="color:red">Last-Modified</span>: Mon, 2 Jul 2023 12:32:12
> Content-Type: image/jpg
> 
> (.......object content.......)

## 2. Example when the client **does** have the [[Web resource]] in its cache
### 2.1 Request message (conditional GET)
> GET /picture/car.jpg HTTP/1.0
> User-agent: Mozilla/4.0
> <span style="color:red">If-modified-since</span>: Mon, 2 Jul 2023 12:32:12
### 2.2 There are two possibilities: the object has not been modified, or it has been modified.
#### 2.2.1 Server response when the object has **not** been modified
> HTTP/1.0 <span style="color:red">304 Not Modified</span>
> Date: Wed, 4 Aug 2023 18:35:11
> Server: Apache/1.3.0 (Unix)
>   
> (....... <span style="color:red">empty body, no content </span>........)
#### 2.2.2 Server response when the object **has** been modified
> HTTP/1.0 <span style="color:red">200 OK </span>
> Date: Wed, 4 Aug 2023 18:35:11
> Server: Apache/1.3.0 (Unix)
> Last-Modified: Wed, 4 Aug 2023 17:59:43
>
> (....... <span style="color:red">object content</span> .......)

```mermaid
sequenceDiagram
Client ->>+ Server: (1.1) GET /picture/car.jpg
Server ->>- Client: (1.2) 200 OK <br> Last-Modified: Mon, 2 Jul 2023 12:32:12<br>(car.jpg)
Client ->>+ Server: (2.1) GET /picture/car.jpg <br> If-modified-since: Mon, 2 Jul 2023 12:32:12
Server ->>- Client: (2.2.1) 304 Not Modified ()
Client ->>+ Server: (2.1) GET /picture/car.jpg <br> If-modified-since: Mon, 2 Jul 2023 12:32:12
Server ->>- Client: (2.2.2) 200 OK <br> Last-Modified: Tue, 3 Aug 2024 20:43:33<br>(car.jpg)
```
