---
title: Sideload Office Add-ins on iPad and Mac for testing
description: 'Test your Office Add-in on iPad and Mac by sideloading.'
ms.date: 09/24/2021
ms.localizationpriority: medium
---

# Sideload Office Add-ins on iPad and Mac for testing

To see how your add-in will run in Office on iOS, you can sideload your add-in's manifest onto an iPad using iTunes, or sideload your add-in's manifest directly in Office on Mac. This action won't enable you to set breakpoints and debug your add-in's code while it's running, but you can see how it behaves and verify that the UI is usable and rendering appropriately.

> [!NOTE]
> To sideload an Outlook add-in, see [Sideload Outlook add-ins for testing](../outlook/sideload-outlook-add-ins-for-testing.md).

## Prerequisites for Office on iOS

- A Windows or Mac computer with [iTunes](https://www.apple.com/itunes/download/) installed.
  > [!IMPORTANT]
  > If you're running macOS Catalina, [iTunes is no longer available](https://support.apple.com/HT210200) so you should follow the instructions in the section [Sideload an add-in on Excel or Word on iPad using macOS Catalina](#sideload-an-add-in-on-excel-or-word-on-ipad-using-macos-catalina) later in this article.

- An iPad running iOS 8.2 or later with [Excel](https://apps.apple.com/app/microsoft-excel/id586683407) or [Word](https://apps.apple.com/app/microsoft-word/id586447913) installed, and a sync cable.

- The manifest .xml file for the add-in you want to test.

## Prerequisites for Office on Mac

- A Mac running OS X v10.10 "Yosemite" or later with [Office on Mac](https://products.office.com/buy/compare-microsoft-office-products?tab=omac) installed.

- Word on Mac version 15.18 (160109).

- Excel on Mac version 15.19 (160206).

- PowerPoint on Mac version 15.24 (160614)

- The manifest .xml file for the add-in you want to test.

## Sideload an add-in on Excel or Word on iPad using iTunes

1. Use a sync cable to connect your iPad to your computer. If you're connecting the iPad to your computer for the first time, you'll be prompted with **Trust This Computer?**. Choose **Trust** to continue.

2. In iTunes, choose the **iPad** icon below the menu bar.

3. Under **Settings** on the left side of iTunes, choose **Apps**.

4. On the right side of iTunes, scroll down to **File Sharing**, and then choose **Excel** or **Word** in the **Add-ins** column.

5. At the bottom of the **Excel** or **Word Documents** column, choose **Add File**, and then select the manifest .xml file of the add-in you want to sideload.

6. Open the Excel or Word app on your iPad. If the Excel or Word app is already running, choose the **Home** button, and then close and restart the app.

7. Open a document.

8. Choose **Add-ins** on the **Insert** tab. (On the **Insert** tab, you may need to scroll horizontally until you see the **Add-ins** button.) Your sideloaded add-in is available to insert under the **Developer** heading in the **Add-ins** UI.

    ![Insert Add-ins in the Excel app.](../images/excel-insert-add-in.png)

## Sideload an add-in on Excel or Word on iPad using macOS Catalina

> [!IMPORTANT]
> With the introduction of macOS Catalina, [Apple discontinued iTunes on Mac](https://support.apple.com/HT210200) and integrated functionality required to sideload apps into **Finder**.

1. Use a sync cable to connect your iPad to your computer. If you're connecting the iPad to your computer for the first time, you'll be prompted with **Trust This Computer?**. Choose **Trust** to continue. You may also be asked if this is a new iPad or if you're restoring one.

2. In Finder, under **Locations**, choose the **iPad** icon below the menu bar.

3. On the top of the Finder window, click on **Files**, and then locate **Excel** or **Word**.

4. From a different Finder window, drag and drop the manifest.xml file of the add-in you want to side load onto the **Excel** or **Word** file in the first Finder window.

5. Open the Excel or Word app on your iPad. If the Excel or Word app is already running, choose the **Home** button, and then close and restart the app.

6. Open a document.

7. Choose **Add-ins** on the **Insert** tab. (On the **Insert** tab, you may need to scroll horizontally until you see the **Add-ins** button.) Your sideloaded add-in is available to insert under the **Developer** heading in the **Add-ins** UI.

    ![Insert Add-ins in the Excel app.](../images/excel-insert-add-in.png)

## Sideload an add-in in Office on Mac

1. Open **Terminal** and go to one of the following folders where you'll save your add-in's manifest file. If the `wef` folder doesn't exist on your computer, create it.

    - For Word:  `/Users/<username>/Library/Containers/com.microsoft.Word/Data/Documents/wef`
    - For Excel:  `/Users/<username>/Library/Containers/com.microsoft.Excel/Data/Documents/wef`
    - For PowerPoint: `/Users/<username>/Library/Containers/com.microsoft.Powerpoint/Data/Documents/wef`

2. Open the folder in **Finder** using the command `open .` (including the period or dot). Copy your add-in's manifest file to this folder.

    ![Wef folder in Office on Mac.](../images/all-my-files.png)

3. Open Word, and then open a document. Restart Word if it's already running.

4. In Word, choose **Insert** > **Add-ins** > **My Add-ins** (drop-down menu), and then choose your add-in.

    ![My Add-ins in Office on Mac.](../images/my-add-ins-wikipedia.png)

    > [!IMPORTANT]
    > Sideloaded add-ins will not show up in the My Add-ins dialog box. They are only visible within the drop-down menu (small down-arrow to the right of My Add-ins on the **Insert** tab). Sideloaded add-ins are listed under the **Developer Add-ins** heading in this menu.

5. Verify that your add-in is displayed in Word.

    ![Office Add-in displayed in Office on Mac.](../images/lorem-ipsum-wikipedia.png)

## Remove a sideloaded add-in

You can remove a previously sideloaded add-in by clearing the Office cache on your computer. Details on how to clear the cache for each platform and application can be found in the article [Clear the Office cache](clear-cache.md).

## See also

- [Debug Office Add-ins on a Mac](debug-office-add-ins-on-ipad-and-mac.md)
- [Sideload Outlook add-ins for testing](../outlook/sideload-outlook-add-ins-for-testing.md)
