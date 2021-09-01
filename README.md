# hello-servant-jwt

This is based on these tutorial
- https://github.com/haskell-servant/servant/blob/master/doc/cookbook/jwt-and-basic-auth/JWTAndBasicAuth.lhs
- https://docs.servant.dev/en/stable/cookbook/jwt-and-basic-auth/JWTAndBasicAuth.html

## Build and Run

```
stack build
stack exec hello-servant-jwt
```

Then on another console, you can do:
```
curl -v 'http://localhost:3001/bar'
curl -v 'http://user:wrong_password@localhost:3001/bar'
curl -v 'http://user:pass@localhost:3001/bar'
curl -v -H 'Authorization: Bearer eyJhbGciOiJIUzUxMiJ9.eyJkYXQiOnsiYXVPcmdJRCI6MSwiYXVJRCI6MX19.6ZQba-Co5Ul4wpmU34zXlI75wmasxDfaGRmO3BsOx-ONupX93OBfyYBCIJ3tbWMXKBVVqMDt0Pz-5CakyF2wng' 'http://localhost:3001/bar'
```
