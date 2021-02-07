---
title: "Markdown Practice"
date: 2021-02-07T18:47:51+01:00
draft: false
image: "images/cover1.jpg"
tags: ["projects"]
---

# My first headline

Here is the first paragraph of my first post as a practice. Here I can do some formatting:
 - `Like monospaced`
 - Or _italic_ / *italic* 
 - Or __more emphasised__
 - Or combined **here is something, and here _something other_**
 - And I can show how I correct ~~tyopw~~ typos.

## Using other levels of structure

Here is the example how I can use more levels to structure my ideas in a topic.

For a step-by-step tutorial it's best to use a numbered list:

1. Decide what to talk about.
2. Make a draft of the main ideas.
    1. The overal statement/function of the content.
    2. What's neccessary before we begin?
    3. What are the steps to execute?
    4. What are the expected results?
3. Content structured this way remains concise and clear.
4. Create sections for each step for building a task, a Task contains all the substeps needed, as subsections:
    - Use headers,
    - Horizontal rules,
    - And other formatting to differentiate, or structure the content.

## Using code examples

For APIs it is vital to provide besides the conceptual explanation, proper code examples.

This example shows the content in this source file: [GitHub](https://github.com/ddyfedd/stoplight_api_tutorial/blob/main/reference/openweathermap.v1.yaml)

When you use a tool like [Swagger.io](https://editor.swagger.io/) to edit your OpenAPI reference file, link above, you can run test codes in the connected OpenWeatherMap API endpoint (in this case on the `weather` endpoint).[^1]

[^1]: This requires that you have your own API key for using OpenWeatherMap API, you can get your key at: <https://home.openweathermap.org/users/sign_up>. After registering you can access your API key for authorizing your requests.

### Create a code sample

There are several ways to get a code snipet for your documentation, here are the steps using an OpenAPI specification written in YAML combined with Swagger[^2]:

[^2]: This example is made by writing the linked YAML content in Swagger's text editor. You can use other tools for this purpose, like [Postman](https://www.postman.com/)

1. Click on the __[Authorization]__ button.
2. Enter your API key on the Authorization panel, then press __[Login]__. Now you can run requests with the parameters.
3. Click the `GET /wheather` endpoint to expand:
    1. Press the __[Try it out!]__ button!
    2. Set up your parameters as you wish! **_Note:_** You have to set at least the `id` parameter.
    3. After you are set up, press the **[Execute]** button!
4. The response is shown below, you get:
    - A cURL link, you can run in your command prompt:
        ```sh
        curl -X GET "https://api.openweathermap.org/data/2.5/weather?id=2172797&units=metric&lang=en&mode=json&appid={API-key}" -H  "accept: application/json"
        ```
    - A basic request URL:
        ```http
        https://api.openweathermap.org/data/2.5/weather?id=2172797&units=metric&lang=en&mode=json&appid={API-key}
        ```
    - And the response of the API, in the choosen format (default: `json`):
        ```json
        {
            "coord": {
                "lon": 145.7667,
                "lat": -16.9167
            },
            "weather": [
                {
                "id": 804,
                "main": "Clouds",
                "description": "overcast clouds",
                "icon": "04n"
                }
            ],
            "base": "stations",
            "main": {
                "temp": 25.55,
                "feels_like": 30.95,
                "temp_min": 25,
                "temp_max": 26.11,
                "pressure": 1004,
                "humidity": 94
            },
            "visibility": 5000,
            "wind": {
                "speed": 1.03,
                "deg": 290
            },
            "clouds": {
                "all": 90
            },
            "dt": 1612550301,
            "sys": {
                "type": 1,
                "id": 9490,
                "country": "AU",
                "sunrise": 1612555668,
                "sunset": 1612601653
            },
            "timezone": 36000,
            "id": 2172797,
            "name": "Cairns",
            "cod": 200
        }
        ```



