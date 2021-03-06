## Spring Boot Websocket + React: user notifications with web socket ##

This example will shows how to send notifications, via web socket, to specific logged-in users (definded by access_token).

Could be useful, for example, if you are trying to implement a real-time user notification system with ReactJS.

[*DEMO*:](https://giphy.com/gifs/3o6fIRpgI9LnZ3jrXi/fullscreen)

![Demo](https://media.giphy.com/media/3ohs7JcKo7aeM2PHdC/giphy.gif)


### Build and run

#### Configurations
Backend:

Open the `application.properties` file in *websocket-spring* and set your own database (in my case I'm using MongoDB). You can change User collect to Entity and repository like your project.

#### Prerequisites

- Java 8
- Maven > 3.0

#### From terminal
1. Start mongodb database
    ```
    $ mongod
    ```
2. Go on the project's *websocket-spring* folder, then type:
    ```
    $ mvn spring-boot:run
    ```
    Or, just open Maven project on IDE like IntelliJ IDEA and run `main method` in Application class
3. Go on project:s *websocket-react* folder, then type:
    ```
    $ npm install
    $ npm start
    ```
    or
    ```
    $ yarn install
    $ yarn start
    ```
### Usage

- Launch the application and login into it with one of the following credentials (Username / Password):
    * user1 / user1
    * user2 / user2

- Keep a window open on the index and login by user1
- Open a new private/incognito windows of your web browser and login with *user2*
- From this web browser specify *target user* and click the button to send a fake action: **target user** will be notified.

### Reference
Special thanks to **azanelli** for your great [example](https://github.com/netgloo/spring-boot-samples/tree/master/spring-boot-web-socket-user-notifications)