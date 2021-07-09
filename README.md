# Menstrual Product Locator

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
This app would allow college students to quickly find nearby menstrual products, whether they're in bathrooms on campus or donated by students who happen to have one in their backpack.

### App Evaluation
- **Category:** Health
- **Mobile:** Mobile is extremely important since all users will need the fast convenience of logging in on their phone to quickly find a product.
- **Story:** Creates a community of people on campus who menstruate. Allows them to support each other by donating products to each other during their times of need. Rewards people for logging free products in bathrooms on the map, or for donating a product to someone.
- **Market:** Any college students on campus who menstruate.
- **Habit:** Students always log on whenever they need a product in a public area but do not have one
- **Scope:** Begin with focusing on implementing a map where users can log that they need a menstrual product in a certain building, or log free products in a certain bathroom. Later on, expand into providing resources about menstrual health and products

## Product Spec
### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can log in with college ID/email
* User can create a new account
* User can see the map of nearby products offered in public bathrooms
* User can see the map of nearby students who need a product
* User can log their location on the map to signal they need a product
* User can accept another user's request for a product
* User can text the other user to commmunicate where to drop off the product
* User can earn exp points for logging free products
* User can see their exp level

**Optional Nice-to-have Stories**

* User can view discounts on menstrual products offered in nearby pharmacies or grocery stores
* User can learn about more sustainable menstrual products
* User can chat with other users in an app-wide chat

### 2. Screen Archetypes

* Login Screen
   * User can log in with college ID/email
   * User can create a new account
* Map Screen
   * User can see the map of nearby products offered in public bathrooms
   * User can see the map of nearby students who need a product
   * User can log their location on the map to signal they need a product
   * User can accept another user's request for a product
* Chat Screen
    * User can text the other user to commmunicate where to drop off the product
* Profile Screen
    * User can earn exp points for logging free products
    * User can see their exp level

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Map
* Profile

**Flow Navigation** (Screen to Screen)
* Login screen
   * Map screen
* Registration screen
    * Map screen
* Chat screen
    * Map screen
* Log request for a product screen
    * Map screen
    * Chat screen
* Log free public products screen
    * Map screen
* Settings screen
    * Profile screen

## Wireframes
<img width="917" alt="Screen Shot 2021-07-07 at 9 56 30 AM" src="https://user-images.githubusercontent.com/52675934/125110733-d0a4a000-e099-11eb-9834-0db1a2a37055.png">


## Schema
### Models
| Property               | Type                                 | Description                                 |
| ---------------------- | ------------------------------------ | ------------------------------------------- |
| user                   | Pointer to User                      | app user                                    |
| userLocation           | ParseGeoPoint Pointer to User        | user's specific location                    |
| freeProduct            | ParseObject                          | free product station                        |
| freeProductLocation    | ParseGeoPoint Pointer to freeProduct | free product location                       |
| buildingLocation       | String                               | user's described location                   |
| productRequest         | ParseObject                          | a user's request for a product              |
| productRequestLocation | ParseGeoPoint Pointer to freeProduct | location for a user's request for a product |
| password               | Pointer to User, String              | user's password                             |
| profilePic             | Pointer to User, File                | user's profile picture                      |
