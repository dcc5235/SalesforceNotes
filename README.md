# Salesforce Email Marketing Notes

<details><summary>Email Marketing Best Practices</summary>

#### CAN-SPAM (The Controlling the Assault of Non-Solicited Pornography And Marketing Act) Requirements
The CAN-SPAM act requires that Commercial emails, whose primary purpose is to deliver commercial content, meet the following criteria:

- Accurately identify the sender in the header information.
- Use a subject line that accurately represents the content of the email.
- Identify the message as an advertisement, unless you have express consent (opt-in) from the subscriber.
- Include your physical mailing address.
- Provide a mechanism to opt out. You cannot require a subscriber to log in or visit more than a single page to unsubscribe.
- Honor opt-out requests within 10 days.
  
#### CAN-SPAM Explanation
The CAN-SPAM act is a law that sets:

- The rules for commercial email
- Establishes requirements for commericial messages
- Gives recipients the right to have you stop emailling them
- Spells out tough penalties for violations
  
#### Transactional Messages
If a customer orders a product from your website, the receipt sent via email is a transactional message. Transactional messages must identify the sender in the header information. 
  
#### Optimize Deliverability of Messages

1. Ensure subscribers have opted in
2. Have a recognizable "From Name" and "Email Address"
3. Manage cadence of messaging and frequency of content (ideally set expectations on this with the subscriber)
4. Purge old or inactive emails
5. Authenticate your email: Domain keys, Sender ID, and SPF Configuration
  
</details>

<details><summary>Email Content Creation</summary>

#### Content Personalization
In the world of digital marketing, content is typically characterized as either static or personalized. Static content does not change for any reason, for example, the company logo at the top of an email or social links at the bottom (header and footer). Personalized content changes based on data found in the data extension or list at the time of a send or push, for example, a person’s name within a text or specific content related to their interests.
  
- Personalized content: 
  1. Personalization strings (%): Insert subscriber attributes, such as subscriber name, into the subject line, preheader, or content of your email. These can be People or System attributes. Note they are case-insensitive, and should always have a default value set.
  2. Dynamic content: Display content according to rules that you define based on the subscriber’s attributes or data extension field values. Select Subscriber/Send Preview to see how Dynamic Content and AMPscript renders in an email (can set country to specific images).
  3. AMPscript: Use this scripting language to embed subscriber-specific content within HTML emails, text emails, landing pages, SMS messages, and push notifications from MobilePush.

- Dynamic Header/Pre–Header: You can set a rule to change the header/pre-header based on subscriber attributes. E.g. if an individual has a birthday coming up, a rule can be set to say ‘Happy Birthday!’ in the header/pre-header
  
#### Content Blocks
- A/B Testing
- Button
- Code Snippet
- Dynamic Content (a more tailored message reaches segmented audience)
- Enhanced Dynamic Content (import to content builder)
- External Content (reference from a URL)
- Free Form (links, images)
- HTML
- Image Block
- Image Carousel
  
#### Create Email
1. SF provides various templates, but you can choose your own email creation process. 
  - Template Based: Choose this option if you already have a template that you’re using for this email.
  - HTML Paste: Choose this option to type or paste HTML code for an email into the editor.
  - Text Only: Choose this option if you want to create an email that displays as text only in your subscribers’ inbox regardless of their display preferences. Opens data is never reported for text-only emails.
  - Unprocessed HTML Paste: Choose this option if you want to create an HTML-based email that you do not want to be affected by the application. No validation, personalization strings, or other manipulations are done to the email’s content.
  - Unprocessed Text Only: Choose this option if you want to create a text-only email that you don’t want to be affected by the application. No validation, personalization strings, or other manipulations are done to the email’s content. 
  - Simple Automated Email: Choose this option if you want to create an email you send based on a date attribute. For example, if you want to send your subscribers an email on their birthday, you can create an automated email.
2. Add content - SF includes code snippets.
  - Physical Mailing Address (Required per CAN-SPAM)
  - Forward to a Friend
  - View Email as Webpage
  - Privacy Policy
  - Unsubscribe Center
  - Profile Center (Required per CAN-SPAM)
3. Preview & test - test emails based on subscriber preview & attributes.
  
#### Create Content Blocks & Email
You can create a wide range of content blocks with Marketing Cloud, including text, image, text + image, free form, HTML content, dynamic content, A/B testing, button, social share, add a social Follow Block,layouts, external content, reference, and image carousel.

Note: Link Title is the text that describes the link to the subscriber.
</details>

<details><summary>Email Delivery</summary>
At this stage of the email send flow, you can edit the email, see its properties, copy location of email, etc. Next, define properties, select audience, configure delivery (send immediately or schedule delivery, track clicks), then review and send. 

  1. Define Properties: Edit the subject line, preheader, from options, and send classification.
  2. Select Audience: Select the audience you want to target and any you want to exclude or suppress. You can send to all audience types, including sales Cloud Reports and Campaigns.
  3. Configure Delivery: Configure your schedule, send throttling, and any advanced options.
  4. Review and Send: Preview the selected email, review send configurations, correct errors, and send.
  
Subscriber Preview in Content Builder allows you to view a single email, including
- dynamic content,
- A/B testing,
- personalization
  
Note: Use Subscriber Preview to see exactly what the email will look like to an individual subscriber in a data extension.

#### User Initiated vs Triggered Emails
  
User Initiated Send is a method where you can specify and target specific components such as email, audience, suppressions, etc. You are able to schedule sends with those on demand or you could trigger them via API.

A Triggered Send is listening for an action most like done via an API call to initiate the send. For example, a customer form fill-out, a purchase will trigger a response email built in the Marketing Cloud. This can be built in Interactions in Email Studio.
  
</details>

<details><summary>Email Message Design</summary>

#### Email Sender Definitions

- Sender Profile: Specifies the ‘From’ information – From Name, From Email, Description of the Sender
- Delivery Profile: Specifies the IP Address the email is sending from, as well as configuring a standard Header and Footer profile
- Send Classification: Defines the CAN-SPAM classification of the email (i.e. if the message is transactional or promotional), plus groups together the Send Profile, Delivery Profile, and Send Priority of each classification
- Send Throttle: Allows you to send emails during the hours you specify, starting the day you send the email until all messages are sent. Example: This can be configured that emails are only sent between 9am-5pm ET each day.

#### Mobile vs Responsive Templates

Mobile aware are user design tactics to create a single, mobile-friendly template that can work across all screen types. Often they are therefore:
- single column,
- using large text,
- images, and buttons,
- and spaced out buttons and links.

Responsive templates are designed to be responsive, serving up versions of an email that are optimized for a screen. It often involves extra coding or additional template design.  When coding a responsive design for email, CSS3 Media Queries are used to activate the mobile version.
  
#### Testing Tools within the Marketing Cloud
- A/B Testing
In Marketing Cloud you can perform A/B testing on:
 - Subject Lines
 - Emails
 - From Names
 - Content Areas
 - Send Date and Time
 - Pre-headers

Note that in A/B testing, you select the desired audience test segment sizes and the system automatically sends the winning version to the remainder audience.  Not the other way around.  And also you CANNOT select individual subscribers, you only select the segment sizes.

#### Testing Tools within the Marketing Cloud:
- Content Detective – Spam filtering software to identify words, patterns, and phrases that are likely to trigger spam filters. It also suggests solutions to potential problems. It does not scan HTML code.
- Validation – Will confirm Correct field syntax, content and data being used for Dynamic Rules are being used correctly, Guide Template Language and AMPScript is being used correctly and also validates for the presence of Unsubscribe link and From Email address.
- Send Preview – Allows you to see how your email will render with Personalisation strings populated, Dynamic content displaying based on subscriber data, and Guide Template Language and AMPScript will be executed and the data will be displayed or the content will be rendered.
- Test Send – Allows you to see how content will render, will send up to 5 email addresses at once, though personalization does not populate, dynamic content displays default content, AMPscript code and Guide Template Language is displayed, and not all links are active.
</details>

<details><summary>Marketing Automation</summary>

#### Automation Tools
1. Playbooks – step-by-step guides for executing digital marketing through the customer lifecycle. 3 are available: Welcome series, Birthday email, and Customer Anniversary 

NOTE: Playbooks will no longer be supported from January 2019. They are featured in Journey Builder for quick starts.

2. Triggered Emails – Message sent to an individual executed from an event that happens outside the Marketing Cloud (e.g. sign up, form fill-out etc.). Triggered emails include Welcome emails, Purchase Confirmation, Abandon Shopping Cart, or Shipping Notices
3. Journey Builder – 1:1 marketing engine that allows you to build real-time messages in customer journeys across online and offline channels based on customer behaviour. Used for customer lifecycle programs. Includes Journey Builder templates such as Abandon Cart, Anniversary Send, Onboarding/Welcome
4. API – For technical resources. The API source code allows applications to communicate with one another.
5. Automation Studio – Drag and Drop interface to define a workflow that automates various activities. E.g. import data, refresh segments, export data, or send emails.
  
#### Automation Studio
Steps to build an automation

1. Select the Type of Automation:
  - Scheduled – Based on a schedule you define the date and time to start the automation, how often the automation is to execute, and when the automation is to stop
  - Triggered/File Drop (Note this has been renamed to ‘File Drop’) – Automation will start as soon as a file is placed on your designated enhanced FTP.
2. Build your automation workflow with Steps and Activities

Workflow – Your Automation canvas where you define and create your Automation

Steps – The order in which activities are to be executed

Activities – A task to be executed in Automation Studio

An automation can have multiple steps. Each step can have multiple activities. All activities within a step execute concurrently, and all activities in the step must execute successfully before moving to the next step. 

#### Activities

- Data Extract Activity – It gives you the ability to extract tracking information or data from a data extension. This allows you to transform an XML file into a comma-delimited, tab-delimited, or pipe-delimited format for you to import into Email
- Import File Activity – Will import the file from an FTP site to a list or data extension.
- File Transfer Activity – Allows you to de-encrypt or unzip a file or to take a file that has been extracted and place it on the FTP location.
- Filter Activity – Applies the data filter to a list or a data extension and places the results in a filtered list or filtered data extensions. The filter only works on 1 Data Extension
- Refresh Group Activity – Used with lists only. Takes the criteria for the group and applies it to the list to refresh the segment.
- SQL Query Activity – Takes the SQL statement and applies it to the specified data extension. The records meeting the criteria are placed in a resulting data extension. SQL can run on multiple data extensions.
- Send Email Activity – Allows you to choose a User-Initiated Email definition to execute or allows you to define the parameters for the Send.
- Verification Activity - Avoid unintended outcomes by verifying the data used in an Automation Studio automation.
- Script Activity - A Server-Side JavaScript activity contains your Server-Side JavaScript and executes that script when started, either on its own or as part of automation in Automation Studio.
- Wait Activity - Wait activities in Automation Studio cause automation to wait for a specific duration or until a specific time before performing the next step. You can include one or multiple wait activities in single automation.

NOTE – You must define the activities in their respective application prior to setting up automation. E.g. define File Import, or configure Email/ SMS send
  
</details>

<details><summary>Data Management</summary>
  

  
</details>

<details><summary>Data Segmentation and Refresh</summary>
  

  
</details>

<details><summary>Subscribers Management</summary>
  

  
</details>

<details><summary>Tracking and Reporting</summary>
  

  
</details>

<details><summary>Lorem Ipsum</summary>
  

  
</details>
