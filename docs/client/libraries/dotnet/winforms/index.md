WinForms library
==========================

The WinForms client library can help you display error pages and collect information about the open forms.

## Error pages

An error page is displayed when an exception is detected. It looks like this per default:

![](/screens/libraries/winforms/winforms_error_minimal.png)

You configure it by using the following properties:

```csharp
Err.Configuration.UserInteraction.AskUserForDetails = true;
Err.Configuration.UserInteraction.AskUserForPermission = true;
Err.Configuration.UserInteraction.AskForEmailAddress = true;
```

Examples:

![all flags set](/screens/libraries/winforms/winforms_error_all.png)

![only ask for permission](/screens/libraries/winforms/winforms_error_permission.png)

![only details](/screens/libraries/winforms/winforms_error_details.png)

![only email](/screens/libraries/winforms/winforms_error_email.png)

## Context information

WinForms have to built in context collections

### OpenForms

Coderr collects information from all open forms using reflection. 

The information includes all controls and their configuration (position, content, visibility etc)

![Control content is included](/screens/libraries/winforms/winforms_open_forms.png)

### Screenshots

Screenshots can be activated by one of the following configuration lines:

```csharp
//only of the active form
Err.Configuration.TakeScreenshotOfActiveFormOnly();

// of all forms            
Err.Configuration.TakeScreenshots();
```

The context collection will be shown as:

![](/screens/libraries/winforms/winforms_screenshots.png)

# Links

* [WinForms API reference](https://coderr.io/docs/api/client/winforms)
* [Getting started guide](/getting-started/)
* [Server installation](https://coderr.io/documentation/server/installation/)
