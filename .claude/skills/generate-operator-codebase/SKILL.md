---
name: generate-operator-codebase
description: Use the templater in this repo to generate a codebase for basic HW orriented operators.
---

# Generate Operator Codebase

## Instructions
1. Make sure the templater binary is build for generating coebases
    - Check if the `templater` binary exists.
    - Build it if needed: `make templater`
2. Create a config file for your operator. You can use the example config files in the `configs` directory as a reference.
3. Run the templater directly from an empty dir to generate the codebase for your operator.
    - The output directory is always the current directory, so make sure to run the templater from the desired output directory.
    - Use `./examples/config-kmm-only.yaml` as default if no config file is provided.
        - Let the user know you are using a default config file if no config file is provided.
    - Run the templater: `<templater_binary> -f <path_to_config_file>`

## Debugging Tips
- Generating the code base will result in running `operator-sdk init` which will fail if the target directory isn't empty.
    In case you are running multiple attempts as part of your flow, make sure to clean the directory before retrying to run the 
    templater.

<!--
## Examples
Show concrete examples of using this Skill.
-->
