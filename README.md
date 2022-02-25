# ReadME


### Пример использования
```swift
MPAnalytics.shared.sendEvent(
    eventName: "ScreenView",
    properties: [
        "eventType": "page_view",
        "screenTitleName": "Title",
		    "screenClassName": screenName
    ],
    location: nil) { error in
        debugPrint(#line, error?.localizedDescription as Any)
    }
```

### 📦 Содержимое пакета для автоматического отслеживания 
```json
{
  "meta" : {},
  "profile" : {},
  "data" : [
    {
      "properties" : [
        {
          "key" : "screenTitleName",
          "value" : "Title"
        },
        {
          "key" : "screenClassName",
          "value" : "MPAnalyticsPlayground.MPAnalyticsViewController"
        },
        {
          "key" : "eventType",
          "value" : "page_view"
        }
      ],
      "eventAction" : "ScreenView",
    }
  ]
}
```
Автоматические отчеты о просмотре экрана можно отключить в iOS,
задав для SberVisorAutomaticScreenReportingEnabled значение NO (логическое значение) в Info.plist.
