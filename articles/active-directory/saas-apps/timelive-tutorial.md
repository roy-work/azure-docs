---
title: 'Tutorial: Azure Active Directory integration with TimeLive | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and TimeLive.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 03/27/2019
ms.author: jeedes
---
# Tutorial: Azure Active Directory integration with TimeLive

In this tutorial, you learn how to integrate TimeLive with Azure Active Directory (Azure AD).
Integrating TimeLive with Azure AD provides you with the following benefits:

* You can control in Azure AD who has access to TimeLive.
* You can enable your users to be automatically signed-in to TimeLive (Single Sign-On) with their Azure AD accounts.
* You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).
If you don't have an Azure subscription, [create a free account](https://azure.microsoft.com/free/) before you begin.

## Prerequisites

To configure Azure AD integration with TimeLive, you need the following items:

* An Azure AD subscription. If you don't have an Azure AD environment, you can get one-month trial [here](https://azure.microsoft.com/pricing/free-trial/)
* TimeLive single sign-on enabled subscription

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* TimeLive supports **SP** initiated SSO

* TimeLive supports **Just In Time** user provisioning

## Adding TimeLive from the gallery

To configure the integration of TimeLive into Azure AD, you need to add TimeLive from the gallery to your list of managed SaaS apps.

**To add TimeLive from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon.

	![The Azure Active Directory button](common/select-azuread.png)

2. Navigate to **Enterprise Applications** and then select the **All Applications** option.

	![The Enterprise applications blade](common/enterprise-applications.png)

3. To add new application, click **New application** button on the top of dialog.

	![The New application button](common/add-new-app.png)

4. In the search box, type **TimeLive**, select **TimeLive** from result panel then click **Add** button to add the application.

	 ![TimeLive in the results list](common/search-new-app.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with TimeLive based on a test user called **Britta Simon**.
For single sign-on to work, a link relationship between an Azure AD user and the related user in TimeLive needs to be established.

To configure and test Azure AD single sign-on with TimeLive, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Configure TimeLive Single Sign-On](#configure-timelive-single-sign-on)** - to configure the Single Sign-On settings on application side.
3. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Create TimeLive test user](#create-timelive-test-user)** - to have a counterpart of Britta Simon in TimeLive that is linked to the Azure AD representation of user.
6. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal.

To configure Azure AD single sign-on with TimeLive, perform the following steps:

1. In the [Azure portal](https://portal.azure.com/), on the **TimeLive** application integration page, select **Single sign-on**.

    ![Configure single sign-on link](common/select-sso.png)

2. On the **Select a Single sign-on method** dialog, select **SAML/WS-Fed** mode to enable single sign-on.

    ![Single sign-on select mode](common/select-saml-option.png)

3. On the **Set up Single Sign-On with SAML** page, click **Edit** icon to open **Basic SAML Configuration** dialog.

	![Edit Basic SAML Configuration](common/edit-urls.png)

4. On the **Basic SAML Configuration** section, perform the following steps:

    ![TimeLive Domain and URLs single sign-on information](common/sp-identifier.png)

	a. In the **Sign on URL** text box, type a URL using the following pattern:
    `https://<domainname>.livetecs.com/`

    b. In the **Identifier (Entity ID)** text box, type a URL using the following pattern:
    `https://<domainname>.livetecs.com/`

	> [!NOTE]
	> These values are not real. Update these values with the actual Sign on URL and Identifier. Contact [TimeLive Client support team](mailto:support@livetecs.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

5. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

6. On the **Set up TimeLive** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

	a. Login URL

	b. Azure AD Identifier

	c. Logout URL

### Configure TimeLive Single Sign-On

1. In a different web browser window, sign in to your TimeLive company site as an administrator.

2. Select **Preferences** under **Admin Options**.

	![Screenshot shows the Admin Options with Preferences selected.](./media/timelive-tutorial/configure1.png)

3. In the **Application Preference** section, perform the following steps:
	
	![Screenshot shows the Application Preference section where you can enter the values described.](./media/timelive-tutorial/configure2.png)

	a. Select **Security** tab.

	b. Check **Enable Single Sign On (SSO)** checkbox.

	c. Select **SAML** from the drop down menu with heading **Sign in using Single Sign-On (SSO) with**.

	d. In the **SAML SSO URL**, Paste **Login URL** value which you have copied form the Azure portal.

	e. In the **Remote logout URL**, Paste **Logout URL** value which you have copied form the Azure portal.

	f. Open the downloaded **base-64 encoded certificate** from Azure portal in Notepad, copy the content, and then paste it into the **X.509 Certificate** textbox.

	g. Click **Update**.

### Create an Azure AD test user 

The objective of this section is to create a test user in the Azure portal called Britta Simon.

1. In the Azure portal, in the left pane, select **Azure Active Directory**, select **Users**, and then select **All users**.

    ![The "Users and groups" and "All users" links](common/users.png)

2. Select **New user** at the top of the screen.

    ![New user Button](common/new-user.png)

3. In the User properties, perform the following steps.

    ![The User dialog box](common/user-properties.png)

    a. In the **Name** field enter **BrittaSimon**.
  
    b. In the **User name** field type brittasimon@yourcompanydomain.extension. For example, BrittaSimon@contoso.com

    c. Select **Show password** check box, and then write down the value that's displayed in the Password box.

    d. Click **Create**.

### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to TimeLive.

1. In the Azure portal, select **Enterprise Applications**, select **All applications**, then select **TimeLive**.

	![Enterprise applications blade](common/enterprise-applications.png)

2. In the applications list, select **TimeLive**.

	![The TimeLive link in the Applications list](common/all-applications.png)

3. In the menu on the left, select **Users and groups**.

    ![The "Users and groups" link](common/users-groups-blade.png)

4. Click the **Add user** button, then select **Users and groups** in the **Add Assignment** dialog.

    ![The Add Assignment pane](common/add-assign-user.png)

5. In the **Users and groups** dialog select **Britta Simon** in the Users list, then click the **Select** button at the bottom of the screen.

6. If you are expecting any role value in the SAML assertion then in the **Select Role** dialog select the appropriate role for the user from the list, then click the **Select** button at the bottom of the screen.

7. In the **Add Assignment** dialog click the **Assign** button.

### Create TimeLive test user

In this section, a user called Britta Simon is created in TimeLive. TimeLive supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in TimeLive, a new one is created after authentication.

### Test single sign-on 

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the TimeLive tile in the Access Panel, you should be automatically signed in to the TimeLive for which you set up SSO. For more information about the Access Panel, see [Introduction to the Access Panel](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Additional Resources

- [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](./tutorial-list.md)

- [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)

- [What is Conditional Access in Azure Active Directory?](../conditional-access/overview.md)