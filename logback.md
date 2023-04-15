<pre><code>&lt;configuration&gt;
    &lt;variable name="LOG_PATH" value="D:\logs"&gt;fileName.log&lt;/variable&gt;
    &lt;appender name = "STDOUT" class="ch.qos.logback.core.ConsoleAppender"&gt;
        &lt;encoder&gt;
            &lt;pattern&gt;%d{HH:mm:ss.SSS} [%thread] %-5level %logger{36} -%kvp- %msg%n&lt;/pattern&gt;
       &lt;/encoder&gt; 
    &lt;/appender&gt;
    
     &lt;appender name = "FILE" class="ch.qos.logback.core.FileAppender"&gt;
        &lt;file&gt;${LOG_PATH}\myapp.log&lt;/file&gt;
        &lt;encoder&gt;
            &lt;pattern&gt;%d{HH:mm:ss.SSS} [%thread] %-5level %logger{36} -%kvp- %msg%n&lt;/pattern&gt;
       &lt;/encoder&gt; 
    &lt;/appender&gt;
&lt;/configuration&gt;
</code></pre>


| Tag  | Operation |
| ------------- | ------------- |
| <pre><code>&lt;configuration&gt; &lt;/configuration&gt;</code></pre> |  A configuration tag is typically used to define a set of parameters or settings that are used to configure a system, application, or software component. The configuration tag is typically nested within the root element of an XML document and contains one or more child elements that define specific configuration settings |
| <pre><code>&lt;appender&gt; &lt;/appender&gt;</code></pre> | In XML, an appender is used to define how log messages are handled in a logging framework. An appender specifies the target destination where log messages should be output, such as a file, console, or network socket, and also includes options for formatting and filtering log messages. </br> An appender in XML typically has the following properties: </br> `name` A unique identifier for the appender </br> `class` The fully-qualified class name of the appender implementation.|
| <pre><code>&lt;encoder&gt; &lt;/encoder&gt;</code></pre> | In XML, an appender is used to define how log messages are handled in a logging framework. An appender specifies the target destination where log messages should be output, such as a file, console, or network socket, and also includes options for formatting and filtering log messages.|
| <pre><code>&lt;pattern&gt; &lt;/pattern&gt;</code></pre> |In the context of logging frameworks, a pattern is a string that defines the structure and content of the formatted log output. </br> `%date` Date and time of the log event. </br> `%level` Log level (e.g. INFO, ERROR). </br> `%logger` Logger name. </br> `%thread` Thread name. </br> `%msg` Log message. </br> `%n` Newline character. </br> `%class` Class name. </br> `%method` Method name. </br> `%line` Line number.|
| <pre><code>&lt;file&gt; &lt;/file&gt;</code></pre> | In Logback, the `file` tag is used to specify the name and location of the file where log messages should be written to|
| <pre><code>&lt;appender&gt; &lt;/appender&gt;</code></pre> | In XML, an appender is used to define how log messages are handled in a logging framework. An appender specifies the target destination where log messages should be output, such as a file, console, or network socket, and also includes options for formatting and filtering log messages. </br> An appender in XML typically has the following properties: </br> `name` A unique identifier for the appender </br> `class` The fully-qualified class name of the appender implementation.|

