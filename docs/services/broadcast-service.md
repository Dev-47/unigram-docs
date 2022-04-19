# unigram-broadcast-service

This service will be responsible for sending broadcast to a specific channel (group) and the memebers in that channel can add comments to each broadcast
sent. Permissions are restricted to authorized users only with permission of `can_send_broadcast` from the `unigram-account-service`.
All users must be authenticated to perform any action on this service. Broadcasts can only be edited by the `author`.

# expected endpoints

- `/broadcast/`
  - using the `GET` method, list all broadcast available, and also allow options to use filters
    - filter options: `date_of_creation`, `category`

  - using the `POST` method, broadcasts can get created by authorized users with the permission of `can_create_broadcast`
    - each broadcast should belong to a university
    - each broadcast should belong to a new / exisiting category
    - broadcast category can be nested

- `broadcast/:broadcast_id/`
  - using the `GET` method, a broadcast can be fetched using the `broadcast_id`, this should return a single broadcast object

- `broadcast/:broadcast_id/join/`
  - using the `GET` method, an authenticated user that belongs to a university can request to join a broadcast

- `broadcast/:broadcast_id/leave/`
  - using the `GET` method, an authenticated user that belongs to a university can leave a broadcast

- `broadcast/:broadcast_id/send-broadcast/`
  - using the `POST` method, an authenticated user with the permission of `can_send_broadcast` can send broadcast to channel
  - pass all data to the body of the request
