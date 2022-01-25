# Cache headers
## Request/Response
- Cache-Control
```
	max-age		max-age	<seconds>
			s-maxage	specific to shared caches
			must-revalidate	must validate when stale
			proxy-revalidate	specific to shared caches
	no-cache	no-cache	must be validated before each reuse
	no-store	no-store	no store response in any cache
			private	only store in browsers
			public	can store in shared cache
			must-understand	decide on status code
	no-transform	no-transform	no convert images, etc...
	max-stale	
	min-fresh	
	only-if-cached	
			immutable	bad, consider cache-busting pattern
			stale-while-revalidate
	stale-if-error	stale-if-error
```
- Pragma: no-cache
## Response
- Expires: <http-date> (ignored when Cache-Control: max-age present)
- Age: <delta-seconds> (seconds the object was in a proxy cache)
- Clear-Site-Data (HTTPS only): "cache", "cookies", "storage", "executionContexts", "*"