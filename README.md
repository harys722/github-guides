<div align="center">
    <img src="https://gh-guides.rweb.site/media/logo.png" alt="Logo" width="120" height="120" :no-zoom>


  <h1 align="center">GitHub Guides</h1>

  <p align="center">
    Learn more about GitHub &amp; GitHub pages as a developer.
    <br />
    <br />
    ⭐ <a href="https://github.com/harys722/github-guides">Star Repository</a>
    &bull;
    🍴 <a href="https://github.com/harys722/github-guides/">Fork Repository</a>
  </p>
</div>

# Table of Contents
- [Welcome to GitHub Guides](#welcome-to-github-guides)
- [Discord Domain Connection](#discord-domain-connection)
- [Bluesky Custom Handle](#bluesky-custom-handle)
- [GitHub Notifications on Discord](#github-notifications-on-discord)

# Welcome to GitHub Guides
Hey user, welcome to GitHub Guides! Here we'll share practical, step-by-step tutorials and helpful resources on topics. We've got practical tips and resources on GitHub Pages, Discord domain connections, Bluesky custom handles, and GitHub notifications on Discord. Learn how to setup them.

## Discord Domain Connection
This guide will walk you through the process of connecting your username.github.io domain to your Discord profile.

### Get your verification string

1. Open your Discord app and press **Settings**.

   ![](https://harys722.github.io/github-guides/media/discord/step_1.png)

2. Open the **Connections** section.

   ![](https://harys722.github.io/github-guides/media/discord/step_2.png)

3. Press the **View more** button.

   ![](https://harys722.github.io/github-guides/media/discord/step_3.png)

4. Click on the domain button (the globe icon).

   ![](https://harys722.github.io/github-guides/media/discord/step_4.png)

5. In the field that appears type your username.github.io domain name and click **Next**. (e.g. `your-username.github.io`).

   ![](https://harys722.github.io/github-guides/media/discord/step_5.png)

6. You'll see the **Verify using HTTPS** option near to Verify button, press it.

   ![](https://harys722.github.io/github-guides/media/discord/step_6.png)

7. Copy the verification string.

   ![](https://harys722.github.io/github-guides/media/discord/step_7.png)


### Configuration
Now that you have the Discord verification TXT string, you need to fork this [repository](https://github.com/harys722/.well-known/). After forking this repository, go to `discord` file and remove everything and then paste your Discord verification string there. Once you paste it, commit the changes to save the file. After doing all these steps, repeat steps 1-5 and press the verify button. If it shows an error like `Unable to verify your domain`, try waiting a few minutes (sometimes up to 24 hours) as the records may not have propagated yet. It usually takes less than 2 minutes.

You can also create your own repository instead of forking this [repository](https://github.com/harys722/.well-known/). To create your own repository, read through GitHub's official guide [Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository). The repository name **must** be `. well-known` and must contain the `discord` file with only your Discord verification TXT string content, otherwise the setup will not work properly.

Once you have created the repository and configured everything, now you just need to enable **GitHub Pages**, for that, go to Settings -> Pages -> Branch -> Main -> Save and you are ready to go.

After all, now that your GitHub domain is connected to your Discord profile, shine up your Discord profile with this domain and don't forget to star this repository. 😉

## Bluesky Custom Handle
This guide will walk you through the process of setting up your custom username.github.io handle in your Bluesky profile.

### Get your verification string

1. Open your Bluesky app and go to your profile **Settings**.

   ![](https://harys722.github.io/github-guides/media/bsky/step_1.png)

2. Open the **Accounts** page.

   ![](https://harys722.github.io/github-guides/media/bsky/step_2.png)

3. Go to the **@ Handle** settings.

   ![](https://harys722.github.io/github-guides/media/bsky/step_3.png)

4. Click on the "I have my own domain" button.

   ![](https://harys722.github.io/github-guides/media/bsky/step_4.png)

5. **Enter** your github.io domain name in the text input and then click on **No DNS Panel**. (e.g. `your-username.github.io`).

   ![](https://harys722.github.io/github-guides/media/bsky/step_5.png)

6. **Copy** the Bluesky verification string.

   ![](https://harys722.github.io/github-guides/media/bsky/step_6.png)


### Configuration
This setup will remain the same as the Discord domain connection guide, but we will mention it again here to prevent incomprehensible issues. Now that you have the Bluesky verification TXT string, you need to fork this [repository](https://github.com/harys722/.well-known/). After forking this repository, go to this `atproto-did` and remove everything and then paste your Bluesky verification string there. Once you paste it, commit the changes to save the file. After doing all these steps, repeat steps 1-5 and press the `Verify DNS Record` button. If it shows an error like `Failed to verify handle. Please try again.`, try waiting a few minutes (sometimes up to 24 hours) as the records may not have propagated yet.

You can also create your own repository instead of forking this [repository](https://github.com/harys722/.well-known/). To create your own repository, read through GitHub's official guide [Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository). The repository name **must** be `. well-known` and must contain the `atproto-did` file with only your Bluesky verification TXT string content, otherwise the setup will not work properly.

Once you have created the repository and configured everything, now you just need to enable **GitHub Pages**, for that, go to Settings -> Pages -> Branch -> Main -> Save and you are ready to go.

After all, now that you have setup your custom handle in Bluesky, let your friends know this new handle and don't forget to star this repository. 😉

## GitHub Notifications on Discord
Want to get instant updates on your GitHub projects in your Discord server? This guide shows you how to set up GitHub webhooks to send notifications of new issues, pull requests or any push straight to your Discord channel. It's easy to do and super helpful for keeping everyone in the know.

### Create the Discord webhook
1. Open your Discord app and go to the **Settings** of specific channel in your Discord where you want to receive notifications.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_1.png)

2. Navigate to **Integrations** section and create a new webhook.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_2.png)

3. After creating the webhook, copy its URL and save it for future use.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_3.png)

### Add Discord webhook to GitHub repository

4. Now go to **Settings** of your desired GitHub repository for which you want to receive action notifications. 

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_4.png)

5. Paste the webhook URL that you copied from Discord earlier into the Payload URL and make sure to add `/github` at the end otherwise it won't work. Set the content type to `application/json` and choose the events that will trigger the webhook.

   Once you're done, you may click the **Add webhook** green button below to complete the process.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_5.png)

6. If you have configured it correctly, you should get a response similar to this image.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_6.png)

### Testing the webhook

7. To test a webhook, you can take a simple action such as creating an issue or a pull request. You can also simply create or add some files to your repository.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_7.png)

8. Once you make some changes to your GitHub repository, you should immediately receive a notification on the Discord channel you configured the webhook on.

   ![](https://harys722.github.io/github-guides/media/discord/github-notify/step_8.png)

Anyway, now that you've set up your GitHub notifications in your Discord server, let's test further by creating files or issues to make sure it works properly and don't forget to star this repository. If you have any questions or need help setting it up, don't hesitate to open an issue in our GitHub repository or ask in the discussions. 😉

---

<div align="center">
  <p>&copy 2025 harys722. All rights reserved. </p>
</div>
