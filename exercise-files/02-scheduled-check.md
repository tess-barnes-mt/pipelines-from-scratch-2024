# 2 - scheduled pipelines

## Instructions
We don't want to remember to check links on the Madetech Learn site, we want it to happen regularly automatically.

- Copy the link-checker config you created in exercise 1 into the yaml file for this exercise
- Create a cron statement for a time 10 minutess in the future
- Add a schduled trigger to the pipeline config
- Make sure the config file is in the `.github/workflows` folder
- Commit & push your code
- Check the pipeline has run after the time has elapsed
- Change the schedule to run every 10 minutes
- Commit & push your code
- Once you have seen your scheduled pipeline run on schedule, use the web interface to disable it

## Hints
Github runs the schedule and we will be using a github hosted runner for the pipeline. Because of high volumes the schedule might be late.

Github only supports Standard Cron syntax, check your cron statement before using it

## References
Scheduled workflows: [Github docs](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#schedule)

Check your cron syntax: https://crontab.guru/ 

## Notes


