# Structure
type/subtype
type/subtype;parameter=value
descrete, multipart types

## Descrete types
- application
- text
- font
- image
- audio
- video
- model
- example

## Multipart types
- message
- multipart

## Important types for web
- application/octet-stream - unknown binary file, browsers propose "Save As"
- text/plain - unknown textual file, browsers display it

- text/css, text/html ( application/xml, application/xhtml+xml )
- text/javascript (bad: application/javascript, application/ecmascript, text/ecmascript)

### Image types
- image/png, image/apng - (Animated) Portable Network Graphics, APNG, PNG. apng, png
- image/jpeg - Joint Photographic Expert Group, JPEG. jpeg, jpg, jfif, pjpeg, pjp
- image/gif - Graphics Interchange Format, GIF. gif
- image/svg+xml - Scalable Vector Format, SVG. svg
- image/webp - Web Picture Format, WEBP. webp
- image/avif - AV1 Image  File Format, AVIF. avif

not recommended
- image/bmp - Bitmap File, BMP. bmp
- image/x-icon - icrosoft Icon, ICO. ico, cur
- image/tiff - Tagged Image File Format, TIFF. tiff, tif

### Audio, video
- audio/wave, audio/wav, audio/x-wav, audio/x-pn-wav
- audio/webm
- video/webm
- audio/ogg
- video/ogg
- application/ogg

- audio/aac

### Multipart/form-data
Content-Type: multipart/form-data; boundary=aBoundaryString
...

--aBoundaryString
Content-Disposition: form-data; name="myFile"; filename="img.jpg"
Content-Type: image/jpeg

(data)
--aBoundaryString
Content-Disposition: form-data; name="myField"

(data)
--aBoundaryString
(more subparts)
--aBoundaryString--

### multipart/byteranges
HTTP/1.1 206 Partial Content
Accept-Ranges: bytes
Content-Type: multipart/byteranges; boundary=3d6b6a416f9b5
Content-Length: 385

--3d6b6a416f9b5
Content-Type: text/html
Content-Range: bytes 100-200/1270

eta http-equiv="Content-type" content="text/html; charset=utf-8" />
    <meta name="vieport" content
--3d6b6a416f9b5
Content-Type: text/html
Content-Range: bytes 300-400/1270

-color: #f0f0f2;
        margin: 0;
        padding: 0;
        font-family: "Open Sans", "Helvetica
--3d6b6a416f9b5--

