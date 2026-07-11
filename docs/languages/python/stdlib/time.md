
- time.time() # Returns float of seconds since unix epoch till the current set system-time
- time.monotonic() # Uses OS hardware clocks, that measure absolute time rather than system-time. Returns float of seconds from boot, but only use it as difference btw two calls to this function.
- time.sleep(ms)
- time.perf_counter() # Use for precision
