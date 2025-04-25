# ser321-assignment-2-upper-layers-of-the-osi-model-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/ser321-assignment-2-upper-layers-of-the-osi-model-solved/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;95830&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;SER321 Assignment 2  Upper Layers of the OSI-Model Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
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
            5/5 - (1 vote)    </div>
    </div>
<h1>Prerequisites</h1>
<ol>
<li>The assigned readings in module 2 on Canvas</li>
<li>Lecture videos from Canvas</li>
<li>Running and understanding the following examples from the GitHub repo (Network/SimpleGrabHttpURL, Network/SimpleGrabURL, Network/HTTP-JSON)</li>
<li>Setup of a second device (second computer, AWS EC2, Raspberry PI) – see Canvas for details</li>
<li>Videos, tutorials about Wireshark</li>
<li>Understanding about lower levels of Networking (module 1)</li>
</ol>
<strong>Learning outcomes of this assignment are:</strong>

<ol>
<li>Understanding the upper layer Network protocols</li>
<li>Understanding how to use the upper layer protocols, e.g. HTTP, SMTP, FTP</li>
<li>Compare the different traffic for different protocols when running a client/server application on two different systems</li>
<li>Understanding how to use the command line</li>
</ol>
<h1>1&nbsp;&nbsp;&nbsp;&nbsp; Understanding HTTP (20 points)</h1>
For this you will only need your web browser and Wireshark (Wireshark only for taking a look at things yourself). To understand GET HTTP requests a little better we want to do a couple of GET requests through an API. In this case, GitHub. The API basically works by nesting topics, so sometimes you need to do a base call to get data and you will use the result to do the next call, etc.

Do the following:

Go to the GitHub Api documentation <a href="https://docs.github.com/rest/reference/">page.</a> This will give you some information about the API. It might be overwhelming at first, that is ok. The interesting part here is you can make requests directly on your browser and not just from Java, JavaScript etc. For instance we use the <a href="https://docs.github.com/en/free-pro-team@latest/rest/reference/repos#list-repositories-for-a-user">List repositories for a user</a> API to get all the public repos from a specific user. In your browser use this URL:

https :// api . github .com/users/amehlhase316/repos

This should show you a JSON of all my public repos (you can of course use a different username if you like, my public profile is boring).

Next, we want to look at one specific repo, we will use the <a href="https://docs.github.com/en/free-pro-team@latest/rest/reference/repos#get-a-repository">Get a repository</a> API method for that, go to:

https :// api . github .com/repos/amehlhase316/memoranda

This will give us a JSON about the memoranda project where I am the owner (or another project you want to use of course).

Now, find and run another call that gets all the commits on the default branch for one of the repositories you chose. Any public repo that has some branches and some commits on their branches is fine.

<strong>Deliverable (5 points): </strong>Paste the url you used into your document and take a screenshot and add it to your document (the screenshot should show the call you made and the JSON result – if the JSON is too big, partially showing it is ok).

Do another call. In this call, add GET parameters to the call from above that specifies a specific branch (so not the default) and set the per_page limit to 50 (so that now 50 commits instead of just 30 are shown). Usually APIs limit the response size and will return one page and you can call the next one if you need more data or you increase the page limit as we do here for simplicity. If you are stuck on this, go to the documentation and try to understand how to do it.

<strong>Deliverable (5 points): </strong>Paste the url you used into your document and take a screenshot of your browser and add it to the document.

<strong>Deliverable: Answer the following in your document (10 points):</strong>

<ol>
<li>Explain the specific API calls you used.</li>
<li>Explain the difference between stateless and a stateful communication.</li>
</ol>
Now you should take a look at Wireshark and check the communication that was going on with your calls. You do not have to document anything for me but I advise you to take a detailed look and do your best to understand all the traffic you generated.

<h1>2&nbsp;&nbsp;&nbsp;&nbsp; Setup your second system and run Server on it (65 points)</h1>
For this part you will need to setup your second machine (which you should have already done). See <a href="https://canvas.asu.edu/courses/66080/pages/setup-for-the-course?module_item_id=4034383">setup Page on Canvas.</a> We will call your local machine “first machine” and your second one (AWS, PI, extra computer) “second machine” in this document.

<h2>2.1&nbsp;&nbsp;&nbsp;&nbsp; Getting the sample code onto your systems (should be done already)</h2>
This is something that should be done already but in case you did not do this yet. So now that you have your second machine setup you should make sure the <a href="https://github.com/amehlhase316/ser321examples">GitHub repo </a><a href="https://github.com/amehlhase316/ser321examples">w</a>ith all of the examples is available on that second machine and first machine. I would advise you to fork the given repository and then clone that repo on all the machines you want to work on, so you can make changes and still commit, push and pull. This fork will be public, thus it is not for your assignment changes but just for “playing” with the examples.

You can of course also download the zip and add it to both systems (but then you won’t be able to pull updates easily). If you have not worked with GitHub before I advise you to go to the <a href="https://canvas.asu.edu/courses/66080/pages/review-git-slash-github?module_item_id=4284036">GitHub review page</a> on Canvas.

<h2>2.2&nbsp;&nbsp;&nbsp;&nbsp; Running a simple Java WebServer (10 points)</h2>
You now need to work with the <em>Socket/WebServer/</em>. Copy this folder into YOUR assignment 2 folder of your private repo before you make any major changes.

We want to run the <em>FunWebServer </em>task from Gradle in this example.

The Server should run on your second machine (AWS). You should also start Wireshark on your first machine again if it does not run anymore.

When your Server runs on your second machine go to a Web Browser on your first machine and go to: <em>ipOfSecondMachine:9000 </em>(you can also change the port if you like of course, the port you use must be opened up for TCP traffic on AWS). If everything works as intended this should bring up a web page.

<strong>Delivearble: 10 points: </strong>Take a screen shot of your web browser showing the <em>ipOfSecondMachine:9000 </em>and the web page. You should take a screen shot of your second machine (can be two separate screen shots or just one) and add it to your document under Task 2. The screen shot should look something like this:

<h2>2.3&nbsp;&nbsp;&nbsp;&nbsp; Analyze what happens (10 points)</h2>
Wireshark should still be running in the background. Go to Wireshark and create a filter so that it shows your Network traffic to and from your WebServer. Take a screenshot of your Wireshark capture and add it to your document.

<strong>Delivearble: Now in your document answer the following (1-2 points each):</strong>

<ol>
<li>What filter did you use? Explain why you chose that filter.</li>
<li>What happens when you are on /random and click the “Random” button compared to the browser refresh (you can also use the command line output that the WebServer generates to answer this)?</li>
<li>What kinds of response codes are you able to get through different requests to your server?</li>
<li>Explain the response codes you get and why you get them.</li>
<li>When you do a <em>ipOfSecondMachine:9000 </em>take a look what Wireshark generates as a server response. Are you able to find the data that the server sends back to you?</li>
<li>Based on the above question explain why HTTPs is now more common than HTTP.</li>
<li>What port does the server listen to for HTTP requests in our case and is that the most common port for HTTP?</li>
<li>What local port is used when sending different requests to the WebServer? How does it differ to the traffic to your SMTP server from part 1?</li>
</ol>
<h2>2.4&nbsp;&nbsp;&nbsp;&nbsp; Setting up a “real” Web server (10 points)</h2>
Stop your Java Web server and do the following while on your second machine (it might need to be apt-get depending on your system setup).

Lets setup nginx so you have a real Web server running: Run the following:

<table width="567">
<tbody>
<tr>
<td width="436">sudo amazon−linux−extras install nginx1 −−&gt; when prompted , sudo nginx −−&gt; to start the web server</td>
<td width="131">type y</td>
</tr>
</tbody>
</table>
Then change the config file for the server. Note: All changes will be in the server&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; …

section. (On the Pi the config file looked different sometimes, just a warning).

sudo vim /etc/nginx/nginx . conf

You need to enter the server_name and a location block into your config file. It should look something like this (with the correct ip from your host and port you used in the Java file) – this is only a snippet but shows the part that you need to change.

<table width="567">
<tbody>
<tr>
<td width="533">. . . .

server {

server_name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 18.223.100.162;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #CHANGE IP HERE

root&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; /usr/share/nginx/html ;

location / {&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #Add location&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; block with

proxy_pass http :// localhost :9000/; }

# Load configuration f i l e s for the default server block . include /etc/nginx/ default .d/∗. conf ;

# redirect&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; server&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; error&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; pages to the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; static&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; page /40x . html

#

error_page 404 /404.html ; location = /40x . html {

} . . . .
</td>
<td width="34"></td>
</tr>
</tbody>
</table>
correct&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; port

Now reload nginx with the configuration updates by using:

Your web server is running and your port 80 traffic will be re-directed to the port you specified in <em>location block </em>above.

Start your Java funWebServer again.

Make sure Wireshark is running again. Now go to your browswer again. The url you need to use should change slightly now with the real webserver. Make sure that it is different and that you understand why.

<strong>Delivearble: Now in your document answer the following:</strong>

<ol>
<li>What is the URL that you can use now to reach the main page?</li>
<li>Check your traffic to your Webserver. What port is the traffic going to now? Is it the same as previously used or is it and should it be different?</li>
<li>Is it still HTTP or is it now HTTPs? Why?</li>
<li>Take a screen shot of your Web browser, your second machine and also showing the port on Wireshark, similar to the screen shot you took before (but also with Wireshark) and add it to your document for this task. If we do not see that you can now get to the webserver with the “different URL” we will not see that you actually setup the server correctly so make sure that shows up if you want points for this task.</li>
</ol>
If you like you can stop your nginx again:

Should bring you back to the stage you had without your nginx WebServer.

<h2>2.5&nbsp;&nbsp;&nbsp;&nbsp; Brownie points/Extra Credit (5 points extra) – just this one section: Setting up HTTPs</h2>
This did not work on every instance for some reason, thus extra credit if you can make it work.

Only attempt if you are ready for some extra steps and some research!! You can think about creating a copy of the current nginx config file in case you want to go back and this would make things easier later on. Start your nginx again

Now, to make our traffic secure we want our communication to go through HTTPs. This will need some more work and some additional steps but worth it to understand what is actually going on.

Work on your second machine for this.

Get a Domain, here we use DuckDNS – you can use something else if you like. In the end we just get a Domain Name which will get resolved to your IP address (remember DNS from the lecture):

In a Broswer visit DuckDNS (your main machine), then

<ol>
<li>login with whatever method you prefer</li>
<li>enter a sub domain –&gt; click “add domain” 3. select “install” from the top navigation bar</li>
<li>Duck DNS/Install:</li>
</ol>
<ul>
<li>Choose “linux cron”</li>
<li>Select the domain you created</li>
<li>Go to your second maching &amp; follow the linux cron instructions Note: When saving the crontab, use (esc –&gt; :wq! –&gt; Enter) instead of the instruction’s (CTRL+o –&gt; CTRL+x).</li>
</ul>
Your Domain is setup, now we can continue with the certificate setup. On your second machine run the command to change your nginx config info:

sudo vim /etc/nginx/nginx . conf

Change the server name from the IP you had to your newly created DuckDNS domain name. E.g., ser321.duckdns.org. Save the changes and reload nginx. When you go to DuckDNS.org now you should see your domain name listed and it should now show the IP from your second machine as the IP address. So your domain “perfectname.duckdns.org” gets resolved to your machines IP address.

Now, you should already be able to use <em>yourdomain.duckdns.org </em>to reach your server (still as HTTP and of course after starting your Java program again). Stop the Java program before continuing.

We need to setup a certificate, we can use <a href="https://certbot.eff.org/instructions">Certbot. </a>Run

sudo yum install −y certbot python2−certbot−nginx sudo certbot

Press 2 for nginx. This should bring you to some setup questions.

Lets finish setting up the certificate, run:

sudo /usr/ local /bin/certbot −−nginx −−debug

When prompted –&gt; type y

When prompted –&gt; enter an email address

When prompted –&gt; type a to agree

When prompted –&gt; type n to decline emails

When prompted –&gt; type the number associated with your domain (it is listed above this prompt)

When prompted –&gt; type 2 to configure a redirect

Your certificate should be all setup.

Now, you should be able to go to <em>perfectname.duckdns.org </em>and get to your website through HTTPs. Check on Wireshark and on the Browser you should see that your traffic is going through HTTPs now.

Take a screen shot of your Web browser, your second machine and also showing the port on Wireshark, similar to the screen shot you took before (but also with Wireshark) and add it to your document. We need to see that it now shows HTTPS in your broswer to receive the extra credit points.

<strong>Delivearble: Now in your document answer the following:</strong>

<ol>
<li>What port is your traffic going through now?</li>
<li>Can you still find the plain text responses as before with HTTP?</li>
</ol>
If you want to stop the nginx just call

Your domain should not work anymore and you should only be able to use the ip address to access your Java server again.

OPTIONAL, in case you want to remove the certificate (which you can do but when nginx is stopped you will only have the “normal traffic” again anyway).

Removing the certificate so only the nginx WebServer works, step one is to remove the certificate, step two to update the nginx config, which is easy if you copied the file back before you started with HTTPS and you can just replace it now. If you did not copy it then open it and remove everything related to the certificate and the port 443. Also if you do not want to use the Domain anymore the server name do:

/usr/ local /bin/certbot−auto revoke −−cert−name YOUR_DOMAIN sudo vim /etc/nginx/nginx . conf

DONE.

This ends the “Brownie points/Extra Credit” section and the rest are normal points.

<h2>2.6&nbsp;&nbsp;&nbsp;&nbsp; Some programming on your WebServer (50 points)</h2>
This should be done no matter if you have nginx running or not! Working without certificate might be better so you can read the traffic on Wireshark if you need to. I advise you to spend some time on the Webserver code and play around so you understand what happens and how things work.

In the WebServer code you will see a couple todos, which are the things you need to implement and some further details will be explained here. These are the changes that you need to implement on your private repo not the example repo. You can definitely use a JSON library, look at the JSON examples in the repo mentioned at the beginning of the document how to include a JSON library into your Java and Gradle files.

<h3>2.6.1&nbsp;&nbsp;&nbsp;&nbsp; Multiply (8 points)</h3>
Check out the <em>if </em>for the <em>multiply </em>case. This is a normal GET request that gets two parameters. Your task is now to add some error handling into it in case the user does not provide the correct inputs, or just one input etc. You can handle it as you see fit, e.g. set default values, just print a message but your server should not crash and it should respond in a good way (true for the whole assignment, DO NOT have your server crash).

Important is that you create an appropriate header response with a good error code for that case. You can find explanations about error codes <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Status">here:</a> <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Status">https://developer.mozilla.org/en</a><a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Status">US/docs/Web/HTTP/Status.</a>

Explain in your document what you decided to do and which error code you decided to use and why. DO NOT just catch any error and send out just one error message. The error message should be specific to the error you caught.

Example protocol, you can change the responses to what you want to send back and you should add on to the status codes.

<h3>multiply request</h3>
<strong>request </strong>host :PORT/multiply?num1=1&amp;num2=2 Path:

Body Parameter (you can make the parameters optional as well and use default values if they are not provided):

num1 ( int ) − required num2 ( int ) − required

<strong>response</strong>

This is just an example and not complete, since the error handling will be your job! OK Response (200) – Example

HTTP response status codes

200 −− OK, multiply happened correctly xxx −− Error1 xxx −− Error2

<h3>2.6.2&nbsp;&nbsp;&nbsp;&nbsp; GitHub (10 points)</h3>
You see another <em>if </em>statement waiting for <em>github</em>?. In there you see a fetch that will pull information from GitHub. This part is about parsing a JSON response and understanding this response.

Implement your webserver so that when calling

<em>host </em>: <em>PORT/github</em>?<em>query </em>= <em>users/amehlhase</em>316<em>/repos </em>you should get a response with all my public repos (not a lot). You should parse that JSON in your code and respond with some data. The data you should return is the full_name of the repos, the ids of the repos, login of the owner of each repo. Go by what this assignment wants displayed, the given code in the example repo says something else.

The webpage should display this information in some way (does not have to be pretty). Make sure you include good error handling and that we cannot crash your server with wrong request (which we will try). You should include good error codes, so not just one big try and catch!

Example protocol, you can change the responses to what you want to send back and you should add on to the status codes.

<h3>github request</h3>
<strong>request </strong>host :PORT/github?query=users/amehlhase316/repos Path:

Body Parameter:

<table width="567">
<tbody>
<tr>
<td width="267">query ( String ) − required // This Parameter is the one that</td>
<td width="36">will</td>
<td width="119">be given to the</td>
<td width="145">real GitHub API</td>
</tr>
</tbody>
</table>
<strong>response </strong>This is just an example and not complete, since the error handling will be your job!

OK Response (200)

Example (you can of course format this differently to send back to the HTML page)

<table width="567">
<tbody>
<tr>
<td width="112">[

{” fullname “:
</td>
<td width="455">“repoName” ,</td>
</tr>
<tr>
<td width="112">” id “: 1 , ” loginname “:</td>
<td width="455">“ownerName”</td>
</tr>
<tr>
<td width="112">} ,

{” fullname “:
</td>
<td width="455">“repoName2” ,</td>
</tr>
<tr>
<td width="112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ” id “:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2 ,

” loginname “:

}

]
</td>
<td width="455">“ownerName2”</td>
</tr>
</tbody>
</table>
HTTP response status codes 200 – OK, the data could be fetched xxx – Error1 xxx – Error2

<h3>2.6.3&nbsp;&nbsp;&nbsp;&nbsp; Make your own requests (15 points – 7.5 for each request)</h3>
In your webserver add two more request types that the webserver can handle. This should be similar to the multiply or github request. You can do any request you like but they should fulfill the following requirements:

<ol>
<li>the request should be a bit more than just a new version of the multiply (e.g. do not just do an add/subtract/divide)</li>
<li>the two requests you come up with should not be almost the same thing</li>
<li>the request should get at least two argument and use these arguments for something</li>
<li>the request should have proper error handling, we should not be able to crash your server with wrong input or wrong calls and the error message should be appropriate (good error codes)</li>
<li>You should explain your request on the main page that opens when going to your server and give an example how we can use your request, provide the exact url with example data that we can just copy and paste</li>
</ol>
<h3>2.6.4&nbsp;&nbsp;&nbsp;&nbsp; Explain the protocol you designed for your requests (10 points – 5 for each request)</h3>
For the requests you created in 2.6.3, you should have come up with some kind of protocol how the request is called and what it returns and which error codes it returns. Write down this protocol and explain it in detail, you can write it in a similar way as I did above.

<h3>2.6.5&nbsp;&nbsp;&nbsp;&nbsp; Webserver for everyone (5 points)</h3>
Now, figure out how you can keep your webserver running even when closing the terminal window to AWS. Then post the link to your server with your public IP address and port to Slack #servers.

<h3>2.6.6&nbsp;&nbsp;&nbsp;&nbsp; Test other webservers (2 points)</h3>
Test 2 other servers that are provided in the #servers channel and make a valuable comment on each one you test (you can do this up to 2 days after the due date). No valuable comment, no points.

<h1>3&nbsp;&nbsp;&nbsp;&nbsp; Submission</h1>
Submit your link to your GitHub repo Assignment2 folder on Canvas.

Throw your PDF <em>UpperLayers_asurite.pdf </em>with all your answers, explanations, and screenshort into your Assignment 2 folder. No Wireshark captures needed.

Now, add the webserver directory into the Assignment2 folder as well. Call the directory “Webserver” and it should have all necessary files in that folder for us to run your code and to see your implementation. You should leave the port at 9000. We will run the code through going to your Webserver directory and call <em>gradle FunWebServer</em>. If this does not work you will not receive points for the server!!! So things should look as follows:

<ul>
<li>Assignment2</li>
<li>UpperLayers\_asurite.pdf</li>
<li>/Webserver</li>
<li>/src</li>
<li>/www</li>
<li>gradle</li>
<li>md</li>
</ul>
Zip this whole Assigment 2 folder and put it on Canvas as well!
