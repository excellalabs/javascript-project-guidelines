# React API Libraries

# Axios

• Promise-based
• Automatically succeeds/fails based on request code (2XX-3xx -> Then, else Catch)
• Seems to be the industry standard for React
• Has unit test support (MockAdapter)
• JSON Responses

# Fetch

• Built-in JS API system
• Promise-based
• Not easily supported by IE, but polyfills are available

# SuperAgent

• Axios alternative
• Possibly faster for use in NodeJS, but slower than Axios in browser

# React-Query

• Does not own it’s own API requests, but is a wrapper to aid with more complicated # Request logic
• Would require something like Axios or Fetch to operate
• Hook-based
• Worth investigating for more complicated uses

# Questions

• Is there an RxJS-ready React API library?

# Conclusion

• Use Axios, as a default choice for better security, better cross-browser support, and testing support
• Socket.io is our default choice for the odd occasion when sockets are asked for
