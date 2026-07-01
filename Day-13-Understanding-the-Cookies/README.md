Day 13 - Understanding Cookies
Objective

Learn what cookies are, how websites use them to remember users, and understand why protecting cookies is important for web security.

Lesson of the Day

Today, I learned about cookies, one of the fundamental technologies used by websites.

A cookie is a small text file that a website stores in your browser. It allows the website to recognize you and remember information about your session or preferences.

Without cookies, websites would not be able to keep users logged in or remember settings such as language preferences and shopping carts.

What is a Cookie?

A cookie is a small piece of data stored by the browser on behalf of a website.

Cookies are commonly used to:

Keep users logged in.
Remember user preferences.
Store session information.
Personalize the browsing experience.
Track website activity.
Why Cookies Matter

Imagine logging into a website.

After successful authentication, the server creates a session and sends a cookie to your browser.

For every future request, the browser automatically sends that cookie back to the server.

Instead of asking you to log in again for every page, the server recognizes your cookie and knows that you are already authenticated.

Cookies in Network Communication

Whenever your browser communicates with a website, cookies travel along with the request.

The communication path is typically:

Browser
   ↓
Wi-Fi
   ↓
Router
   ↓
Internet Service Provider (ISP)
   ↓
Website Server

If the connection uses HTTP, cookies travel without encryption and can potentially be intercepted.

If the connection uses HTTPS, the cookies are encrypted while travelling across the network, making interception much more difficult.

Firesheep and Cookie Security

One important historical lesson involved Eric Butler, who released the Firesheep extension in 2010.

Firesheep demonstrated how session cookies sent over unencrypted HTTP connections could be captured on shared Wi-Fi networks.

Attackers could use these stolen session cookies to hijack logged-in sessions without knowing the user's password.

This demonstration encouraged websites to adopt HTTPS much more widely to protect users' sessions.

Practical Activity

Today's hands-on task was to understand how cookies work by inspecting and modifying them.

I:

Installed the Cookie-Editor browser extension.
Viewed the cookies stored by a website.
Edited a cookie value.
Logged in again and observed how cookies changed after authentication.

This activity helped me understand that cookies play a major role in maintaining user sessions.

What I Learned
Cookies are small text files stored in the browser.
Websites use cookies to recognize users and maintain sessions.
Session cookies are automatically sent with requests to the server.
HTTPS protects cookies while they travel across the network.
Understanding cookies is important for learning web security.
Key Takeaways

✅ Cookies help websites remember users.

✅ Session cookies allow users to stay logged in.

✅ HTTP can expose cookies to attackers because data is not encrypted.

✅ HTTPS protects cookies while they are transmitted.

✅ Browser developer tools and extensions can be used to inspect cookies for learning and testing purposes.

Reflection

Today's lesson helped me understand that something as small as a cookie plays a huge role in how websites work.

Before today, I only knew cookies were related to browsers. Now I understand that they are essential for authentication, session management, and user experience.

The practical exercise of viewing and editing cookies gave me a better understanding of how web applications manage user sessions behind the scenes.

Quote of the Day

"A cookie may be small, but it plays a big role in web security."

Progress Tracker
Day: 13/90
Topic: Cookies
Concepts Learned: Cookies, Session Management, HTTP vs HTTPS, Cookie Security, Firesheep
Practical Activity: Inspected and edited browser cookies using Cookie-Editor.
Key Insight: Cookies help websites remember users, but they must be protected with HTTPS to prevent session hijacking.
Status: ✅ Completed
