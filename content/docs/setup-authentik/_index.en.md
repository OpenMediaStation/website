+++
title = 'Setup Authentik'
+++

## Create application

Go to applications

Create with wizard

Set name and slug

Select Oauth 2 open id provider

default-provider-authorization-explicit-consent

Public client save client id

Add redirect uris: 
my.test.app:/oauth2redirect
http://localhost:8000/redirect.html

Advanced => Authentication flow: default-authentication-flow

Advanced protocol settings => Access token validity hours=5

Add scope offline access

Access provider created and save  OpenID Configuration URL 

## Ensure DeviceCodeAuthorization flow


