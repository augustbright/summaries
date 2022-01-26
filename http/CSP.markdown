Content-Security-Policy: <policy-directive>; <policy-directive>
<meta http-equiv="Content-Security-Policy" content="<policy-directive>; <policy-directive>">


### Fetch directives
Fetch directives control the locations from which certain resource types may be loaded.

- default-src - fallback for other fetch directives
- script-src - javascript
- style-src - stylesheets
- font-src - fonts loaded using @font-face
- img-src - images and favicons
- child-src - web workers and nested browsing contexts
- connect-src - < a ping >, JS APIs
- frame-src - nested browsing contexts (frame, iframe)
- manifest-src - application manifest files
- media-src - < audio >, < video >, < track >
- object-src - < object >, < embed >, < applet >

#### experimental
- prefetch-src - rel="prefetch"
- srcipt-src-elem
- script-src-attr
- style-src-elem
- style-src-attr
- worker-src

### Document directives
Document directives govern the properties of a document or worker environment to which a policy applies

- base-uri - < base > element
- sandbox - enable sandbox

### Navigation directives
Navigation directives govern to which locations a user can navigate or submit a form, for example.

- form-action
- frame-ancestors - parents for < frame >, < iframe >, < object >, < embed >, or < applet >

#### experimental
- navigate-to - navigation by any means

### Other directives
- upgrade-insecure-requests

#### experimental
- require-sri-for
- require-trusted-types-for
- trusted-types


### Keyword values
- none - Won't allow loading of any resources
- self - Only allow resources from the current origin

#### experimental
- strict-dynamic
- report-sample

### Unsave values
- unsafe-inline - Allow use of inline resources
- unsafe-eval - Allow use of dynamic code evaluation such as eval, setImmediate, and window.execScript 

#### experimental
- unsafe-hashes
- unsafe-allow-redirects

### Hosts values
- Host
	- example.com, *.example.com, https://*.example.com:12/path/to/file.js
	- example.com/api/
	- example.com/file.js
- Scheme - https:, http:, data: etc.

### Other values
- nonce-*
- sha*-*

