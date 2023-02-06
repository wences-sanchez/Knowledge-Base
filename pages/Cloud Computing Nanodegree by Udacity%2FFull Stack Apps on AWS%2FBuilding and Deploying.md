tags:: Udacity, Cloud Development
deck:: [[Cloud Development Nanodegree::Full Stack Apps on AWS]]

-
- ## 2.Organizing our Code & Working with Larger Systems
	- ![image.png](../assets/image_1675530476287_0.png)
	- In larger projects, we use:
	- In server.ts:
		- ```typescript
		  import { IndexRouter } from "./controllers/v0/index.router"
		  
		  //...
		  app.use("/api/v0/", IndexRouter);
		  ```
	- In controllers/v0/index.router.ts:
		- ```typescript
		  const router: Router = Router()
		  
		  router.use("/feed", FeedRouter);
		  ```
	- In controllers/v0/feed/routes/feed.router.ts:
		- ```TypeScript
		  const router: Router = Router()
		  
		  router.get("/", ) //...) ...;
		  // THIS IS NOT THE ROOT BUT THE SUB-FOLDER ROOT
		  ```
	- In the file controllers/v0/feed/routes/feed.router.ts, the root directory `router.get('/',...` is not the server root directory. The root in this case is based on where the server is entering from, which in this case, is `api/v0/feed/routes`.
	-