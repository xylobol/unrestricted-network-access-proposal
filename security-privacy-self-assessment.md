https://www.w3.org/TR/security-privacy-questionnaire/

### 3.1 Does this specification deal with personally-identifiable information?

Yes: IP addresses. In addition, it could be used to communicate personally-identifiable information.

### 3.2 Does this specification deal with high-value data?

Yes. See 3.1.

### 3.3 Does this specification introduce new state for an origin that persists across browsing sessions?

No.

### 3.4 Does this specification expose persistent, cross-origin state to the web?

Yes. The proposed capabilities of the API would allow a web application to bypass CORS and CSP checks. 

### 3.5 Does this specification expose any other data to an origin that it doesn’t currently have access to?

Yes. If permission is granted, the proposed API could be used to send and recieve arbitrary data.

### 3.6 Does this specification enable new script execution/loading mechanisms?

No.

### 3.7 Does this specification allow an origin access to a user’s location?

Yes, in the form of imprecise IP location data. 

### 3.8 Does this specification allow an origin access to sensors on a user’s device?

No.

### 3.9 Does this specification allow an origin access to aspects of a user’s local computing environment?

Yes. It would allow access to the public and (if applicable) private IP addresses of the device.

### 3.10 Does this specification allow an origin access to other devices?

No.

### 3.11 Does this specification allow an origin some measure of control over a user agent’s native UI?

No.

### 3.12 Does this specification expose temporary identifiers to the web?

Yes. If the network was configured with DHCP, the proposed API would allow access to the public and (if applicable) private IP addresses of the device.

### 3.13 Does this specification distinguish between behavior in first-party and third-party contexts?

No.

### 3.14 How should this specification work in the context of a user agent’s "incognito" mode?

No change in behavior.

### 3.15 Does this specification persist data to a user’s local device?

No.

### 3.16 Does this specification have a "Security Considerations" and "Privacy Considerations" section?

Yes.

### 3.17 Does this specification allow downgrading default security characteristics?

Yes. If permission were granted by the user, the proposed API would allow communication of arbitrary information to and from arbitrary origins, sidestepping CSP and CORS.
