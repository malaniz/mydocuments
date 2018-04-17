[x] get the access token
  [x] generate manually the token
    ```
    ruby -e "require 'securerandom'; puts SecureRandom.urlsafe_base64 24"

    U6DJxpr0NqUyHOyY903IKUjZEcyvNeMf
    ```
  [x] insert into the table access_token on getlisteddb
    ```
    use getlisteddb;
    insert into access_tokens (
      user_id, access_token
    ) values (
      100146363,
      'U6DJxpr0NqUyHOyY903IKUjZEcyvNeMf'
    )
    ```
  [x] test if that works
    ```
    use getlisteddb;
    select * from access_tokens;

    id 	 user_id   	 access_token                     	 updated_at          	 created_at          	 invalidated_at
    1  	 100146363 	 U6DJxpr0NqUyHOyY903IKUjZEcyvNeMf 	 2018-04-17 17:46:58 	 2018-04-17 17:46:58 	 NULL
    ```

[ ] make the first entrypoint call with success
  [ ] trying to get insights domains
    ```
    curl http://local.moz.com:8080/local/api/v1/insights/domains?access_token=U6DJxpr0NqUyHOyY903IKUjZEcyvNeMf
    ```
