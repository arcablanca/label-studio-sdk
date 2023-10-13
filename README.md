# Label Studio Python SDK

Use this Python SDK to integrate Label Studio into your data science and machine learning pipelines to make data labeling simpler. 

With the Label Studio Python SDK, you can perform the following tasks in a Python script:
- Create a Label Studio project, including setting up a labeling configuration. 
- Import tasks from external or local storage, including pre-annotated tasks.
- Modify project settings, such as task sampling or the model version used to display predictions. 
- Create annotations from predictions or pre-annotated tasks. 
- Retrieve task annotations, including specific subsets of tasks.  
See the [Label Studio SDK Tutorial](https://labelstud.io/guide/sdk.html) for example code snippets and additional details. 

If you want to take action not supported natively by the SDK, you can [call the API](https://labelstud.io/api) directly and consider contributing to the SDK.

## About the SDK

This is the first release of the Label Studio SDK. It supports Label Studio Enterprise, Label Studio Teams, and Label Studio Community.

- **Find a bug?** [Create a GitHub issue](https://github.com/heartexlabs/label-studio-sdk/issues)!
- **Have a question?** [Join the Slack Community](https://slack.labelstud.io/?source=github-sdk)!
- **Want to contribute?** [See the contributing guide](https://github.com/heartexlabs/label-studio-sdk/CONTRIBUTING.md)

## Quickstart
To start using the SDK in your machine learning and data science projects and pipelines, do the following:

1. Install the SDK using pip: `pip install label-studio-sdk`
2. Import `label_studio_sdk` in your Python script.
3. Connect to the API and create a project:
```python
from label_studio_sdk import Client

ls = Client(url='http://localhost:8080', api_key='YOUR-API-KEY')
ls.start_project(title='New Project', label_config='<View></View>')
```

## Available classes and methods

The Label Studio SDK includes the following:
- a Client module to handle authentication
- a Data Manager module for filtering tasks in Label Studio
- a Project module to take actions related to Label Studio labeling projects 
- a Utils module for working with the labeling configuration

For all the details, see the [reference documentation](https://labelstud.io/sdk) or [review the code directly](https://github.com/heartexlabs/label-studio-sdk/tree/master/label_studio_sdk). 

## Error logging

To see error logs, you can use `stderr` (we use `logger.error()` for error output). If you use console to run SDK commands, you will see all errors there. 

## Contribute to the SDK

If you want to extend the SDK:

1. Pull this repository. 
2. Install the SDK locally 
3. Follow the [contributing guidance](CONTRIBUTING.md) 

## Examples

Please check [the examples folder](examples), there are many of very useful codes that you can learn from. 
