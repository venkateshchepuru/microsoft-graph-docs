---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &graphconfig.TabsRequestBuilderGetQueryParameters{
	Expand: [] string {"teamsApp"},
	Filter: "teamsApp/id eq 'com.microsoft.teamspace.tab.planner'",
}
configuration := &graphconfig.TabsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.TeamsById("team-id").ChannelsById("channel-id").Tabs().GetWithRequestConfigurationAndResponseHandler(configuration, nil)


```