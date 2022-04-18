# unigram-accounts-service

This service will handle user/account based operations;
- authentications
- profile updates
- preferences
- passwords / resets
- account types

This service would be required to have the following endpoints
**NB**: Never return sensitive data to the json response. All response data must be in json format.

- login: to authenticate users with `username` and `password`, returns a `token` along with any other information (excluding `password`)
- register: register new users with `email`, `username` and `password`, returns a `token` along with any other information (excluding `password`)
- logout: invalidates existing `token` for a user
- profile: with mutiple request methods, a user profile can be fetched with one method(GET), and updated with another method(PUT/PATCH), profile update should not include password updates
- password update / reset: endpoint to reconfirm `username` and `password` and send OTP for password update
