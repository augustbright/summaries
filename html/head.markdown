## metadata (name="" content="")
```
HTML SPEC NAMES
application-name	Simple web pages shouldn't define an application-name
author			
description
generator		software that generated the page
keywords
referrer	HTTP Referer header for to requests sent from the document
			no-referrer
			origin
			no-referrer-when-downgrade
			origin-when-cross-origin
			same-origin
			strict-origin
			strict-origin-when-cross-origin
			unsafe-URL
theme-color="<CSS color>"
color-scheme	Specify compatible modes
			normal
			light | dark
			only light

OTHER SPEC
width/height	"device-width/device-height/integer"
initial-scale="0.0 - 10.0"
user-scalable="yes|no"
minimum-scale/maximum-scale="0.0 - 10.0"
viewport-fit="auto | contain | cover"

SOME OTHER
creator
publisher
robots(googlebot) - comma-separated values:
	index/noindex
	follow/nofollow
	all/none
	noarchive(nocache)
	nosnippet
	noimageindex
og:image
og:description
og:title
twitter:title
```

## http-equiv
```
content-security-policy
content-type
default-style
x-ua-compatible="IE=edge"
refresh="10[;url=...]"
```

## link attributes
```
href - abolute or relative
hreflang

REL
	stylesheet		prefetch
	icon			preload
	apple-touch-icon	modulepreload
	apple-touch-startup-image
	manifest

	next/prev
	tag/author
	help/license/search
	canonical

AS
	audio/video
	font
	document
	embed/object/track
	fetch
	font
	image
	style/script/worker

media - media type/mediaquery

crossorigin="anonymous | use-credentials"
disabled
imagessizes
imagesrcset
type - MIME type

```

# script
```
src
type
	omitted or JS MIME
	module
	other - not processed by browser
async - load in parallel, eval ASAP
defer - document parsed -> EVAL -> DOMContentLoaded

integrity - hash
nonce - crypto nubber for CSP
referrer
nomodule - eval if ES2015 modules unsupported
```