# Visual Studio Plugin for .NET Core Project

### No local cache found for Microsoft.AspNetCore.App.2.1.1

#### Observations:
1. Nexus IQ Component panel is showing an empty list, even after clicking the magnifiying glass.
2. Connections to Nexus IQ Server is fine.
3. No 403 error caused by Nexus Firewall.
3. It shows error message `No local cache found for <component-name.version>`

#### Cause:
Visual Studio has bundled the .NET Core components, without going through Nuget. So there is no Nuget cache for the plugin to analyze. This only affects .NET Core project.

#### Solution:
In Visual Studio `Package Manager Console`, manually install the package with this command: `Install-Package <component-name> -Version <version>`. For example:

```
Install-Package Microsoft.AspNetCore.App -version 2.1.1
```
Then, click the magnifying glass again to load the components. 

Repeat these step for other components that show up as no local cache. If you face "Blocked by project" error, please follow instructions from [this website](https://newbedev.com/microsoft-aspnetcore-app-2-1-1-upgrade-blocked-by-project).

