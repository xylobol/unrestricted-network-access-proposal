# Unrestricted Network Access in Progressive Web Apps

This is a proposal for adding a web API that allows Progressive Web Applications to request unrestricted network access. Unrestricted network access would include, but not be limited to,

* a way to sidestep content security policy and/or cross-origin resource security on networked resources,
* a way to send arbitrary data to a server or other system, and
* access to details such as the public and private IP address of the device.

This sort of access could be dangerous, so it needs to be granted by the user and be easy to revoke. The user agent would need to be very clear on what the permission does and how to revoke it.

## Use Cases

* A media player could use the API to, for example, load a podcasts RSS feed from a server with a different origin and strict CSP/CORS, parse the feed, then load an audio file from the same server.- 
* An instant messaging application could use the API to load an image from a server with strict CSP/CORS, without needing to use its own backend as a proxy of sorts.
* A third-party social network client could use the API to access a social networks API.
* An email client could use the API to communicate with an POP3 server to download messages.

## Why do we need a new built-in API?

* There’s no way for the above use case examples to exist unless they had the infrastructure to support such a thing.
* Progressive Web Apps can become more aligned with the ability of native programs.

## Security & Privacy

Allowing complete unfettered network access has many obvious security and privacy issues. Therefore, access to the API should only be granted if all the following circumstances are met:

* The user has initiated action on the requesting page (e.g., clicked a button),
* a secure context is requesting access, and
* the PWA has been installed/added to the home screen.

In addition, the User Agent should make the ramifications of granting permission very clear, and make it easy to revoke the permission.

## Alternatives Considered

* Not having a dedicated API at all, and retaining the current model of a client interacting with its backend to access CSP/CORS-protected assets.
  * This isn’t ideal because serverless PWAs cannot access protected assets, and there’s still limited access to the local network (e.g., accessing internal IP address).

## Potential Follow-Up Work

* We have not done the work of defining the API with a WebIDL document yet.
* The ability to convey network connectivity status should be considered (e.g. whether the device is on WiFi or mobile data, what kind of mobile data connection, whether the device is in data-saver mode or the network is flagged metered)
