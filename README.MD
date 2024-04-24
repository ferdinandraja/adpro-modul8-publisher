## How many data your publlsher program will send to the message broker in one run?
The publisher will send exactly 5 data to message broker in one run. The reason is because there are 5 `publish_event` in `main` and each `publish_event` sends one `UserCreatedEventMessage` to message broker.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
It means that both publisher and subscriber communicate in the same message broker. The message that publisher sends will be received by the subscriber.

## Running RabbitMQ as message broker.
<img src="img/ss1.png">

## Sending and processing event.
<img src="img/ss2.png">
When we use the RabbitMQ, if we run the subscribern and then run th epublisher, the publisher will send a message to RabbitMQ, and the subscriber will receive the message, just like what happen in the picture.

## Sending and processing event.
<img src="img/ss4.png">
After running the publisher for some tries, I found a  relation between the spikes and the publisher. From what I understand, the spikes will go up everytime I run the publisher. That means that the spike can indicate the message rates.
