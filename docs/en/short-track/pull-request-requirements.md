# Pull Request Requirements (PR)

Pull Request is a place to discuss contributor's code. It should not be a monologue but rather a fruitful collaboration between a contributor and a reviewer. Stay professional, respect each other's time and efforts.

## Pull Request description must contain the following

1. Task URL.
2. Screenshot showing the result of Task's completion. The screenshot is added to a Pull Request as an image attachment. To achieve that you can just drag-and-drop the screenshot to the Description text area.
3. Deployment URL of your application. For frontend - Website URL, for backend - API Endpoint URL. To create deployment you can use the following:
   - gh-pages (if you have access to a private RS School repo)
   - web hosting, like [netlify.com](https://app.netlify.com/drop) (if you don't have access to a private RS School repo or can't deploy to `gh-pages` because of permissions)
   - other static assets storage with web serving capabilities, like [S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
   - serverless or self-hosted solutions for your API (make sure URL is public and accessible by other people)
   - naming scheme: GitHub account name - Task name.
4. Submittion Date / Deadline Date.
5. Your self-check of Task's completion result and opinion on the achieved Score.

### Description Example

```
1. Task: https://github.com/rolling-scopes-school/tasks/blob/master/tasks/fancy-weather.md
2. Screenshot:
   ![](https://docs.rs.school/images/fancy-weather.png)
3. Deployment: https://chakapega-fancy-weather.netlify.com/
4. Done 28.05.2020 / deadline 31.05.2020
5. Score: 220 / 300
- Markup, design, UI (15/30)
  - [x] minimum page width at which it is displayed correctly – 320 рх (10)
  - [±] application's appearancecorresponds to the layout and/or its improved version (5/10)
  - [ ] aaplication works and looks correctly with any language (0)
- Section "Today's weather" displays the following data (15/20)
  - [x] use weather data and location (10)
  - [±] clock, refreshed each second (5/10)
 ...
```

## Pull Request must not contain the following

- Commented code
- Leftover and/or irrelevant files, auto-generated code, node_modules, etc.
