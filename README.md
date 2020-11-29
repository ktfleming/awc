# awc
Quick access to AWS web console pages

#### Requirements

Requires the [AWS CLI](https://aws.amazon.com/cli/), [jq](https://stedolan.github.io/jq/), [fzf](https://github.com/junegunn/fzf), and zsh to be on your PATH.

### Installation

Just make the `awc` script executable and put it somewhere on your PATH.

### Usage

Select from a top-level AWS category (EC2, S3, SQS, etc.) using fzf, then select a sub-category (instances, buckets, queues, alarms, etc.). The AWS CLI will be used to query for a list of all items that fall under the selected sub-category and made available to select in fzf. Upon selection, it will open the details page for that item in Chrome. You can select multiple items (see [fzf documentation](https://github.com/junegunn/fzf#usage), defaults to TAB key) and then press Enter to open up all invidivual pages.

You can set the environment variable `AWC_FZF_OPTS` to change the options that are passed to fzf.

### Notes

Since I just made this for my own personal use,
- The command to open an item's page is hard-coded to use the macOS `open` command and Chrome
- The AWS categories and sub-categories are limited to those that I regularly use

Of course any PRs to improve/expand on the above are welcome.
