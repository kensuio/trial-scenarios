# Kensu Trial Scenarios for Matillion
## Overview
This repository contains assets designed to support  [Kensu trial](https://www.kensu.io/free-trial) users to create common Data Observability scenarios within their Matillion environments.

Each directory's README provides more detailed guidance tailored for the individual scenarios and configuration.


## Importing Scenario Files into Matillion

1. **Open Matillion**: Log in to your Matillion instance.
2. **Navigate to Project**: Go to the project where you want to create the scenario jobs.
3. **Import Asset**: 
    - Go to `Project` > `Import`
    - Choose `From File` and select the appropriate JSON file from the sub-directory.
4. **Configuration**: Follow any instructions contained within the README for the individual Pupose Built scenario to complete project configuration.
5. **Validation**: Confirm that jobs and variables are populated correctly.

## Repository Structure
The repository is organized into directories for each Purpose-Built Matillion Destination highlighted in the  [Kensu trial](https://www.kensu.io/free-trial) .  Each sub-directory contains JSON files that can be imported to populate a Matillion project with the jobs and variables needed to create specific Kensu trial scenarios.

```plaintext
    ├── Matillion_for_Snowflake/
    │   └── matillion_job.json
    └── Matillion_for_Redshift/ (Coming Soon)
 ```   
## Supported Technologies

- Matillion for Snowflake
