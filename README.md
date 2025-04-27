# comp3310-engn3539-etc-assignment-3---testing-mqtt-p0-solved
**TO GET THIS SOLUTION VISIT:** [COMP3310/ENGN3539/etc Assignment 3 – Testing MQTT P0 Solved](https://www.ankitcodinghub.com/product/comp3310-engn3539-etc-assignment-3-testing-mqtt-p0-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124399&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP3310\/ENGN3539\/etc Assignment 3 – Testing MQTT P0 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Introduction:

Assignment 3

MQTT is the most common open IoT protocol being deployed today. It uses a publisher/subscriber model, allowing for an almost-unbounded number of sources to publish information, each at their own rate, and subscribers to receive information as desired. As such, it is designed to provide high-performance communication mechanisms, with minimal delays and excellent scaling performance. We’ll use it to monitor the performance of some imaginary system: say counting the total kilograms of minerals rushing by on a conveyor belt, that you can control. This assignment will look at the functionality and performance of the publishers, brokers, the network (potentially) and subscribers.

helper librariesAssignment Project Exam Help. The assessment will not rely solely on running on your code, but more on the data gathering

You will be submitting two things: your code and your analysis report. Note that there will be two submission links on the Wattle course-site:

compile/run the components as appropriate.

Outcomes

We’re assessing your understanding of MQTT, as well as your code’s functionality in subscribing/publishing to a broker, dealing with high message rates from a number of sources, measuring message performance and statistics of a networked application, and your insight to interpret what you’re seeing. You will be exploring MQTT functionality, the quality-of-service (QoS) levels, describing how they work, why you would use different levels, and how they perform in real-world deployments given various publishers.

Resources

You will need to set up your own MQTT server/broker for you to connect to as per the specifications below, on your own computer, or it’s even better if you have a separate computer to use for the broker and publishers. There are a number of free brokers to choose from, https://mqtt.org/software/ has a good list.

You can test your broker works by subscribing to the $SYS topics, which describe the server, and it will help get you familiar with the information presented there – you will be using them for your analysis later.

Assignment programming:

You need to write two programs.

• A Publisher: o A Publisher will first subscribe (listen) to a set of ‘request’ topics, namely request/qos, request/delay and request/instancecount. When it sees new values for these, it will start publishing accordingly.

o You will have 5 instances of a Publisher running at the same time, called pub-1 to pub-5. These will help stress the broker (and network, if you have separate computers). The ‘instancecount’ will tell you how many publishers should be active, while the rest should keep quiet.

o Each Publisher will send a sequence of simple message to the broker, namely an incrementing counter (0, 1, 2, 3, …). It will publish those messages to the broker at a requested MQTT QoS level (0, 1 or 2), and with a requested delay between messages (0ms, 1ms, 2ms, 4ms) for 60 seconds.

o Each Publisher will publish to the topic counter/&lt;instance&gt;/&lt;qos&gt;/&lt;delay&gt;, so e.g. counter/1/0/4 is the messages coming from Publisher-instance-1 at qos=0 and delay=4.

o After it has finished its 60sec burst of messages, each Publisher should go back to listening to the ‘request’ topics for the next round of instructions.

o At 0ms delay and qos=0 your publisher should be able to publish very quickly, potentially many thousands of messages per second.

• An Analyser: Who controls your Publishers? Your Analyser. o Your Analyser will start by publishing to the request/qos, request/delay and request/instancecount topics, asking for some number of Publishers to deliver accordingly. o It will then listen to the specified counter topic(s) on the broker and take measurements (below) to report statistics on the performance of the Assignment Project Exam Helppublisher/broker/network combination.

o The measurements should be taken across the range of delay (4), QoS (3), and instance-count (5) values as above, so that you can compare them; things can get weird under load.

reconnect when changing the subscription QoS.

o Yes, thats 3*3*4*5=180 tests, each taking 1min. Fortunately your code could do it all for you.

Once your code is working, you need to tackle the following:

1. Start the Publishers, then run your Analyser. Have the Analyser tell the broker what you want the Publisher(s) to send, and record data for 60sec as below.

Tips: (i) only print to screen for debugging, not while measuring, otherwise it will slow your code down a lot and mess up your data. (ii) Use the counter values to tell you what messages are arriving, or are not arriving, to calculate the rates below.

a. Collect statistics, for each instance-count/delay/QoS combination, to measure over the 60sec period:

i. The total average rate of messages you actually receive from all publishers across the period [messages/second].

ii. The rate of message loss you see [percentage].

(how many messages did you see, versus how many should you have seen)

iii. The rate of any out-of-order messages you see [percentage]

(i.e. how often do you get a smaller number after a larger number)

iv. The median inter-message-gap you see, compared to the requested delay [milliseconds]. Only measure for actually consecutive counter-value messages, ignore the gap if you miss any messages in between.

b. While measuring the above also

i. Subscribe to and record the $SYS/# measurements, and identify what, if anything, on the broker do any loss/misordered-rates correlate with. (Look at measurements under e.g.

‘load’, ‘heap’, ‘active clients’, ‘messages’; anything that seems relevant. See e.g.

https://mosquitto.org/man/mosquitto-8.html for ideas. Be aware of the timing of the $SYS measurements, to reflect when you actually put the broker under load)

2. In your report: [around 4-5 pages of text for all of Q2 and Q3, plus any charts]

a. Subscribe to some broker to retrieve some $SYS/# value. Wireshark the handshake for one example of each of the differing QoS-levels (0,1,2), include screenshots in your report that show the wireshark capture of a pub/sub (filter for mqtt), and briefly explain how each QoS-level transfer works, and what it implies for message duplication and message order. Discuss briefly in your report in which circumstances would you choose each QoS level. [around 0.5 page of text]

b. Summarise your measurements, in suitable table form, and simple charts, to compare the impact of different delays and QoS combinations. Explain what you expected to see, especially in relation to the different QoS levels, and whether your expectations were matched.

c. Describe what correlations of measured rates with $SYS topics you expect to see and why, and whether you do, or do not.

3. Consider the broader end-to-end (internet-wide maybe) network environment, in a situation with millions of sensors publishing to thousands of subscribers. Explain in your report [around 1 page]

a. WAssignment Project Exam Helphat performance challenges there might be when using MQTT in general for high volumes of

messages, from the sources publishing their messages, all the way through the network and broker to your subscribing client application. If you lose messages, where might they be lost, and why? Think about links, routers, memory/buffers, cpus, etc.

Bonus questions:

1. What happens if the Analyser modifies the request topics at the same time the Publisher sees the changed values – how could you ensure it doesn’t start prematurely? Does your code do this?

2. How does it run with 10, or more, publishers with qos=0, delay=0ms? This will be subject to your computer’s performance.

3. Try to run this on a public broker, across the internet. What happens to the performance and stability of the results? Don’t repeat all 180 tests, just try the 0ms-delay ones, as much as they let you.

Assessment

• Your code clarity, and documentation/comments (15%). o Could somebody else pick this up, debug it or add features? Do you explain your approach and choices you made?

• Your code subscribing, properly publishing/listening to the broker, and collecting data (15%). o Do your Analyser and Publisher work efficiently and as specified? Can your publishers publish messages at a high rate when the delay=0ms? Can the Analyser run a number of tests with limited human input?
