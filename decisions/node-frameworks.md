# Node Frameworks

When determining what Node Framework to use, we recommend NEST (with Angular) or NEXT (with React) over vanilla Express to save yourself configuration headaches. With that being said, Express, NEST, and NEXT are all mature enough to be grabbed for a project and Express is most likely to get through government approvals due to its ubiquity and maturity. Excella does not have widespread experience with any of these back-ends, but some individuals do. Below are some more detailed pros and cons for each Node Framework that Excellians have experience with or knowledge of.

## NEST

-	Node, Express, SocketIO, Typescript
-	Angular-like API Framework
-	Very easy to grok for Angular (2+) devs
-	Strongly opinionated
-	Provides lots of dev-friendly things out of the box
-	Try/Catch inherently
-	Auto-parsing of Response Body
-	Actively supported
-	Can serve static files
-	GraphQL Wrapper is available
-	Poor documentation
-	Not very useful error messages
-	Active support/development
-	Documentation?
-	May be sub-standard

## NEXT

-	React-like API framework
-	Supports Typescript
-	I18n support
-	Has a UI feature for server-side rendering
-	CSS

## KOA

-	Supports TypeScript
-	Can serve static files for server-side rendered stuffs
-	Built by the Express team
-	Largely eliminates the need for callback functions
-	Solid documentation

## Express

-	Ancient
-	Tried and true, very robust and mature
-	Stable core features, so very predictable
-	Prolific
-	Likely represents a significant amount of the global NODE knowledge
-	Docs, StackOverflow, etc
-	Barebones API package
-	Often included as a baseline in other, larger frameworks
-	Super flexible
-	Does it’s few things super, duper well
-	Can take extra work to set up, figure out it’s mix-ins, etc
-	Possible risk of pulling in a bad mixin
-	More configuration than convention
-	Loads of plugins, packages
-	Vanilla JS by default, supports TypeScript
-	NO support for web sockets out-of-the-box

## SocketIO

-	WebSockets!
-	Can be an entire API on its own using only websockets
-	More often paired with Express to add in WebSocket support
-	Rare to use only SocketIO except for specific use cases
-	Example use would be for a chat app or something with lots of streaming data

## HAPI

-	Walmart
-	Config driven
-	Can create a server on a specific IP
-	Manually generated endpoints
-	Static file support
-	Front-end agnostic
-	Excella has never used this

## Fastify

-	Meant to be an Express replacement, trying to be faster
-	Has NEST and NEXT implementations
