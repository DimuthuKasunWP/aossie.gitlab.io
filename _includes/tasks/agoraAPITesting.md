#### Rest API testing for Agora-web


- **Description:**

Let's create API endpoint testing for Agora-web.

Use 
https://www.playframework.com/documentation/2.6.x/ScalaFunctionalTestingWithScalaTest#Testing-with-a-server 
to write tests for APIs.

class PostServerSpec extends PlaySpec with GuiceOneServerPerSuite {
  
  "test server logic" in {
    val wsClient = app.injector.instanceOf[WSClient]
    val server =  s"localhost:$port"
    val testURL = s"http://$server/v1/posts"
    val response = await(wsClient.url(testURL).get())
    val json = response.json
    val elem0 = (json)(0)
    
    response.status mustBe OK
    response.header("Content-Type") mustBe Some("application/json")

    (elem0 \ "id").as[String] mustBe "1"
    (elem0 \ "title").as[String] mustBe "title 1"
    (elem0 \ "link").as[String] mustBe "/v1/posts/1"
    (elem0 \ "body").as[String] mustBe "blog post 1"    
  }
}

Update the Documetation

- **Tags:** Scala, Scala test, REST API

- **Categories:** Outreach/Research, Quality Assurance, Coding
