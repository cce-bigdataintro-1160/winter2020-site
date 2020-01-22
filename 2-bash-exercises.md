### Create scripts to automate basic processes
* Any file containing shell commands can be executed as a shell script
* Shell script files will usually have a `.sh` extension and begin with the shebang line: `#!/bin/bash`
* In order to execute a script, first make it executable by adding the x permission right to it with `chmod +x <name of script>.sh`
* Then run it using `./<name of script>.sh`

1. Write a script that suggests the data formats: csv, xlsx, pdf, doc and txt. It should allow the user to pick their desired extension then create a file named `selected.<extension selected>`. Use the `read` command to read the user input!
2. Write a script that keeps only the first N number of lines of all files in '/Users/<myusername>/files_to_clean/*.csv'. N should be an argument passed before starting the script! If other people depend on this being done daily, how can we automate it's daily execution at 8:00AM? 
3. Answer what does this script do:
   ```
   #!/bin/bash
   for dir in 0 1 2 S
   do
     mkdir $dir-files
     touch $dir-files/$dir
   done
   ```

### Scheduling commands and scripts with the crontab
* The crontab is a command scheduler that allows us to run commands on predefined schedules
* Its widely used for maintenance tasks, like cleaning up directories and backing up data
* Uses a [crontab schedule expression](https://crontab.guru/) to describe the execution times
* Use the commands `crontab -e` to edit and `crontab -l` to list the existing scheduled commands
* Let's schedule our crontab to save the current date at every minute to the file dates.txt on the home directory as an example
