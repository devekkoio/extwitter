0.4.1
------
#### Enhancements
* Support specifying `user_id` as basic parameter in addition to the existing `screen_name` in the following functions.
    - ExTwitter.follower_ids
    - ExTwitter.followers
    - ExTwitter.friend_ids
    - ExTwitter.friends
    - ExTwitter.lists
    - ExTwitter.user_lookup

0.4.0
------
#### Changes
* Maps returned by the APIs will have atom keys instead of string keys.
* Use [poison](https://hex.pm/packages/poison) as internal JSON parser.
* Apply some benchmark related updates (#11, #13)

0.3.0
------
#### Enhancements
* Add `ExTwitter.follower_ids`, `ExTwitter.friend_ids`.
* Add `ExTwitter.RateLimitExceededError` for handling rate limit exceeded case.

#### Changes
* `ExTwitter.followers` and `ExTwitter.friends` now return `ExTwitter.Model.Cursor` instead of `ExTwitter.Model.User`. Call `cursor.items` for the returned cursor to fetch the list of users or ids.