---
layout: page
title: FAQ
permalink: /faq/
accordion:
  - title: What is Möbius Sync?
    content: Möbius Sync is a third-party iOS app for Syncthing.
  - title: What is Syncthing?
    content: >
      From the [syncthing.net](https://www.syncthing.net/) website:
      
      > Syncthing is a continuous file synchronization program. It synchronizes files between two or more computers in real time, safely protected from prying eyes. Your data is your data alone and you deserve to choose where it is stored, whether it is shared with some third party, and how it's transmitted over the internet.
      
      
      **Möbius Sync** adds iOS (iPhone and iPad) to the list of supported platforms, which already includes Windows, macOS, Linux, Android and various UNIX and NAS platforms. See <https://syncthing.net/downloads/> and <https://docs.syncthing.net/users/contrib.html>.
  - title: Why use Möbius Sync and Syncthing?
    content: >
      - Avoid paying cloud providers for storage - sync between your own devices directly.

      - Use an open and sync protocol and sync engine, with many advanced features and high configurability.
  - title: What can and cannot Möbius Sync do?
    content: >
      **Möbius Sync** can sync files between multiple remote devices and multiple folders. The included Syncthing engine is very powerful and highly configurable.

      **Möbius Sync** is restricted by iOS security and performance features in a few ways:

      1. No iOS app can run continuously in the background. This means that **Möbius Sync** can only connect to other devices whilst the app is open, for a short time thereafter, and whenever it is triggered to run briefly in the background. See *Background sync*.

      2. iOS apps cannot access each others' files. This means you will need to copy files in and out of Syncthing using the Apple *Files* app. See *Accessing my synced files*.

      3. Photos and videos are not stored as files under iOS. This means you cannot sync photos and videos directly using Syncthing. See *Syncing my photos and videos* for future plans.
  - title: Background sync
    content: Apple iOS restricts apps from running continuously in the background, but apps can run for short times sporadically. **Möbius Sync** uses various methods to invoke background behaviour, and this is an area to be enhanced over time.
  - title: Accessing my synced files
    content: >
      To access files that have been synced onto your iPhone or iPad from another device:

      - Select *Open Folder* button to open the folder in the Apple *Files* app

        - View/preview/edit your files where supported directly within *Files*

        - Click the *share* icon to print, or open/export files in other installed iOS apps.

      To store files from other iOS apps into a synced folder:

        - Use the relevant app's *Open In* or *Share* or *Export* feature to open the standard iOS sharing popup

          - Select *Save to Files*

            - Browse to the appropriate folder *On My iPhone* or *On My iPad*, then *Möbius Sync*, then the shared folder

              - Rename the file if necessary

              - Create a New Folder if necessary

              - Hit *Save*

      For more details on the *Files* app, see: <https://support.apple.com/en-us/HT206481>
  - title: Syncing my photos and videos
    content: >
      Because iOS manages photos and videos within the Photo Library, they are not accessible to Syncthing to synchronise directly as files.


      We understand that the ability to synchronise photos and videos captured on your iPhone or iPad to other Syncthing-enabled devices is a highly desirable feature and is planned for the future.


      Two-way sync of photos and videos is even more difficult and is further down the roadmap.
  - title: Is Möbius Sync open source?
    content: >
      The Syncthing core of **Möbius Sync** is open source software (OSS), published under MPL-2.0. Accordingly, modifications to Syncthing for **Möbius Sync** under iOS are published under MPL-2.0 at: <https://github.com/MobiusSync/syncthing/>


      The Möbius Sync iOS app is not open source at this time.
  - title: Paying for Möbius Sync - unlimited file sync
    anchor: unlimited-files
    content: >
      **Möbius Sync** can be used free of payment up to total file storage of **20MB**:


      If you exceed this limit, Syncthing will be disabled, giving you two options:

        - On completing the one-time in-app purchase for *Unlimited file sync*, Syncthing will be re-enabled and any limits will be removed.

        - If you wish to continue using **Möbius Sync** for free:

          - Use the Apple *Files* app to delete any locally-created files beyond the storage limits. **Beware these files may be deleted on your remote device(s) if you do not remove the Syncthing sharing association from the other device(s) beforehand.**

          - If you are trying to share remote folder(s) exceeding 20MB in total, you should remove the sharing of those folder(s) or remove files on the remote device to come within the limit. Note that removing a sharing association does not delete local copies. You may need to use the Apple *Files* app to delete any stray local copies to reduce usage within the free limit.
  - title: Isn't charging for Möbius Sync against the spirit of Syncthing as OSS?
    content: >
      It was a difficult decision to decide to charge for **Möbius Sync,** as we are clearly benefiting from the excellent and significant open-source contributions of the Syncthing authors and community. However we feel this is justified because:

      - An iOS app for Syncthing has been high on many people's wishlist for many years but has not been forthcoming under an open-source model (including with bountysource).

      - We hope that a modest charge to unlock the Möbius Sync feature set will incentivate us to continue working on the product, where nobody has succeeded without revenue until now.

      - Limited **Möbius Sync** usage is available for free.

      - We believe that lack of iOS support has been an impediment to Syncthing vs other competitors, and we hope that offering an (albeit commercial) iOS open will introduce many new users to the Syncthing ecosystem.

      - We have co-operated with the Syncthing community re naming, use of logo etc via the Syncthing forum, and will continue to do so.

      - We plan to contribute back to the Syncthing community when possible, and in method(s) to be decided. You may hold us to account on this.

      - We are amenable to exploring ways to make the **Möbius Sync** source code available to others in a way that does not undermine the commercial incentive to continue support and development.
  - title: Privacy and security
    content: >
      We know that privacy and security are very important factors in choosing for many. We understand the closed-source nature of parts of **Möbius Sync** compromises this in some regard. To mitigate this:

      - We have retained the full Logging and Debug Facilities of Syncthing so you can see that it's behaviour matches other Syncthing platforms.

      - We have avoided analytics and any connections to third-party services so network auditing can confirm that we are not sending your data elsewhere.

      - By avoiding analytics, we do not have the temptation to monetise any data collected about you.

      - We look forward to supporting the imminent end-to-end encryption feature in Syncthing.

      - We are open to exploring ways of releasing source code to interested parties without compromising our commercial incentive to continue development.

      - We would like to hear if there any ways we can make you feel more comfortable.
  - title: Sync topology
    content: >
      **Möbius Sync** is able to participate in networks of one or more other devices running Syncthing on any platform.


      We recommend the most convenient way to use **Möbius Sync** will be to synchronise with at least one other device that is continuously running (i.e. a computer, not a mobile device).


      Syncing between two iOS devices is possible, and will work best when you can open **Möbius Sync** on both device simultaneousy whenever you want them to sync. This is because iOS does not allow us to control when **Möbius Sync** can run in the background, and it is unlikely that two iOS devices will schedule their background activtiy at the same time, in order to be able to sync peer-to-peer.
  - title: Initial setup
    content: >
      We recommend that you initially setup your non-iOS device(s) with Syncthing, then add your iOS devices. It is probably easiest to initaite new connection(s)/share(s) from the iOS side and accept on the other device(s).


      You may need to keep **Möbius Sync** open for a number of minutes while the initial connections and synchronisations are completed.
  - title: Data collection and analytics
    content: >
      **Möbius Sync** does not contain any analytics or data collection, other than that which is inherent in the Apple App Store distribution mechanism. See also *Usage report*.
  - title: Usage report
    content: Syncthing core contains an optional and anonymous Usage Report. This is currently disabled in **Möbius Sync**, although we may add it in future releases.
  - title: Future plans
    content: >
      - Usage report (opt-in)

      - Network data/Wifi network usage control

      - Improving background syncing

      - Better integration with Files

      - Selective sync

      - Photo/video library (Send Only)

      - Photo/video library (Send and Receive)


      Feedback on what is important to you is most welcome.
  - title: Syncthing features
    content: >
      We have tried to retain and expose via the Settings GUI all of the Syncthing features, except for those we know will not work. This is because we know Syncthing has some very advanced users.


      Some of the features and settings are complicated and dangerous and may not work with iOS. We have not tested them all. Please don't be upset with us if they don't all work, but do please let us know, so we can update here.
  - title: Backup
    content: >
      **Möbius Sync** is not a backup tool. Syncthing is not a backup tool. **Please back up your data**. We do not take responsibility for data loss.
  - title: iCloud backup
    content: >
      Sync folders under **Möbius Sync** are currently included in your iCloud backup. We hope to make this configurable in future.
  - title: Warning - data usage
    content: >
      **Möbius Sync** currently syncs whenever it runs, and will use Wifi and/or **mobile data**. Data usage may be high. We plan to make this configurable in future.
  - title: Support and bug reporting
    content: >
      You may discuss Syncthing-releated support issues on <https://forum.syncthing.net/> but do not file **Möbius Sync** queries/issues there.


      Issues and queries can be raised at <https://github.com/MobiusSync/MobiusSync/issues>.


      In the future we may set up our own forum.


      Meanwhile, please see the *Contact us* section below.
  - title: How can I help?
    content: >
      If you want to support **Möbius Sync**, you can:

      1. Write a review in the Apple App Store.

      1. Post or tweet about us wherever you can.

      1. Pay for the in-app purchases, even if you don't need them.

      1. [Donate to Syncthing](https://syncthing.net/donations/).

      1. Give us feedback.
  - title: Contact us
    content: >
      Contact us at:

      - On Twitter [@MobiusSync](https://twitter.com/mobiussync)

      - On the [Syncthing forum](https://forum.syncthing.net/), but being mindful that the Syncthing open-source community are not obliged to support our commercial product.

      - On IRC Freenode channels [#syncthing](https://kiwiirc.com/client/irc.freenode.net/#syncthing) or [#mobiussync](https://kiwiirc.com/client/irc.freenode.net/#mobiussync).

      - Via our company [Pickup Infinity](https://www.pickupinfinity.com/contact).
---
{% include accordion.html %}
