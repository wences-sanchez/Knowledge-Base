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
		  ```