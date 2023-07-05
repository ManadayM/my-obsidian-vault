---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1590328890650-1c94261ff33e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4OTIzMzcx&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-27) | (time:: 17:32) | (weather:: Vadodara: 🌦   +30°C ↗17km/h)

# Clean Architecture
![[Clean Architecture 2022-08-08 15.05.46.excalidraw|100%]]
It is an architecture model that was developed by [[Bob Martin]]. 

## The Four Circles
There are 4 core circles in Clean Architecture.

### Entities
- Primary concepts of your business.
- **Entities have no imports or requires.** Use [[Dependency Injection]] for the dependencies.
- For example, an application for an insurance company might have an entity like a `Claim`. For a product sales application, it would have entities like `Customer`, `Product`, `Order`, etc.

### Use Cases
- Interactions b/w entities.
- For example
	- **Insurance App**: `Filing a claim`.
	- **Sales App**: `Customer places an order`.
	- **Social Media App**: `User posts a tweet`.

### Adapters
To isolate our various use cases from the tools that we use like Frameworks and Drivers from the outermost circle.

### Frameworks & Drivers
All about frameworks and drivers that we use to build our applications like Express.js as Framework, MongoDB driver for Node.js as a driver, etc.

## The Arrows
- You'll notice arrows from the outermost circle to the innermost circle in a uni-direction.
- These **arrows signify the flow of dependency**. An outer circle can depend on the inner circle but **the inner circle cannot depend on the outer circle**.
- This rule is the magic of Clean Architecture. It implies that if the flow of the dependencies goes from **outside → inside** then changes are going to be propagated from **inside → outside**.
- If something changes in a framework or driver. Since there's nothing depending on a framework or driver the changes are isolated to that circle.
- **Most likely to change:** Put them on the outer circles.
- **Most likely to remain the same:** Put them into the innermost circles.

## Inject dependencies, not import
> [!NOTE] Avoid **inside → outside** dependency
> Check this important explanation https://youtu.be/CnailTcJV_U?t=603 by Dev Mastery.

Use **[[Dependency Injection]]** to avoid having inverted dependencies i.e. inside layer is dependent on the outside layer.

> [!INFO] Clean Architecture in action
> https://github.com/dev-mastery/comments-api


### 📚 Readings & References
- https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html
- https://dev.to/rubemfsv/clean-architecture-the-concept-behind-the-code-52do
- https://dev.to/rubemfsv/clean-architecture-applying-with-react-40h6


---
#### Internal Links
[[2022-07-27]], [[Software Engineering]] 