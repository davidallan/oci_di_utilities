# oci_di_utilities


# Setup
Define the following environment variables and then execute the script to create the tasks in OCI DI.  Get the project key and the workspace and the region and set;
export PROJECTKEY=
export WORKSPACE_ID=
export REGION=us-ashburn-1

# Install
install.sh

# Permissions

The theme for all of these permissions is to allow the disworkspace resource permission to perform the APIs concerned. The tasks have been defined using workspace resource BUT REST tasks can be defined to use workspace or application resource, application resource will give a tighter control. The example permissions can be further refined for example the specific operation can be added.

## Compute tasks
```
allow any-user to manage compute-container-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## Container Instance tasks
```
allow any-user to manage compute-container-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## Data Science tasks
```
allow any-user to manage data-science-family in compartment yourcompartment where ANY {request.principal.type = 'disworkspace'}	
```

## Object Storage tasks
```
allow any-user to manage object-family in compartment yourcompartment where ANY {request.principal.type = 'disworkspace'}	
```

## AI Speech tasks
```
allow any-user to manage ai-service-speech-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## AI Vision tasks
```
allow any-user to manage ai-service-vision-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## AI Speech tasks
```
allow any-user to manage ai-service-speech-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## AI Document tasks
```
allow any-user to manage ai-service-document-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## NoSQL tasks
```
allow any-user to manage nosql-family in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## Monitoring tasks
```
allow any-user to read metrics in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## Notification tasks
```
allow any-user to use ons-topics in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

## Dataflow tasks
```
allow any-user to manage dataflow-run in compartment yourcompartment where ALL {request.principal.type = 'disworkspace'}
```

