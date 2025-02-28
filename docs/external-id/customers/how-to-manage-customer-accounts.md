---
title: Add and manage customer accounts
description: Learn how to add and manage customer accounts in Microsoft Entra ID for customers.
 
author: msmimart
manager: celestedg
ms.service: entra-external-id
 
ms.subservice: customers
ms.topic: how-to
ms.date: 07/12/2023
ms.author: mimart
ms.custom: it-pro

---
# Add and manage customer accounts (preview)

There might be scenarios in which you want to manually create customer accounts in your Microsoft Entra customer tenant. Although customer accounts are most commonly created when users sign up to use one of your applications, you can create them programmatically and by using the Microsoft Entra admin center. This article focuses on the Microsoft Entra admin center method of user creation and deletion.

To add or delete users, your account must be assigned the *User administrator* or *Global administrator* role.

## Prerequisites

- If you haven't already created your own Microsoft Entra customer tenant, create one now.
- Understand user accounts in Microsoft Entra ID for customers.
- Understand user roles to control resource access.

[!INCLUDE [preview-alert](../customers/includes/preview-alert/preview-alert-ciam.md)]

## Create a customer account

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) with Global Administrator or Privileged Role Administrator permissions.
1. If you have access to multiple tenants, use the **Settings** icon :::image type="icon" source="media/common/admin-center-settings-icon.png" border="false"::: in the top menu to switch to your customer tenant from the **Directories + subscriptions** menu.
1. Browse to **Identity** > **Users** > **All users**.
1. Select **New user** > **Create new user**. 
1. Select **Create a customer**.
1. Under **Identity**, select a **Sign in method** and enter the **Value**:
   - **Email**: Enter the customer's email address, which will become their sign-in name.
   - **User Name**: Enter a user name for the customer.
1. Next to **Name** (required), enter the first and last name of the customer (for example, *Mary Parker*).
1. Under **Settings**, use the yes or no toggle to set **Block sign in**, and the select the user's primary location in the **Usage location** list. Then enter the customer's **First name** and **Last name**.
1. Copy the autogenerated password provided in the **Password** box. Give this password to the user to sign in for the first time.
1. Select **Create**.

Unless you've selected **Block sign in**, the user can now sign in using the sign in method (email or username) that you specified.

## Reset a customer's password

As an administrator, you can reset a user's password, if the user forgets their password. When you reset the user's password, a temporary password is autogenerated for the user. The temporary password never expires. The next time the user signs in, the password will still work, regardless how much time has passed since the temporary password was generated. Then user must reset password to a permanent one. 

To reset a customer's password:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) with Global Administrator or Privileged Role Administrator permissions.
1. If you have access to multiple tenants, use the **Settings** icon :::image type="icon" source="media/common/admin-center-settings-icon.png" border="false"::: in the top menu to switch to your customer tenant from the **Directories + subscriptions** menu.
1. Browse to **Identity** > **Users** > **All users**.
1. Search for and select the user that needs the reset, and then select **Reset Password**.
1. In the **Reset password** page, select **Reset password**.
1. Copy the password and give it to the user. The user will be required to change the password during the next sign-in process.

## Delete a customer account

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) with Global Administrator or Privileged Role Administrator permissions.
1. If you have access to multiple tenants, use the **Settings** icon :::image type="icon" source="media/common/admin-center-settings-icon.png" border="false"::: in the top menu to switch to your customer tenant from the **Directories + subscriptions** menu.
1. Browse to **Identity** > **Users** > **All users**.
1. Search for and select the user to delete.
1. Select **Delete**, and then **Yes** to confirm the deletion.

For details about restoring a user within the first 30 days after deletion, or for permanently deleting a user, see [Restore or remove a recently deleted user using Microsoft Entra ID](~/fundamentals/users-restore.md).
