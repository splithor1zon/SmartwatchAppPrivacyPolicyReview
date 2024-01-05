***WIP** - Feel free to contribute!*

# Smartwatch App Privacy Policy Review (focused on AI/ML privacy)

## Contents

- [Smartwatch App Privacy Policy Review (focused on AI/ML privacy)](#smartwatch-app-privacy-policy-review-focused-on-aiml-privacy)
  - [Contents](#contents)
  - [Background](#background)
  - [Problem statement](#problem-statement)
  - [Research questions](#research-questions)
  - [Objectives](#objectives)
  - [Scope and limitations](#scope-and-limitations)
- [Privacy policy review](#privacy-policy-review)
    - [Quick result table](#quick-result-table)
    - [Commentary on privacy policies](#commentary-on-privacy-policies)
    - [Fitbit](#fitbit)
    - [Garmin Connect](#garmin-connect)
    - [Apple Health](#apple-health)
    - [Mi Fitness (Xiaomi Wear)](#mi-fitness-xiaomi-wear)
    - [Zepp Life (former Mi Fit)](#zepp-life-former-mi-fit)
    - [Zepp (Amazfit)](#zepp-amazfit)
    - [Huawei Health](#huawei-health)
    - [Samsung Health](#samsung-health)
    - [Whoop](#whoop)
    - [Gadgetbridge - Privacy-oriented open-source project](#gadgetbridge---privacy-oriented-open-source-project)
- [Fitness analytics use-cases](#fitness-analytics-use-cases)
    - [Activity classification](#activity-classification)
    - [Sleep stage classification](#sleep-stage-classification)
    - [Sleep quality score](#sleep-quality-score)
    - [Data abnormality detection](#data-abnormality-detection)
    - [Menstrual cycle tracking](#menstrual-cycle-tracking)
    - [Walking steadiness](#walking-steadiness)
    - [Exercise recommendations](#exercise-recommendations)

## Background

There are many popular fitness tracking apps on the market, usually joined with the purchase of their respective hardware (wearable band, smartwatch). There is also a high probability the reader uses one as well. The dark side of these apps and wearable devices is about information privacy, as society considers medical and biometric data highly sensitive. Fortunately, there are a few examples of privacy-oriented open-source fitness tracker apps. But what happens when we would like to use AI/ML-powered analytics using these data? Use cases for such analytics would be for example sleep quality diagnosis, sleep schedule recommendation, exercise recommendations, health condition risk assessment, etc.

## Problem statement

These analytics rely on processing large quantities of data and the collection of biometric data from users. Usually, these apps also make the consent granting either automatic or obtuse. This goes against the principles of privacy and currently can be mitigated just with an on/off switch. Certainly, these apps are more focused on user-friendliness, but there does not have to be a compromise between user-friendliness and privacy.

## Research questions

1.	What is the current state of privacy policies and consent granting in AI-powered fitness apps today?
1.	What are the currently available and potential use cases for AI/ML-powered analytics in fitness-tracking apps?

## Objectives

1.	Study available AI-powered fitness-tracking apps, including privacy policies, data collection, and available analytics.
1.	Brief study of research papers on novel approaches to fitness-tracking analytics.

## Scope and limitations

The study of available fitness tracking apps would be limited to just the most popular. As we do not possess the devices necessary for some of the apps to work properly, the study will focus mainly on reading through the privacy policies and any privacy related news from the press. Focusing on the privacy aspect of their integration of AI/ML analytics and general data collection.

# Privacy policy review

To stay focused on the topic of biometric data privacy, this section is concerned only about such data. Account data privacy such as name, email, phone number is certainly important, but out of scope of this review. While reading the privacy policies we try to answer these three questions:

1. Is sharing of biometric data optional to use the app?
1. Is the app capable of local data analysis utilizing ML/AI models?
1. Can user opt-out of the service sharing or selling personally identifiable biometric data to third parties?

There should also be a consideration for the potential technical difficulty of implementing fully local analytics or their diminished quality. So while the third question might sound unrelated, we would still like to shed some light on how the corporations handle the data. Specifically, how many copies of the data under various handlers there might be. With the multiplication of the data, the vulnerability to a potential data breach increases. For the users, if nothing else, denying the spread of sensitive biometric data outside the app operator's servers is an essential privacy tool.

## Quick result table

This table represents the scoring of each reviewed app in the scope of the three questions as defined above.

| Q | Fitbit | Garmin | Apple | Xiaomi | Zepp Life | Zepp | Huawei | Samsung | Whoop |
|---|--------|--------|-------|--------|-----------|------|--------|---------|-------|
| 1 | N      | N      | N?    | N      | N         | N    | Y?     | N?      |       |
| 2 | N      | N      | Y     | N      | N         | N    | N      | N       |       |
| 3 | N      | Y      | Y     | N      | N         | N    | Y      | N       |       |
|   |        |        |       |        |           |      |        |         |       |
| = | 0      | 1      | 2.5   | 0      | 0         | 0    | 1.5    | 0.5     |       |

## Commentary on privacy policies

Before we begin with the analyses of selected fitness tracking apps it is important to discuss potential limitations and obstacles.

Most of the privacy policies are not easy to understand, and sometimes it is difficult to ascertain which functionality will be kept after we withdraw our data sharing consent. That is the reason why this table may not reflect reality. Better accuracy would require detailed testing of individual apps, and even forensic analysis of the traffic between the apps and servers. While we tried to verify some surprising claims the app developers made, it was not always possible. Our findings might quickly become obsolete if developers push updates to their apps or privacy policies.

For the users that do not want to read complicated privacy policies, we would like to propose a simple test to determine the app privacy capabilities: If the app is capable of working without internet access, it *could* be a privacy-friendly app. Certainly, the data should be protected by strong encryption locally as well. Important to mention is that if the user denies internet connection to the app, as it is possible to do on operating system level nowadays, they will certainly lose the benefits such as firmware updates, sync/data migration and analytics model improvements. It is also entirely possible that the app will stop working after a certain time.

This review is focused on providing a solution where user's data does not have to leave the device, but user can still benefit from all the internet access benefits. Generally, none of the reviewed app's privacy policies offered completely positive answers to our questions.

## Fitbit

Starting with the first question, if the user chooses to sync the wearable with the app, the data is synced with their servers as well. There is no provision in the privacy policy that allows the user to withdraw consent for the data syncing. Thus, we have to assume that this behavior cannot be disabled. If the user wishes to keep the biometric data local, the only option is to disable syncing between the wearable and the app, which would make the app useless. This is supported by an excerpt from their [privacy policy][010000]:

> When your device syncs with our applications or software, data recorded on your device is transferred from your device to our servers.

As for the second question, there is no mention of local data analysis/processing in the privacy policy nor the marketing materials.

Recently European privacy advocate group ['noyb' has filed][010001] three complaints against Fitbit. This is due to Fitbit forcing users to consent to data transfers outside of EU. Fitbit moreover does not even provide the possibility of withdrawing their consent, the only option is to delete their account, which is against the EU regulation. When reading through the Fitbit privacy policy, Fitbit declares that they will not sell any data, but the data is ultimately shared with contracted third-parties. These third-parties seem like independent companies, so the Fitbit might have limited oversight capabilities over their handling of the data. The privacy policy does not specify which data is shared, so we have to assume any data can be. Due to these concerns, the third question is answered negatively. This is supported by an excerpt from their [privacy policy][010000]:

> We never sell the personal information of our users. We do not share your personal information except in the limited circumstances described below.
>
> ...
>
> We transfer information to our corporate affiliates, service providers, and other partners who process it for us, based on our instructions, and in compliance with this policy and any other appropriate confidentiality and security measures.

It is also important to mention that [Fitbit was acquired by Google][010002] in 2021, and users are currently presented with an option to migrate their Fitbit account to Google. The data would be then governed by Google's privacy policy. In the future it is expected that these two ecosystems will merge under the Google umbrella. Right now, even Google-branded Pixel Watch devices are essentially Fitbit devices that connect to the Fitbit app.

According to the focused metrics of this review, the Fitbit app gets **0/3** score. 

## Garmin Connect

According to the [privacy policy][010100] users are able to disable synchronization of their biometric data to cloud, but the wordage does not suggest that user can use the app with just local data. The specific quote mentions that user is able to use "your device" without upload consent. Which presumably applies to just the wearable device not the app. Indeed, when we searched for user experiences with the app, a [blog post][010101] suggested that the app is just a synchronization client and cloud data viewer, i.e. it cannot show nor analyze local biometric data. Here is the excerpt from the [privacy policy][010100]:

> You can use your device without providing your consent to upload your activities to your account.

Thus, neither the first, nor the second question can be answered positively.

By default, Garmin does not share the biometric data with any third-party and the data does not leave Garmin-owned companies. This opt-in privacy behavior is viewed as welcome by some [privacy researchers][010102]. Moreover, it seems that Garmin is adequately protecting user data, as there was no leak reported. Not even when an extensive [ransomware attack in 2020][010103] on Garmin servers happened. Considering these facts, the third question can be answered positively.

According to the focused metrics of this review, the Garmin app gets **1/3** score. 

## Apple Health

The Apple ecosystem is based around user's Apple ID account, while you can use iPhone without one, it is unclear if Apple Health app will work in such scenario. So let's consider an experience of an ordinary user with linked Apple ID on his device. The user definitely has option to not use the fitness tracking services. Though, it is unclear if user can choose not to share any biometric data with Apple services, but still use local data for fitness tracking and possibly analytics. So let's see what does their [privacy policy][010200] say:

> **Personal Data Apple Collects from You**
>
> ...
>
> *Health Information.* Data relating to the health status of an individual, including data related to one’s physical or mental health or condition. Personal health data also includes data that can be used to make inferences about or detect the health status of an individual.
>
> *Fitness Information.* Details relating to your fitness and exercise information where you choose to share them
>
> ...
>
> You are not required to provide the personal data that we have requested. However, if you choose not to do so, in many cases we will not be able to provide you with our products or services or respond to requests you may have.

Their privacy policy does not answer our first question positively. With this being said, Apple has declared that its iCloud service can work in an end-to-end encryption mode for certain types of data, when user sets up a two-factor authentication. This mode supposedly prevents even Apple to be able to read synchronized data. Health data [is included][010202] in this end-to-end encryption scheme, so even if the user lets their data be synchronized, it should still be protected from sharing and malicious access. This approach is commendable from the privacy perspective, but more transparency would still be appreciated. It is difficult to find any information on which specific types of data are synchronized to iCloud, even if they would be end-to-end encrypted. There is perhaps a possibility to turn off this data synchronization, as explained in [the white paper][010201]:

>You can choose to turn off syncing of Health app data in Settings > Apple ID > iCloud > Health.

When combined with the statements from the privacy policy, this statement is still ambiguous and does not guarantee the functionality of the Apple Health app. Without a testing device, the user is left guessing. Due to these reasons we decided to award apple half a point for the first question.

As for second question, Apple [provides local biometric data processing][010201] for analytics such as Trends & Highlights, resting heart rate, and Cycle Tracking. This way Apple servers do not need to see this data to produce analytics for users. The technology behind this is likely based on federated learning due to the existence of multiple research papers sponsored by Apple concerning privacy in machine learning topics, e.g.:

- [Enforcing Fairness in Private Federated Learning via The Modified Method of Differential Multipliers][010203]
- [Protection Against Reconstruction and Its Applications in Private Federated Learning][010204]
- [Federated Evaluation and Tuning for On-Device Personalization: System Design & Applications][010205]

For the usage of local data analytics and consequently sending less biometric data to Apple servers, the second question can be answered positively.

Third question could be answered positively assuming the biometric data is encrypted and unreadable by Apple.

According to the focused metrics of this review, the Apple Health app gets **2.5/3** score. 

## Mi Fitness (Xiaomi Wear)

This app made by Xiaomi is meant for newer Xiaomi wearable devices. Previous Mi Fit app for older devices got replaced by Zepp Life app managed by Zepp Health Corporation. So by reviewing the [privacy policy][010300] we learn that Xiaomi Wear collects a broad range of biometric data by default. It is not initially clear from the privacy policy, if this data is sent and stored on the servers, but there is no indication that the data is stored only locally as well. Continuing reading the privacy policy, we learn that the user is able to withdraw the consent to data processing, but there is a vague statement that the user can lose access to certain Xiaomi services. Excerpts from the Xiaomi Wear [privacy policy][010300]:

>In the course of your use of our smart wearables, we may collect and record information relating to your exercise, including the number of steps you take, standing activity and duration, exercise mode, cadence, distance covered, exercise time, elevation, heart rate, swim strokes, stroke rate, number of laps, and heartbeat information. In addition, we may collect your personal information, including your nickname, gender, birthday, height and weight.
>
>You may withdraw your consent for the collection, use, and/or disclosure of your personal information in our possession or control by submitting a request.
>
>Please note that your withdrawal of consent could result in certain **legal consequences**. Depending on the extent to which you authorize us to process your personal information, it may mean that you will no longer be able to enjoy the use of Xiaomi products or services. However, any decision on your part to withdraw your consent or authorization will not affect personal information processing previously performed with your permission.

As it is clear, the privacy policy alone is simply insufficient for determining the answer to our question, so we explore further and find an [independent research][010301] into the privacy of a Xiaomi wearable. They noticed similar issue that we had, the privacy policies for these devices are very confusing. There is though [privacy summary available][010302]. In the summary there is a section about privacy in the Xiaomi Wear app. In the data inventory table we can see that the sensitive information - biometric data is indeed transmitted to their servers and is not even encrypted locally. 

The user has the right to withdraw consent, but we have to assume that the user will not be able to use the app using just local data. This is further supported by [users reporting][010303] the inability to use the app without an active internet connection. Consequently, the first question is answered negatively.

We could not find any supportive materials of the app using local data analytics. Moreover, considering the inability of using the app offline, the second question is answered negatively.

In the privacy policy there is no mechanism to opt-out of third-party data transfers. It seems that Xiaomi is using multiple third-party contractors to provide services for their wearable devices. There is also a dangerous statement that user's data can be transferred into different jurisdictions seemingly at the discretion of Xiaomi. This is supported by an excerpt from the privacy policy:

>We may also share your personal information with our Third Party Service Providers and business partners, therefore, your information may also be transferred to other countries or regions. The jurisdiction of these facilities worldwide may not implement the same personal information protection standards as in your jurisdiction.

Considering the user's inability to properly control the spread of their data, the third question is answered negatively as well.

According to the focused metrics of this review, the Xiaomi Wear app gets **0/3** score. 

## Zepp Life (former Mi Fit)

The saga of confusing privacy policies continues with Zepp Life app as well. Researching this family of devices leads us to discovery of two distinct apps: 'Zepp' and 'Zepp Life'. Both are made by the same corporation - Zepp Health Corporation. This corporation is formerly known as Huami. Amazfit is a consumer-facing brand of devices made by Zepp. This corporation is also [partially owned][010401] by Xiaomi and its apps also [work with many Xiaomi wearable devices][010402] as well. Basically 'Zepp Life' app is a replacement for former 'Mi Fit' app and is meant to support just the legacy Xiaomi wearable devices. By contrast, the 'Zepp' app is built primarily for Amazfit devices. We can assume, their technology and privacy policies will be similarly structured. But let us explore their respective privacy policies starting with 'Zepp Life'.

The ['Zepp Life' privacy policy][010400] states extensive biometric data amount collection: 

>Personal Body Information: When you use Zepp Life and our device, your personal body information may be collected, such as, heart rate, blood oxygen saturation, stress, PAI, BMI, muscle mass, body fat percentage, moisture content, protein, basal metabolism, visceral fat level, bone mass content, body shape and body age.
>
>Exercise Information: When you use the device for exercising, we may collect your exercise information, for example, steps, stand-up times, distance, time, duration, pace, target of excising, achieved exercising targets, maximum oxygen uptake(VO2 Max), recovery time, training effects, sports load, speed, stride frequency, stride length, calories burned, movement track, swing information, serve information, stroke times, stroke velocity, stroke length, stroke speed, swimming trips, swimming style, swolf index and resistance value.
>
>Information Recorded by Your Device: When you use Zepp Life to synchronize device data, personal data is recorded. For example, activity information, sleep data (such as, rapid eye movement(REM), waking times, time and duration of deep/light sleep, naps), blood oxygen saturation information and its change, number of breathing, heart rate, weight, air pressure, altitude, longitude, latitude, cumulative climbing/descending information, balance information.

The company discloses two possibilities of data processing restrictions, by either logging out of the account or switching off the functions which deal with sensitive information. This points to the inability of using certain functions of the app when we do not wish to share our data. Further down there is a section about user's privacy rights, where they explicitly name the right of withdrawing consent to the processing of user data. This possibility is not available globally, it is dependent on the applicability of laws like GDPR. Even then, it is accompanied by a statement that some features might be unavailable after the withdrawal. Obviously, they do not want users to stop sharing their data, and they only do the bare minimum as required by the law. Based on this assessment, the first question is answered negatively, supported by this excerpt from the [privacy policy][010400]:

> We recognize that privacy concerns differ from person to person. Therefore, we provide examples of ways we make available for you to choose to restrict the collection, use, disclosure or processing of your personal information and control your privacy settings:
> - Log in and out of the account;
> - Toggle on/off for other services and functionalities which deal with sensitive or personal information.
>
> ...
>
> In accordance with applicable law, you may have right to:
>
> ...
>
> - Withdraw Your Consent to our processing of your personal information. If you refrain from providing personal information or withdraw your consent to processing, some features of our Service may not be available;

There is no mention of on-device/local/federated analytics in their privacy policy, or marketing materials. The second question is thus answered negatively.

The third question is at least easy to answer, they disclose that biometric data is shared with their service providers and affiliates. There is also no mechanism provided in the privacy policy to block sharing this data with these third-parties. This comes as no surprise, due to the complicated technology and corporate structure of this app's developer. Due to this, it is probably necessary to share the data between affiliated companies. This approach can still elevate risk of data breach and decreases the transparency of where the sensitive data is located. The third question is answered negatively as well.

According to the focused metrics of this review, the Zepp Life app gets **0/3** score.

## Zepp (Amazfit)

Both the privacy policies for Zepp and Zepp Life app are hosted on huami.com server. Overall, there are some slight wording differences, but the content is the same. The [Zepp privacy policy][010500] contains very similar list of biometric data collected than the Zepp Life app. The difference is minimal and perhaps corresponds to the hardware capabilities of supported wearable devices. The withdrawal of data processing consent is also accompanied by the possibility of losing access to certain services. There is also no mention of on-device/local/federated analytics, and the third-party data sharing policy is the same as well. Thus, the score of this app corresponds to the score of Zepp app: **0/3**.

## Huawei Health

Huawei Health app collects extensive list of biometric data, and the [privacy policy][010600] directly says that all the data is automatically synced to the Huawei Cloud service. There is further mention that the app functionality is dependent on collection and processing of this data. With that said, Huawei also offers an option to disable cloud syncing, with the app still functional. We had to verify this by downloading and installing the app, and registering for a Huawei account. We were able to verify that indeed the user is able to disable data syncing, but predictably the analytical functions required us to enable cloud sync. There is though still a question of the app is completely usable without an internet connection, as some users had negative experiences (in 2020) with [offline functionality][010601]. Our limited experience with the app leads us to believe, that this app may be usable even offline, although without the analytics features. The commendable point is the ability to disable the cloud sync and rely only on local data. But due to the ambiguity of statements in the privacy policy and uncertainty if the app will work long-term in offline mode, for the first question We decided to award half a point.

As already mentioned, the analytical functionality is dependent on cloud synchronization, so we have to assume there is no on-device processing happening. Moreover, there is no mention about the on-device/local/federated analytics in their marketing materials nor privacy policy. The second question is answered negatively.

When reading through the privacy policy, there is no explicit mention that data will be shared to third-parties unless the user consents to it. But there is concern that Huawei might share the data in the cloud service with their affiliates. But when we read through [general privacy statement][010602], there is a statement:

> **(2) Information that Huawei collects when you use services**
>
> ...
>
> e. Information stored in the cloud. For example, the information you upload to the cloud will be stored on our servers for rapid access and sharing between devices. *No one has access to such information without your permission.*

So we can assume that even if the user chooses to synchronize their data through Huawei Cloud service, it will not get shared to third-parties without a consent. Due to this, the third question can be answered positively.

According to the focused metrics of this review, the Huawei Health app gets **1.5/3** score.

## Samsung Health

Reviewing the Samsung Health [privacy policy][010700] the user can learn that there is an extensive list of biometric data the app collects. There is also no mechanism specified if the user can opt out of sharing this data. We also could not find any information if the app can be used offline. Due to the lack of information we decided to install the app. First of all, the app requires an internet connection during initial setup, but did not require us to register for an account. During the setup it misleadingly offered allowing optional data collection options. After initial setup, to our surprise, there is an option in the settings to disable the "Collection and use of general/sensitive personal information". This could mean that the app will not share the biometric data collected by wearable device. With our limited testing we were also successfully able to interact with the app even in an offline state. But due to the ambiguity of the privacy policy and lack of information if the app can be run without sharing biometric data we decided to award half a point for the first question.

There is no explicit mention in the [privacy policy][010700] or marketing materials about on-device data analytics, so the second question can be answered negatively. But there is perhaps a local analytics system in place, as there is nothing in the app that would refute that. Unfortunately we are unable to test this claim, as we do not have compatible wearable device available.

Samsung claims in their privacy policy that they disclose the user data to their "Affiliates", "Business partners", "Service providers". There is no clear mechanism in the privacy policy or the app to disable sharing of the data to these third-parties. [Independent researchers][010701] also criticized Samsung's opaque policies concerning sharing user's data to third-parties and deliberately obfuscating important privacy settings. Due to these reasons the third question can be answered negatively. It is though important to mention that if the app can be run in offline mode, there would not be privacy concerns like these, but that is not the meaning behind the third question.

According to the focused metrics of this review, the Samsung Health app gets **0.5/3** score.

## Whoop

[privacy policy][010800]

**-TBD-**

## Gadgetbridge - Privacy-oriented open-source project

When considering the viability of our project, we had to consider either developing complete application system from scratch, or preferably contributing our knowledge and know-how to already established open-source project. [Gadgetbridge][010900] is the best-known complete solution for communicating with and managing wearable devices. Its goal is to replace closed-source vendor-specific apps and allow users to retain most of the functionality of vendor provided apps. It retains all the biometric data locally and supports visualization of the data. Although, as you might have guessed, the data processing is limited to basic statistics. There is also sleep stage classification functionality, but when we explored the code further and read through relevant research papers, it appears that the smartwatches seldom use some kind of statistical algorithm that is not as accurate as neural net models. In this context, Gadgetbridge serves as data visualizer. This is not a bad thing and can be mostly as useful as vendor apps, but there is certainly room for improvement. Its [source code][010901] is available on Github.

[010000]: https://www.fitbit.com/global/us/legal/privacy-policy "Fitbit privacy policy"
[010001]: https://noyb.eu/en/your-fitbit-useless-unless-you-consent-unlawful-data-sharing "noyb: Fitbit complaints"
[010002]: https://www.theverge.com/2021/1/14/22188428/google-fitbit-acquisition-completed-approved "The Verge: Google Fitbit acquisition"

[010100]: https://www.garmin.com/en-US/privacy/connect/policy/ "Garmin privacy policy"
[010101]: https://forums.garmin.com/apps-software/mobile-apps-web/f/garmin-connect-web/108946/using-connect-app-without-internet-access#pifragment-1286=1 "Garmin blog post"
[010102]: https://foundation.mozilla.org/en/privacynotincluded/garmin/ "Mozilla: Garmin"
[010103]: https://www.wired.com/story/garmin-outage-ransomware-attack-workouts-aviation/ "Wired: Garmin ransomware attack"

[010200]: https://www.apple.com/legal/privacy/en-ww/ "Apple privacy policy"
[010201]: https://www.apple.com/privacy/docs/Health_Privacy_White_Paper_May_2023.pdf "Apple Health privacy white paper"
[010202]: https://support.apple.com/en-us/HT202303 "Apple: iCloud data security"
[010203]: https://machinelearning.apple.com/research/enforcing-fairness "Apple: Enforcing Fairness in Private Federated Learning"
[010204]: https://machinelearning.apple.com/research/protection-against-reconstruction-and-its-applications-in-private-federated-learning "Apple: Protection Against Reconstruction"
[010205]: https://machinelearning.apple.com/research/federated-personalization "Apple: Federated Evaluation and Tuning"

[010300]: https://watch.iot.mi.com/html/privacy/index.html?locale=en_US&type=watch_privacy_policy&model=app#/ "Xiaomi privacy policy"
[010301]: https://foundation.mozilla.org/en/privacynotincluded/mi-band-6/ "Mozilla: Mi Band 6"
[010302]: https://trust.mi.com/pdf/Xiaomi__IoT_Privacy_White_Paper_EN_June_2021.pdf "Xiaomi IoT Privacy Whitepaper"
[010303]: https://www.reddit.com/r/miband/comments/t871s8/xiaomi_wear_app_sync_without_internet/ "Reddit: Xiaomi wear app sync without internet"

[010400]: https://upload-cdn.huami.com/tposts/2502792 "Zepp Life privacy policy"
[010401]: https://finance.yahoo.com/news/owning-34-zepp-health-corporation-122845387.html "Zepp ownership"
[010402]: https://www.androidauthority.com/zepp-life-mi-fit-app-3266258/ "Zepp Life compatibility"

[010500]: https://upload-cdn.huami.com/tposts/8191 "Zepp privacy policy"

[010600]: https://legal.cloud.huawei.com/legal/health/privacy-statement.htm?&code=DE&language=en-US&branchid=0&contenttag=default "Statement About Huawei Health and Privacy"
[010601]: https://consumer.huawei.com/en/community/details/Huawei-Health-app-offline-without-internet-connection/topicId_139890/ "Huawei Health offline"
[010602]: https://consumer.huawei.com/en/privacy/privacy-policy/ "Huawei privacy statement"

[010700]: https://samsunghealth.com/privacy "Samsung Health privacy policy"
[010701]: https://foundation.mozilla.org/en/privacynotincluded/samsung-galaxy-watch4/ "Mozilla: Samsung Galaxy Watch 4"

[010800]: https://www.whoop.com/us/en/full-privacy-policy/ "Whoop: privacy policy"

[010900]: https://gadgetbridge.org/ "Gadgetbridge home page"
[010901]: https://codeberg.org/Freeyourgadget/Gadgetbridge "Gadgetbridge source code"

# Fitness analytics use-cases

In this section we would like to focus on researching the common use cases for AI/ML powered analytics currently available in these apps. First, we will list and explain the purpose of selected analytics, and then select which one we would like to experiment with more thoroughly. As the focus of this review is not to develop new analytics, but to explore and experiment with privacy-preserving technologies on top of existing analytical approaches to fitness data.

## Activity classification

Apps ordinarily offer automatic classification function for user's physical activity. The most important sensor input for this function is the accelerometer, and possibly heart rate sensor and location data could be used as well. Usually this functionality determines if the user is idle, sleeping, walking, running or cycling, and there could be even more automatic classification categories available depending on the app. Our personal experience with Xiaomi band was that once an activity was detected, notification came about the possibility of starting a session for tracking of that activity. The user response to these notifications could be used as learning data for the analytics engine. But the approach is of course dependent on the specific app developers.

https://medium.com/@tyler.hutcherson/activity-classification-with-create-ml-coreml3-and-skafos-part-1-8f130b5701f6
https://apple.github.io/turicreate/docs/userguide/activity_classifier/

## Sleep stage classification

## Sleep quality score

## Data abnormality detection

## Menstrual cycle tracking

## Walking steadiness

## Exercise recommendations


https://9to5mac.com/2023/04/07/best-apple-health-features-apple-watch-iphone-accessories/
https://www.apple.com/ios/health/