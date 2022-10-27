# AccessToken and RefreshToken

JWT

- Json Web Token (form of identification)

after login proccess is completed, REST Api will issue the client application an access token and refresh token

Access Token = Short Time
Refresh Token = Long Time

Hazards
XSS
CSRF

Access Token:

- Sent as JSON
- Client stores in Memory
- Do NOT store in local storage or cookie

Refresh Token

- Sent as httpOnly cookie
  Not accessible via Javascript
  Must have expiry at some point

Access Token
Issued at authrization
client uses for API access until expires
verified with middleware
New token issued at refresh request

Refresh Token
Issued at Authorization
Client uses to request new Access Token.
verified with endpoint & database
must be allowed to expire or logout.
