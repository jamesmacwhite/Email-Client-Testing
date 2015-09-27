Email Client Testing Templates
====================

The varying level of HTML/CSS support in email clients makes the job of an email developer a pain. Luckily there are many testing tools out there that allow you to test your email campaigns in a variety of clients, but what happens when you want to find out the underlying rendering engine and its HTML/CSS support? Unfortunately screenshots won't help you here (only tell you something isn't right), but this is where these specifically designed email testing templates come in!

These templates have been designed so you can simply copy and paste and send to any email address to view in any type of email client/inbox of your choice, from here the specially designed templates will give you various information about the email client without you have to do anything (other than send the test of course!)

## Email Client Test

This template aims to test the rendering engine and key technical areas of the email client and present that information to the user via a series of test results.

The two possible outcomes of each test will either be a pass or a fail:

* Red Block - Indicates a FAIL in the specified test
* Green Block - Indicates a PASS in the specified test

**When reviewing the results of the test it is important to be aware of the notes/limitations documented below.**

* IE based clients are forced to render at the highest document mode available (edge) for consistency.
* Internet Explorer 10/11 no longer supports conditional comments unless rendered with a lower document mode less than or equal to Internet Explorer 9 (IE 9). A specific CSS media query is used to detect IE 10/11.
* Windows Phone 8.1 (GDR1 and above) will report true to the WebKit test as IE Mobile 11 will parse some WebKit properties due to changes to the browser.
* Google Chrome (version 28 and above) uses a forked version of Webkit (Blink), however Google Chrome will still report true to the WebKit engine test.
* The HiDPI device test relies on CSS3 support, so if CSS3 is not supported then the test will return false

## Email Acid Test

This template is originally from the [Email Standards Project](http://www.email-standards.org/acid-test), it has been modified with additional tests, including HTML5 and also corrects some minor issues with the original version.

The acid test visually demonstrates the HTML/HTML5/CSS support level of the client that it is rendered in. It is designed to complement the email client test.

## How do I test an email client?

In order to test an email client you'll need to send the a test template through a proper MTA. Litmus offers a free service call PutsMail, which allows you to send an email template to any email address.

1. Go to https://putsmail.com/tests/new
2. Add a single or multiple recipients
3. Paste in the HTML source of any template
4. SEND!

When using PutsMail for the first time, you'll be required to confirm the specified email address is OK to receive tests from PutsMail (this done via a confirmation email with an approve link). Once this has been activated you can then send emails to the email address without any further confirmation.
