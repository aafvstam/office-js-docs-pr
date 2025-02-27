---
title: Grant administrator consent to the add-in
description: 'Learn how to grant administrator consent to your add-in'
ms.date: 01/25/2022
ms.localizationpriority: medium
---

# Grant administrator consent to the add-in

> [!NOTE]
> This procedure is only needed when you're developing the add-in. When your production add-in is deployed to AppSource or the Microsoft 365 admin center, users will individually trust it or an admin will consent for the organization at installation.

Carry out this procedure *after* you have [registered the add-in](../develop/register-sso-add-in-aad-v2.md).

1. Browse to the [Azure portal - App registrations](https://go.microsoft.com/fwlink/?linkid=2083908) page to view your app registration.

1. Sign in with the ***admin*** credentials to your Microsoft 365 tenancy. For example, MyName@contoso.onmicrosoft.com.

1. Select the app with display name **$ADD-IN-NAME$**.

1. On the **$ADD-IN-NAME$** page, select **API permissions** then, under the **Configured permissions** section, choose **Grant admin consent for [tenant name]**. Select **Yes** for the confirmation that appears.

> [!NOTE]
> We recommend this procedure as a best practice if you're using a [Microsoft 365 developer account](https://developer.microsoft.com/microsoft-365/dev-program). However, if you prefer, it's possible to sideload an SSO add-in under development and prompt the user with a consent form. For more information, see [Sideload on Windows](../testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins.md) and [Sideload on Office on the web](../testing/sideload-office-add-ins-for-testing.md).
