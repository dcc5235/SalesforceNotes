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
  

  
</details>

<details><summary>Email Message Design</summary>
  

  
</details>

<details><summary>Marketing Automation</summary>
  

  
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
