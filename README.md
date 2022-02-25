<h1 align="center">Welcome to the official OneSignal Ruby Client 👋</h1>

[![Gem Version][rgb]][rgl]

<p>
  <a href="https://github.com/OneSignal/onesignal-ruby-client/blob/master/README.md" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/OneSignal/onesignal-ruby-client/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://twitter.com/onesignal" target="_blank">
    <img alt="Twitter: onesignal" src="https://img.shields.io/twitter/follow/onesignal.svg?style=social" />
  </a>
</p>


OneSignal - the Ruby gem for the OneSignal

A powerful way to send personalized messages at scale and build effective customer engagement strategies. Learn more at onesignal.com

This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

OneSignal is a simple ruby wrapper for the [OneSignal API][osa].

### 🖤 [RubyGems](https://rubygems.org/gems/onesignal)

## 🚧 In Beta 🚧

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'onesignal', '~> 1.0.0.beta1'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install onesignal --pre

Or install from Github:
    $ gem "onesignal", '~> 1.0.0.beta1', git: 'git://github.com/OneSignal/onesignal-ruby-client.git'

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:

```ruby
require 'time'
require 'onesignal'
# setup authorization
OneSignal.configure do |config|
  # Configure Bearer authorization: app_key
  config.access_token = 'YOUR BEARER TOKEN' # Change this
end

api_instance = OneSignal::DefaultApi.new
notification = OneSignal::Notification.new({app_id: 'YOUR APP ID'}) # Notification

begin
  # Create notification
  result = api_instance.create_notification(notification)
  p result
rescue OneSignal::ApiError => e
  puts "Error when calling DefaultApi->create_notification: #{e}"
end
```

## Documentation for API Endpoints

All URIs are relative to *https://onesignal.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OneSignal::DefaultApi* | [**cancel_notification**](docs/DefaultApi.md#cancel_notification) | **DELETE** /notifications/{notification_id} | Stop a scheduled or currently outgoing notification
*OneSignal::DefaultApi* | [**create_app**](docs/DefaultApi.md#create_app) | **POST** /apps | Create an app
*OneSignal::DefaultApi* | [**create_notification**](docs/DefaultApi.md#create_notification) | **POST** /notifications | Create notification
*OneSignal::DefaultApi* | [**create_player**](docs/DefaultApi.md#create_player) | **POST** /players | Add a device
*OneSignal::DefaultApi* | [**create_segments**](docs/DefaultApi.md#create_segments) | **POST** /apps/{app_id}/segments | Create Segments
*OneSignal::DefaultApi* | [**delete_player**](docs/DefaultApi.md#delete_player) | **DELETE** /players/{player_id} | Delete a user record
*OneSignal::DefaultApi* | [**delete_segments**](docs/DefaultApi.md#delete_segments) | **DELETE** /apps/{app_id}/segments/{segment_id} | Delete Segments
*OneSignal::DefaultApi* | [**export_players**](docs/DefaultApi.md#export_players) | **POST** /players/csv_export?app_id&#x3D;{app_id} | CSV export
*OneSignal::DefaultApi* | [**get_app**](docs/DefaultApi.md#get_app) | **GET** /apps/{app_id} | View an app
*OneSignal::DefaultApi* | [**get_apps**](docs/DefaultApi.md#get_apps) | **GET** /apps | View apps
*OneSignal::DefaultApi* | [**get_notification**](docs/DefaultApi.md#get_notification) | **GET** /notifications/{notification_id} | View notification
*OneSignal::DefaultApi* | [**get_notification_history**](docs/DefaultApi.md#get_notification_history) | **POST** /notifications/{notification_id}/history | Notification History
*OneSignal::DefaultApi* | [**get_notifications**](docs/DefaultApi.md#get_notifications) | **GET** /notifications | View notifications
*OneSignal::DefaultApi* | [**get_outcomes**](docs/DefaultApi.md#get_outcomes) | **GET** /apps/{app_id}/outcomes | View Outcomes
*OneSignal::DefaultApi* | [**get_player**](docs/DefaultApi.md#get_player) | **GET** /players/{player_id} | View device
*OneSignal::DefaultApi* | [**get_players**](docs/DefaultApi.md#get_players) | **GET** /players | View devices
*OneSignal::DefaultApi* | [**update_app**](docs/DefaultApi.md#update_app) | **PUT** /apps/{app_id} | Update an app
*OneSignal::DefaultApi* | [**update_player**](docs/DefaultApi.md#update_player) | **PUT** /players/{player_id} | Edit device
*OneSignal::DefaultApi* | [**update_player_tags**](docs/DefaultApi.md#update_player_tags) | **PUT** /apps/{app_id}/users/{external_user_id} | Edit tags with external user id


## Documentation for Models

 - [OneSignal::App](docs/App.md)
 - [OneSignal::Button](docs/Button.md)
 - [OneSignal::DeliveryData](docs/DeliveryData.md)
 - [OneSignal::ExportPlayersRequestBody](docs/ExportPlayersRequestBody.md)
 - [OneSignal::Filter](docs/Filter.md)
 - [OneSignal::FilterExpressions](docs/FilterExpressions.md)
 - [OneSignal::FilterNotificationTarget](docs/FilterNotificationTarget.md)
 - [OneSignal::GetNotificationRequestBody](docs/GetNotificationRequestBody.md)
 - [OneSignal::InlineResponse200](docs/InlineResponse200.md)
 - [OneSignal::InlineResponse2001](docs/InlineResponse2001.md)
 - [OneSignal::InlineResponse2002](docs/InlineResponse2002.md)
 - [OneSignal::InlineResponse2003](docs/InlineResponse2003.md)
 - [OneSignal::InlineResponse2004](docs/InlineResponse2004.md)
 - [OneSignal::InlineResponse2005](docs/InlineResponse2005.md)
 - [OneSignal::InlineResponse201](docs/InlineResponse201.md)
 - [OneSignal::InlineResponse400](docs/InlineResponse400.md)
 - [OneSignal::InlineResponse4001](docs/InlineResponse4001.md)
 - [OneSignal::InlineResponse4002](docs/InlineResponse4002.md)
 - [OneSignal::InlineResponse409](docs/InlineResponse409.md)
 - [OneSignal::Notification](docs/Notification.md)
 - [OneSignal::NotificationAllOf](docs/NotificationAllOf.md)
 - [OneSignal::NotificationAllOfAndroidBackgroundLayout](docs/NotificationAllOfAndroidBackgroundLayout.md)
 - [OneSignal::NotificationSlice](docs/NotificationSlice.md)
 - [OneSignal::NotificationTarget](docs/NotificationTarget.md)
 - [OneSignal::Operator](docs/Operator.md)
 - [OneSignal::OutcomeData](docs/OutcomeData.md)
 - [OneSignal::PlatformDeliveryData](docs/PlatformDeliveryData.md)
 - [OneSignal::Player](docs/Player.md)
 - [OneSignal::PlayerNotificationTarget](docs/PlayerNotificationTarget.md)
 - [OneSignal::PlayerSlice](docs/PlayerSlice.md)
 - [OneSignal::Purchase](docs/Purchase.md)
 - [OneSignal::Segment](docs/Segment.md)
 - [OneSignal::SegmentNotificationTarget](docs/SegmentNotificationTarget.md)
 - [OneSignal::StringMap](docs/StringMap.md)
 - [OneSignal::UpdatePlayerTagsRequestBody](docs/UpdatePlayerTagsRequestBody.md)


## Documentation for Authorization


### app_key

- **Type**: Bearer authentication

### user_key

- **Type**: Bearer authentication

## License

The gem is available as open source under the terms of the [MIT License][mit].

[rgb]: https://img.shields.io/gem/v/onesignal.svg
[rgl]: https://rubygems.org/gems/onesignal
[osa]: https://documentation.onesignal.com/reference/
[mit]: http://opensource.org/licenses/MIT

## Author

* Website: https://onesignal.com
* Twitter: [@onesignal](https://twitter.com/onesignal)
* Github: [@OneSignal](https://github.com/OneSignal)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/OneSignal/onesignal-ruby-client/issues).

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2022 [OneSignal](https://github.com/OneSignal).<br />
This project is [MIT](https://opensource.org/licenses/MIT) licensed.
