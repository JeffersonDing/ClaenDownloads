# ClaenDownloads

Automatically cleans Downloads folder for macOS

## Usage

After configuring the crontab job, the script runs every week to scan for file in the `Downloads` folder thats over 7 days old and moves them to the trash can.  

### Steps

1. edit the `rmdown` script and modify `<YOUR_USERNAME>` to your username
2. brew install `trash`
3. download or copy `rmdown` binary to `/usr/local/bin`
4. mark `rmdown` as executable by `chmod +x rmdown`
5. create crontab using `crontab -e` and enter the following
```
0 0 * * 0 /usr/local/bin/rmdown >dev/null 2>&1
```
6. check crontab using `crontab -l`


## Modifications
You can change how the script functions by directly modifiing `rmdown`. Change the number `7` to the age of the file in days that you want to remove. For example `10` means any files older than 10 days will be trashed.

You can also specify how often the script runs, please refer to crontab conventions when setting up the job.

# Happy Hacking! 💻

