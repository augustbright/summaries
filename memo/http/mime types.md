# MIME types

type/subtype
type/subtype;parameter=value

*Discrete types*
- application
- audio
- example
- font
- image
- model
- text
- video

*Multipart types*
- message
- multipart

*Important types for web*
- application/octet-stream (means unknown)
- text/plain (unknown human-readable)
- text/css
- text/html
- text/javascript

*multipart/form-data*
```
Content-Type: multipart/form-data; boundary=aBoundaryString

--aBoundaryString
Content-Disposition: form-data; name="myFile"; filename="img.jpg"
Content-Type: image/jpg

(data)
--aBoundaryString
Content-Disposition: form-data; name="myField"

(data)
--aBoundaryString
(more subparts)
--aBoundaryString--
```

*multipart/byteranges*
```
Accept-Ranges: bytes
Content-Type: multipart/byteranges; boundary=123
Content-Length: 385

--123
Content-Type: text/html
Content-Range: bytes 100-200/1270

(fragment)
--123--
```
