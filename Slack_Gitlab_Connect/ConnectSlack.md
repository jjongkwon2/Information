# Gitlab과 Slack 연동하기

### 목적
Gitlab에서 수정되거나 삭제되는 등의 특정 이벤트가 발생했을 경우<br>
Slack 해당 채널에서 바로 관련 메세지가 뜨도록 한다.<br>


### 연동 방법

#### 1. 채널 생성 ( gitlab )<br>
![create_channel](/images_gitlab/create_channel.png)

#### 2. Add an app<br>
![add_an_app](/images_gitlab/add_an_app.png)

#### 3. Manage -> Custom Integrations -> Incoming WebHooks<br>
![webhooks](/images_gitlab/webhooks.png)

#### 4. Add Configuration<br>
![add_configuration](/images_gitlab/add_configuration.png)

#### 5. 해당 채널 선택 ( #gitlab )<br>
![post_to_channel](/images_gitlab/post_to_channel.png)

#### 6. Webhooks 주소 필요
![webhooks](/images_gitlab/webhooks_url.png)


#### 7.Gitlab 프로젝트에서 Webhooks URL 추가
1. gitlab -> project -> settings -> integrations
![gitlab_settings](/images_gitlab/gitlab_settings.png)

2. 스크롤을 내리면 밑에 Slack notification이 있다. 클릭!
(Slack Application도 있으니 주의!)
![slack_notifications](/images_gitlab/slack_notifications.png)

3. Active 체크 (필수!!)<br>
-> Trigger 체크 (Push, Issue, Merge ... ) <br>
-> Username 설정 <br>
-> Save changes

5. Authorize
![slack_authorize](/images_gitlab/slack_authorize.png)

#### 9. Test
1. gitlab 프로젝트를 push
![test_push](/images_gitlab/test_push.png)

2. slack에서 메세지가 온 것을 확인 가능하다.
![test_slack_message](/images_gitlab/test_slack_message.png)
