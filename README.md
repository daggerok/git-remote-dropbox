# git-remote-dropbox
Using Dropbox folder as a Git remote

__installation process__

1) Install by using pip

```bash
pip install git-remote-dropbox
```

2) Generate an OAuth 2 token by using [developer app console](https://www.dropbox.com/developers/apps)
  * create Dropbox API app token:
    * _with "Full Dropbox" access if you're going to be using Dropbox's sharing features to use git-remote-dropbox in a multi-user setup_
    * _or with "App folder" access if you prefer use single-user setup_
  * and create an access token for yourself
 
3) Save your OAuth token in `~/.config/git/git-remote-dropbox.json` or `~/.git-remote-dropbox.json` file.
The file should looks like this:

```json
{
   "default": "xxxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-xxxxxxxxxxxxxxxxxxxxx"
}
```

NOTE: see details in authored GitHub page

__lets you use Dropbox folder (or a shared folder) as a Git remote!__

Once the helper is installed, use it like so:

* clone dropbox folder as a repo:
  ```bash
  git clone "dropbox:///path/to/repo" -b master
  ```
* add remote to existing repo:
  ```bash
  git remote add origin "dropbox:///path/to/repo"
  ```

NOTE: _The repository directory will be created automatically the first time you push._

_links_

* [GitHub: anishathalye/git-remote-dropbox](https://github.com/anishathalye/git-remote-dropbox)
