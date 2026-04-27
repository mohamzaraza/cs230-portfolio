# CS 230 Software Design Portfolio

## The Gaming Room - Draw It or Lose It Software Design Document

### Client Summary
The Gaming Room is a game development company that wanted to expand their 
Android-only game, Draw It or Lose It, into a web-based application accessible 
on multiple platforms including Windows, Mac, Linux, and mobile devices. The 
software I was asked to design was a distributed, server-side Java web application 
that could support multiple simultaneous game sessions, each with their own teams 
and players, while enforcing unique game and team names and maintaining a single 
shared game state across all users.

### What I Did Particularly Well
I think the platform evaluation section came out well. Breaking down each 
operating platform across server side, client side, and development tools gave 
a clear and organized picture of the tradeoffs involved. The recommendations 
section also ended up being thorough, covering architecture, storage, memory, 
distributed systems, and security in a way that directly connected back to the 
client's actual requirements.

### How the Design Document Helped When Developing Code
Working through the design document first made it easier to understand why 
certain design patterns were being used before writing any code. For example, 
understanding the singleton pattern in the design document made it much clearer 
why GameService was structured the way it was when I actually looked at the code. 
Having the requirements and constraints written out also made it easier to catch 
potential issues early rather than discovering them mid-development.

### What I Would Revise
If I could revise one part, I would go back and expand the Domain Model section 
with more detail about how the iterator pattern is used to enforce name uniqueness 
across games and teams. I described the UML diagram well but could have done more 
to explain the step-by-step logic of how the iterator searches existing records 
before allowing a new one to be created. That would make the document more useful 
for a developer picking up the code for the first time.

### Interpreting and Implementing User Needs
The Gaming Room's main needs were cross-platform accessibility, a single shared 
game state, and unique naming enforcement. I implemented these by recommending a 
browser-based approach so no platform-specific installation was needed, using the 
singleton pattern to guarantee one shared GameService instance, and using the 
iterator pattern to check for duplicate names before creating new records. 
Considering user needs is important because software that technically works but 
does not fit how users actually interact with it will not be adopted. Every design 
decision should trace back to a real requirement.

### Design Approach and Future Strategies
I approached the design by first understanding the client's requirements, then 
identifying the constraints those requirements created, and then selecting design 
patterns that addressed those constraints directly. In the future I would use the 
same approach of mapping requirements to constraints to patterns, but I would also 
try to involve more user story thinking earlier in the process to make sure the 
design stays grounded in real use cases rather than just technical correctness.
