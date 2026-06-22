# SocialGoal.Core

## Summary

| Metric | Value |
|--------|-------|
| Total Issues | 24 |
| Mandatory Blockers | 8 |
| Potential Issues | 9 |

## Component Information

| Property | Value |
|----------|-------|
| Language | C# |
| Frameworks | .NETFramework,Version=v4.5 |
| Build tools | MSBuild |

## Cloud Readiness Issues

| Issue Name | Criticality | Story Points | Occurrences |
|------------|-------------|--------------|-------------|
| Windows authentication detected | Mandatory | 3 | [1](#Windows_authentication_detected) |
| Old .NET Framework dependency detected | Potential | 3 | [7](#Old_NET_Framework_dependency_detected) |
| Hardcoded URLs detected | Potential | 1 | [5](#Hardcoded_URLs_detected) |
| Local or network IO operations detected | Potential | 3 | [2](#Local_or_network_IO_operations_detected) |
| SMTP connections detected | Potential | 3 | [1](#SMTP_connections_detected) |
| SQL database connection detected | Potential | 3 | [1](#SQL_database_connection_detected) |
| Access to external resources via HTTP is detected | Potential | 3 | [1](#Access_to_external_resources_via_HTTP_is_detected) |
| Hardcoded sensitive data detected | Optional | 3 | [30](#Hardcoded_sensitive_data_detected) |
| MachineKey dependency is detected | Optional | 3 | [3](#MachineKey_dependency_is_detected) |
| Connection strings without configuration builders detected | Optional | 3 | [2](#Connection_strings_without_configuration_builders_detected) |
| Static content detected | Optional | 3 | [1](#Static_content_detected) |
| System.Data.SqlClient dependency detected | Optional | 3 | [1](#System_Data_SqlClient_dependency_detected) |
| Synchronous API usage detected | Optional | 1 | [1](#Synchronous_API_usage_detected) |

### Issue Details

<details id="Windows_authentication_detected">
<summary><b>Windows authentication detected</b> — affected files</summary>

- `SocialGoal\Web.config`

</details>

<details id="Old_NET_Framework_dependency_detected">
<summary><b>Old .NET Framework dependency detected</b> — affected files</summary>

- `SocialGoal.Core\SocialGoal.Core.csproj`
- `SocialGoal.Data\SocialGoal.Data.csproj`
- `SocialGoal.Model\SocialGoal.Model.csproj`
- `SocialGoal.Service\SocialGoal.Service.csproj`
- `SocialGoal.Tests\SocialGoal.Tests.csproj`
- `SocialGoal.Web.Core\SocialGoal.Web.Core.csproj`
- `SocialGoal\SocialGoal.Web.csproj`

</details>

<details id="Hardcoded_URLs_detected">
<summary><b>Hardcoded URLs detected</b> — affected files</summary>

- `SocialGoal.Tests\Controllers\AccountControllerTest.cs (line 685)`
- `SocialGoal.Tests\Controllers\AccountControllerTest.cs (line 740)`
- `SocialGoal.Tests\Controllers\AccountControllerTest.cs (line 782)`
- `SocialGoal.Tests\Controllers\EmailRequestControllerTest.cs (line 150)`
- `SocialGoal.Tests\Controllers\EmailRequestControllerTest.cs (line 237)`

</details>

<details id="Local_or_network_IO_operations_detected">
<summary><b>Local or network IO operations detected</b> — affected files</summary>

- `SocialGoal\Controllers\AccountController.cs (line 427)`
- `SocialGoal\Controllers\AccountController.cs (line 429)`

</details>

<details id="SMTP_connections_detected">
<summary><b>SMTP connections detected</b> — affected files</summary>

- `SocialGoal.Tests\Controllers\GoalControllerTest.cs (line 1157)`

</details>

<details id="SQL_database_connection_detected">
<summary><b>SQL database connection detected</b> — affected files</summary>

- `SocialGoal\Web.config`

</details>

<details id="Access_to_external_resources_via_HTTP_is_detected">
<summary><b>Access to external resources via HTTP is detected</b> — affected files</summary>

- `SocialGoal\Controllers\AccountController.cs (line 455)`

</details>

<details id="Hardcoded_sensitive_data_detected">
<summary><b>Hardcoded sensitive data detected</b> — affected files</summary>

- `SocialGoal\Web.config`
- `SocialGoal\Controllers\AccountController.cs (line 203)`
- `SocialGoal\Controllers\AccountController.cs (line 81)`
- `SocialGoal\Controllers\AccountController.cs (line 166)`
- `SocialGoal\Controllers\AccountController.cs (line 167)`
- `SocialGoal\Mailers\UserMailer.cs (line 48)`
- `SocialGoal\Mailers\UserMailer.cs (line 45)`
- `SocialGoal\Models\AccountViewModels.cs (line 25)`
- `SocialGoal\Models\AccountViewModels.cs (line 58)`
- `SocialGoal\Models\AccountViewModels.cs (line 15)`
- `SocialGoal\Models\AccountViewModels.cs (line 21)`
- `SocialGoal\Models\AccountViewModels.cs (line 26)`
- `SocialGoal\Models\AccountViewModels.cs (line 38)`
- `SocialGoal\Models\AccountViewModels.cs (line 54)`
- `SocialGoal\Models\AccountViewModels.cs (line 59)`
- `SocialGoal\Models\AccountViewModels.cs (line 26)`
- `SocialGoal\Models\AccountViewModels.cs (line 59)`
- `SocialGoal\Properties\Resources.Designer.cs (line 76)`
- `SocialGoal\Properties\Resources.Designer.cs (line 166)`
- `SocialGoal\Properties\Resources.Designer.cs (line 220)`
- `SocialGoal\ViewModels\ChangePasswordFormModel.cs (line 23)`
- `SocialGoal\ViewModels\ChangePasswordFormModel.cs (line 13)`
- `SocialGoal\ViewModels\ChangePasswordFormModel.cs (line 19)`
- `SocialGoal\ViewModels\ChangePasswordFormModel.cs (line 24)`
- `SocialGoal\ViewModels\ChangePasswordFormModel.cs (line 24)`
- `SocialGoal\ViewModels\UserFormModel.cs (line 39)`
- `SocialGoal\ViewModels\UserFormModel.cs (line 40)`
- `SocialGoal\ViewModels\UserFormModel.cs (line 35)`
- `SocialGoal\ViewModels\UserFormModel.cs (line 40)`
- `SocialGoal\ViewModels\UserFormModel.cs (line 56)`

</details>

<details id="MachineKey_dependency_is_detected">
<summary><b>MachineKey dependency is detected</b> — affected files</summary>

- `SocialGoal.Web.Core\Authentication\DefaultFormsAuthentication.cs (line 40)`
- `SocialGoal.Web.Core\Authentication\DefaultFormsAuthentication.cs (line 22)`
- `SocialGoal.Web.Core\Authentication\DefaultFormsAuthentication.cs (line 27)`

</details>

<details id="Connection_strings_without_configuration_builders_detected">
<summary><b>Connection strings without configuration builders detected</b> — affected files</summary>

- `SocialGoal\Web.config`
- `SocialGoal\Web.config`

</details>

<details id="Static_content_detected">
<summary><b>Static content detected</b> — affected files</summary>

- `SocialGoal\SocialGoal.Web.csproj`

</details>

<details id="System_Data_SqlClient_dependency_detected">
<summary><b>System.Data.SqlClient dependency detected</b> — affected files</summary>

- `SocialGoal\Web.config`

</details>

<details id="Synchronous_API_usage_detected">
<summary><b>Synchronous API usage detected</b> — affected files</summary>

- `SocialGoal\Controllers\AccountController.cs (line 464)`

</details>

## Security Issues

> **Note:** These issues were generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

| Issue Name | Criticality | Story Points | Files |
|------------|-------------|--------------|-------|
| CWE-434: Unrestricted Upload of File with Dangerous Type | Mandatory | 8 | [1](#CWE-434_Unrestricted_Upload_of_File_with_Dangerous_Type) |
| CVE-2026-32933: AutoMapper Vulnerable to Denial of Service (DoS) via Uncontrolled Recursion | Mandatory | 1 | [3](#CVE-2026-32933_AutoMapper_Vulnerable_to_Denial_of_Service_DoS_via_Uncontrolled_Recursion) |
| CVE-2023-33170: Microsoft Security Advisory CVE-2023-33170: .NET Security Feature Bypass Vulnerability | Mandatory | 1 | [1](#CVE-2023-33170_Microsoft_Security_Advisory_CVE-2023-33170_NET_Security_Feature_Bypass_Vulnerability) |
| CVE-2022-29117: .NET Denial of Service Vulnerability | Mandatory | 1 | [3](#CVE-2022-29117_NET_Denial_of_Service_Vulnerability) |
| CVE-2020-1045: Cookie parsing failure in Microsoft.Owin | Mandatory | 1 | [2](#CVE-2020-1045_Cookie_parsing_failure_in_Microsoft_Owin) |
| CVE-2021-21252: Regular Expression Denial of Service in jquery-validation | Mandatory | 1 | [1](#CVE-2021-21252_Regular_Expression_Denial_of_Service_in_jquery-validation) |
| CVE-2024-21907: Improper Handling of Exceptional Conditions in Newtonsoft.Json | Mandatory | 1 | [1](#CVE-2024-21907_Improper_Handling_of_Exceptional_Conditions_in_Newtonsoft_Json) |
| CWE-772: Missing Release of Resource after Effective Lifetime | Potential | 3 | [1](#CWE-772_Missing_Release_of_Resource_after_Effective_Lifetime) |
| CWE-775: Missing Release of File Descriptor or Handle after Effective Lifetime | Potential | 3 | [1](#CWE-775_Missing_Release_of_File_Descriptor_or_Handle_after_Effective_Lifetime) |
| CWE-778: Insufficient Logging | Potential | 3 | [1](#CWE-778_Insufficient_Logging) |
| CWE-732: Incorrect Permission Assignment for Critical Resource | Optional | 5 | [1](#CWE-732_Incorrect_Permission_Assignment_for_Critical_Resource) |

### Security Issue Details

<details id="CWE-434_Unrestricted_Upload_of_File_with_Dangerous_Type">
<summary><b>CWE-434: Unrestricted Upload of File with Dangerous Type</b> — affected files</summary>

- `SocialGoal/Controllers/AccountController.cs`

</details>

<details id="CVE-2026-32933_AutoMapper_Vulnerable_to_Denial_of_Service_DoS_via_Uncontrolled_Recursion">
<summary><b>CVE-2026-32933: AutoMapper Vulnerable to Denial of Service (DoS) via Uncontrolled Recursion</b> — affected files</summary>

- `SocialGoal/packages.config:6`
- `SocialGoal.Tests/packages.config:3`
- `SocialGoal.Web.Core/packages.config:3`

</details>

<details id="CVE-2023-33170_Microsoft_Security_Advisory_CVE-2023-33170_NET_Security_Feature_Bypass_Vulnerability">
<summary><b>CVE-2023-33170: Microsoft Security Advisory CVE-2023-33170: .NET Security Feature Bypass Vulnerability</b> — affected files</summary>

- `SocialGoal/packages.config:15`

</details>

<details id="CVE-2022-29117_NET_Denial_of_Service_Vulnerability">
<summary><b>CVE-2022-29117: .NET Denial of Service Vulnerability</b> — affected files</summary>

- `SocialGoal/packages.config:24`
- `SocialGoal/packages.config:21`
- `SocialGoal.Tests/packages.config:7`

</details>

<details id="CVE-2020-1045_Cookie_parsing_failure_in_Microsoft_Owin">
<summary><b>CVE-2020-1045: Cookie parsing failure in Microsoft.Owin</b> — affected files</summary>

- `SocialGoal/packages.config:21`
- `SocialGoal.Tests/packages.config:7`

</details>

<details id="CVE-2021-21252_Regular_Expression_Denial_of_Service_in_jquery-validation">
<summary><b>CVE-2021-21252: Regular Expression Denial of Service in jquery-validation</b> — affected files</summary>

- `SocialGoal/packages.config:12`

</details>

<details id="CVE-2024-21907_Improper_Handling_of_Exceptional_Conditions_in_Newtonsoft_Json">
<summary><b>CVE-2024-21907: Improper Handling of Exceptional Conditions in Newtonsoft.Json</b> — affected files</summary>

- `SocialGoal/packages.config:33`

</details>

<details id="CWE-772_Missing_Release_of_Resource_after_Effective_Lifetime">
<summary><b>CWE-772: Missing Release of Resource after Effective Lifetime</b> — affected files</summary>

- `SocialGoal/Controllers/AccountController.cs`

</details>

<details id="CWE-775_Missing_Release_of_File_Descriptor_or_Handle_after_Effective_Lifetime">
<summary><b>CWE-775: Missing Release of File Descriptor or Handle after Effective Lifetime</b> — affected files</summary>

- `SocialGoal/Controllers/AccountController.cs`

</details>

<details id="CWE-778_Insufficient_Logging">
<summary><b>CWE-778: Insufficient Logging</b> — affected files</summary>

- `SocialGoal/Controllers/AccountController.cs`

</details>

<details id="CWE-732_Incorrect_Permission_Assignment_for_Critical_Resource">
<summary><b>CWE-732: Incorrect Permission Assignment for Critical Resource</b> — affected files</summary>

- `SocialGoal/Web.config`

</details>

---

## Codebase Insights

> **Note:** These documents are generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

> **Codebase Insights aren't available yet.**
>
> These documents are generated when assessment runs with **Full analysis** coverage. Re-run the assessment and set `analysisCoverage: full` to enable them.

[Share feedback](https://aka.ms/ghcp-appmod/feedback)
