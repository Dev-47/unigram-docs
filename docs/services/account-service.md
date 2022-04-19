# unigram-accounts-service

This service will handle user / account based operations like;
- authentications
- profile updates
- preferences
- passwords / resets
- account types

# expected endpoints

- `/login/`
  - using `POST` method, pass `username` and `password` to request body to authenticate users and return a `token` along with any other information 
- `/register/`
  - using `POST` method, pass `email`, `username` and `password` to request body and return a `token` along with any other information
- `/logout/`
  - using `GET` method, invalidate/destroy existing `token` for a user
- `/profile/`
  - using `GET` method, return the authenticated user
  - using `PUT` / `PATCH` method, update user profile, update should not include password updates
- `password/reset/`
  - using `POST` method, pass `email` to request body
    - send OTP for password update
    - allow password to be updated if OTP is valid
