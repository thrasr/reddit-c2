==Overview==
This is a prototype concept for a command and control (CC) system with communication through reddit. This communication should be encrypted and anonymous.  

The server runs and has an account for posting to reddit.  There should be a dedicated subreddit that only this account has posting privledges to.  The account may also need to have several successful posts before being allowed to post at certain intervals.  Some initial manual posts may be required before the account has enough privledges to post successfully.

The client monitors the subreddit and listens for commands (posts).  Clients should decipher each post and determine what action to take.  Actions include ignoring/dropping to command (if not targeted at the client) or performing a predetermined action in accordance to the command posted.


==Setup==
* Python 2.7
* [PRAW](https://github.com/praw-dev/praw)


==Server==
* Python
* PRAW to post commands
* Hardcoded login info

==Client==
* Python
* PRAW to monitor subreddit (on a X minute loop)
* Anonymous (no login info)
* Listens for commands

==Payload==
* Target (some what of identifying clients)
  * All clients = '*'
  * Specific client = ID number (how do clients get assigned/communicate IDs to server?)
  * Groupings of clients = A letter designates each grouping.  Groupings would be pre-assigned based on what the client is designed to dol
* Command
* Payload - various possibilities (or nothing) - depends on command given
  * URL
  * File location for storage
  * Torrent files (pass file as bytes or possibly just contents of file and create a file on other end?)


==Possible Commands==

=Bitcoin=
* Turn on/off miner


=BitTorrent=
* Download .torrent file
* Torrent file
* Check for .torrent file
