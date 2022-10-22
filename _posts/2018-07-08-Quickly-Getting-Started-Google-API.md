---

firstPublishedAt: 1531981092428
latestPublishedAt: 1531981092428
slug: quickly-getting-started-with-google-maps-api-w-python-july-2018-platform
title: Quickly Getting Started with Google Maps API w/Python (July 2018 Platform)

tag: Technical
author_profile: true 
toc: true
---

You probably want to harness the power of Google Maps API for application development. Moreover, your are coding in Python.

This article provides instruction on how to utilize Google Map’s API from the new Maps Platform, and a brief mention about the legacy process ( Post July 2018 and Pre-July 2018, respectively).

I will start with the newer process, and then go into the Legacy process for existing developer accounts from [developers.google.com](https://developers.google.com/).

If you have any questions, please feel free to reach out to me [via LinkedIn.](https://www.linkedin.com/in/raulm8/)

Prerequisites:

- Python 3.6 (can have older versions…[but get with the times](https://www.linuxjournal.com/content/transitioning-python-3))

- `requests` library (built-in with Python)

- Google Account

# New Process (Post July 2018)

- Get Started

Please go to [https://cloud.google.com/maps-platform/](https://cloud.google.com/maps-platform/) , below.

> [**Geo-location APIs | Google Maps Platform | Google Cloud**](https://cloud.google.com/maps-platform/)
>
> <small>Choose Google Maps Platform to create immersive location experiences and make better business decisions with accurate real-time data & dynamic imagery.</small>

After that, click on “Get Started”.

You will see a list of options to enable API groups. For limiting the number of types of APIs you manage for your account, you can select the desired API you want to use.

If you select one type of API group, then those will only be enabled. All other APIs would have to be enabled thereafter.

For playing around, let’s enable them all, seen below

![Enabling all Google API groups](https://cdn-images-1.medium.com/max/1408/1*PtQxTkIdEjotTBOO5hTgIQ.png)

Thereafter, you can select an existing project (session, if you will) or create a new project. (e.g. Title: myApplicationWillBeFire)

Now, you must enter in some billing information. Though we are entering are billing information, and assumingly testing out this API, we should not be charged for using the API. [Per pricing documentation here](https://cloud.google.com/maps-platform/pricing/), “get \$200 in free usage for Maps, Routes, and Places every month”.

Cool. :)

> **Note: **Just be careful if you have your app running in production with a lot of requests made to Google Maps API. Else, you may get charged in that month of all \$200 credits being used

Assuming you enabled all three API groups, we can now get our API credential key. You can find this credential key in any of the API listings, or in your home page. Just look for the **credentials** tab.

Now that we have the credentials, we request information from the enabled [MapsAPI “Geocoding API”](https://developers.google.com/maps/documentation/geocoding/start) through our python file

<iframe
                width="0"
                height="0"
                src=""
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>

You should see a the JSON object from `response_json` .

Note:[ THIS DOCUMENTATION LINK IS YOUR FRIEND](https://developers.google.com/maps/documentation/)

……..or stackoverflow….ha

# **Old Processs (Pre-July 2018)**

[Per documentation](<https://cloud.google.com/maps-platform/user-guide/?__utma=102347093.1225766217.1531971273.1531974912.1531974912.1&__utmb=102347093.0.10.1531974912&__utmc=102347093&__utmx=-&__utmz=102347093.1531974912.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none)&__utmv=-&__utmk=194186285&_ga=2.26811837.1017490544.1531971273-1225766217.1531971273>), existing developers using Google’s Maps API know

> With the launch of Google Maps Platform, we’ve introduced changes to our products, pricing, and support to provide you with greater flexibility, transparency, and control. This guide explains how these changes may impact you and what steps you need to take. You can also read our [blog ](https://mapsplatform.googleblog.com/2018/05/introducing-google-maps-platform.html)for additional context.

> As of June 11, 2018, you must enable billing with a credit card and have a valid API key for all of your projects. This will give you the ability to scale easily with less downtime and fewer performance issues. In addition, we’ve simplified our 18 individual APIs into three products: Maps, Routes, and Places.

> In June 2016 [we announced](https://maps-apis.googleblog.com/2016/06/building-for-scale-updates-to-google.html) that we would stop supporting keyless usage, meaning any request that doesn’t include an API key or Client ID. This went into effect on June 11 2018, and keyless access is no longer supported. Keyless calls to the Maps JavaScript API and Street View API will return low-resolution maps watermarked with “for development purposes only.” Keyless calls to any of the following APIs will return an error: Maps Static API (including Static Street View), Directions API, Distance Matrix API, Geocoding API, Geolocation API, Places API, Roads API, and Time Zone API.

The old process was to simply to go to developers.google.com with your google account and create your developer account. Therafter, you could generate a key credential key in your project, without having to enable any APIs. It was just starting that project, and then creating the key for one API usage.

# Ending Comments (Will be updated):

#### _Why have a pricing model for API platform?_

My opinion is that applications from indie developers have have been popular, and using Google’s API service at an extraneous/well performed rate shows opportunity to capatilize on provided service. This is normal in industry.

What’s great is that they at least do \$200 each month, pay as you use. Anything more, then you pay.

#### Was it easier back then?

A bit, but times change. haha

#### How is the billing calculated?

> Usage is tracked for each Product SKU.

> A SKU is the combination of the Product API + the service or function called (for example, Places API — Place Details).

> A product may have multiple SKUs billed at different rates (for example, Places API — Place Details; Places API — Autocomplete — Per Character).

> SKU pricing is tiered, based on volume of use, with three tiers: 0–100,000; 100,001–500,000; 500,001+.

> Cost is calculated by SKU Usage x Price per each use.

> For each billing account, for qualifying Google Maps Platform SKUs, a \$200 USD Google Maps Platform credit is available each month, and automatically applied to the qualifying SKUs.

See more info below:

> [**Understanding Billing for Maps, Routes, and Places | Google Maps Platform | Google Developers**](<https://developers.google.com/maps/billing/understanding-cost-of-use?__utma=236542612.1225766217.1531971273.1531974912.1531974912.1&__utmb=236542612.0.10.1531974912&__utmc=236542612&__utmx=-&__utmz=236542612.1531974912.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none)&__utmv=-&__utmk=70452179&_ga=2.185321641.-1225766217.1531971273>)
>
> <small>Learn about the cost of use by SKU for the Google Maps Platform APIs</small>
