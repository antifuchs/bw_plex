# bw_plex
binge watching for plex

## Install
pip install -r requirements.txt


## Usage
bw_plex only works on python 2. :(

1. Download all the themes from pms using `plexjump.py update_all_themes`
2. Create audiofingerprints of the themes so the videos can be matched against something. `plexjump.py create_hash_table_from_themes`
3. Start using `plexjump.py start`

bw_plex will work without step 1 and 2, but it will be much slower.

How it works:

bw_plex will connect to plex using websocket and lisson for any playing events.
If will then download the theme and the first 10 minutes of the episode and try to figure out when the theme ends.
This can take some time so the first ep might simple be ignored. The next episode will be queued up so its ready when you start to watch it.
bw_plex will then seek to where the theme ended in that episode file.



