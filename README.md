# oci_di_utilities


# Setup
Define the following environment variables and then execute the script to create the tasks in OCI DI.  Get the project key and the workspace and the region and set;
export PROJECTKEY=
export WORKSPACE_ID=
export REGION=us-ashburn-1

# Install
install.sh

# Permissions

The theme for all of these permissions is to allow the disworkspace resource permission to perform the APIs concerned.

## Container Instance tasks
allow any-user to manage compute-container-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
