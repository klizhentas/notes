# Ideas about social network

## Things I care about

* No ads, no data mining by third parties
* Decentralized. Can be hosted on third party servers, on own server.
* Data is encrypted and decrypted on the client. Servers do not have access to the data.
* Trust is established using crypto. Use PGP to share keys.
* Dead easy to implement. Use simple technologies like git, https, pgp. Prototype should work with curl, git and bash.
* Should be usable by my mom and friends, so web ui should be as easy as your average social network
* Should have some integration with email, so I can reply by email or get daily digest.

## Things I don't care about

* Scalability. Should work for me and my friends, don't care about large scale groups then.
* Search, etc. I care about receiving some news about my friends and share some notes sometimes.

## Friends and sharing

Friends group is represented by a set of public keys, where every public key represents user identity.
If I wish to share the post with my friends, I will encrypt the post using their public keys.
Every friend can decrypt the post with their private key.



## Publishing

All my posts are in git in some folder (e.g. by date of publication):

network/posts/<date>/<timestamp>_<post_contents_sha512_hash>.md.gpg
network/posts/<date>/<timestamp>_<post_contents_sha512_hash>.files.gpg

If I wish to publish the post to my group, for each user in the group:

network/friends/username/posts/<date>/timestamp_post_name_hash.md.gpg
network/friends/username/posts/<date>/timestamp_post_name_hash.files.gpg

My friends can look into their feeds by checking their feeds for updates

network/feeds/sasha contains url of the web service hosting my posts:

 https://<sasha-url>/network/friends/anna/posts/<date>
                 

Anna can open and decrypt my feeds by syncing and decrypting the data with their private keys:

network/feeds/sasha/synced/posts/<data>timestamp_post_name_hash.contents.gpg
network/feeds/sasha/synced/posts/<dat>timestamp_post_name_hash_files.md.gpg

Note that synced files could be decrypted with Anna's private key.

network/friends/<date>/post_name_files.gpg

## Things to sort out

* How to rotate private keys
* File naming and hashing. Use CAS to make it easy to sync data from peers. Do not expose metadata in file names.
* How to decrypt on the client and post.
