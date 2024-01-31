# Lab 2 - Servers and SSH Keys

## Part 1 - Chat Server

`ChatServer.java`

```
{
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler{
    String line = "";   
    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            String[] message = parameters[0].split("=");
            String[] name = parameters[1].split("=");
            if(name[0].equals("user") && message[0].equals("s")) {
                String test = String.format("%s : %s", name[1], message[1]);
                line += test + "\n";
            }
            return line;
        }
        else {
            return line;
        }
    }
}
class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
}
```
![Image](lab2-ss1.png)
    *
![Image](lab2-ss2.png)
    * 

## Part 2 - `ls` of Chat Server

## Part 3 - Reflection

In lab 2 and 3, I learned how to remotely connect to servers.

