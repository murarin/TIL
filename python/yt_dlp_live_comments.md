# yt-dlp で Youtube Live のチャットを取得する

## チャット取得方法
```python
from yt_dlp import YoutubeDL

ydl_video_opts = {
    'outtmpl' : '%(id)s.%(ext)s',
    'writesubtitles' : True,
    'skip_download' : True
}

with YoutubeDL(ydl_video_opts) as ydl:
    ydl.download([
        'https://www.youtube.com/watch?v=j098o7024Ss'
    ])
```

- 配信中の場合は実行時点以降で投稿されたチャットが保存される。
- アーカイブの場合は全てのチャットが保存される。
- スーパーチャットも保存される。
- `${video_id}.live_chat.json` という名前で保存される。

<br>

## チャット形式

### 通常チャット

#### 得られるデータ
```json5
{"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "replayChatItemAction": {"actions": [{"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "addChatItemAction": {"item": {"liveChatTextMessageRenderer": {"message": {"runs": [{"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}]}, "authorName": {"simpleText": "ハコブネ@玄人"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/zvHG2oTofvyTnHOxGllHDXOHODZqW5lXs_ByiMHxhYemiJZqpa4GlD7vwS8fDafzrBBlwjvYZQU=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/zvHG2oTofvyTnHOxGllHDXOHODZqW5lXs_ByiMHxhYemiJZqpa4GlD7vwS8fDafzrBBlwjvYZQU=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "contextMenuEndpoint": {"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMGsyUzIxUVRFazFYM05EUmxsRlRISlJXV1J0TkhkQmFsRWFLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlEyOWpXRTUyVjBodExWRjBWV1Z3U25Wd01uQk9XV2M0QWtnQlVBRSUzRA=="}}, "id": "ChwKGkNJNkttUExJNV9zQ0ZZRUxyUVlkbTR3QWpR", "timestampUsec": "1670418247739842", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/2ULgJzufGBXPh4FyETmX3jl7AvCtqAgli1H0-MeGL20BpPk4ssF-uvKTpNydDTnjCZ_Y-JuKKQ=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/2ULgJzufGBXPh4FyETmX3jl7AvCtqAgli1H0-MeGL20BpPk4ssF-uvKTpNydDTnjCZ_Y-JuKKQ=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "Member (1 year)", "accessibility": {"accessibilityData": {"label": "Member (1 year)"}}}}], "authorExternalChannelId": "UCocXNvWHm-QtUepJup2pNYg", "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:39"}, "trackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm"}}, "clientId": "CI6KmPLI5_sCFYELrQYdm4wAjQ"}}], "videoOffsetTimeMsec": "219812"}}
{"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "replayChatItemAction": {"actions": [{"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "addChatItemAction": {"item": {"liveChatTextMessageRenderer": {"message": {"runs": [{"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}]}, "authorName": {"simpleText": "N.S"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/MVTbTwUKFdFsz9p7jAV2bab3_0iJn94xwt0GxtCEngvW-Au9AEeSpjuaS5ytvVANdmGKarZ0AA=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/MVTbTwUKFdFsz9p7jAV2bab3_0iJn94xwt0GxtCEngvW-Au9AEeSpjuaS5ytvVANdmGKarZ0AA=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "contextMenuEndpoint": {"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMHQ1TUhKMlRFazFYM05EUmxsRlRISlJXV1J0TkhkQmFsRWFLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlEyWkdNbUpWWDNselFtcGlabGhTYlVrME5FUkliMUU0QWtnQlVBRSUzRA=="}}, "id": "ChwKGkNLeTBydkxJNV9zQ0ZZRUxyUVlkbTR3QWpR", "timestampUsec": "1670418248077195", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/vb-1lybJHkjf7O6CxKwm-Ox-Uw8IfX0ePatrwInQwo9FAsDH1lbVjri5dWTKxvML2ljPlhsoFw=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/vb-1lybJHkjf7O6CxKwm-Ox-Uw8IfX0ePatrwInQwo9FAsDH1lbVjri5dWTKxvML2ljPlhsoFw=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "Member (1 month)", "accessibility": {"accessibilityData": {"label": "Member (1 month)"}}}}], "authorExternalChannelId": "UCfF2bU_ysBjbfXRmI44DHoQ", "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:40"}, "trackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm"}}, "clientId": "CKy0rvLI5_sCFYELrQYdm4wAjQ"}}], "videoOffsetTimeMsec": "220186"}}
{"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "replayChatItemAction": {"actions": [{"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "addChatItemAction": {"item": {"liveChatTextMessageRenderer": {"message": {"runs": [{"text": "半年寝かせてた檸檬堂開けたわ"}]}, "authorName": {"simpleText": "おんりぃ"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/XavRkZ6rGlnBkjQTxvRZebuPuXrLTkZg4AhlH0nHPMGo_z-T4-VvPAveqxDvCoZc9PH69YfgkQ=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/XavRkZ6rGlnBkjQTxvRZebuPuXrLTkZg4AhlH0nHPMGo_z-T4-VvPAveqxDvCoZc9PH69YfgkQ=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "contextMenuEndpoint": {"clickTrackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm", "commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMDlmVVhSbVRFazFYM05EUmxWVllXWlJiMlJvUldkUFExRWFLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlEyWndaVEF4ZDJGRVpqaDBRVGg1VTB0YVoxcG9Za0U0QWtnQlVBRSUzRA=="}}, "id": "ChwKGkNPX1F0ZkxJNV9zQ0ZVVWFmUW9kaEVnT0NR", "timestampUsec": "1670418248198204", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/8e16_tQaCtP4Tppt3NwGDU5iHe3y8ZmCz2eBJCcrA_lUEXTZ--rh3WkrPWVkGSGUSjK7Z8nf=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/8e16_tQaCtP4Tppt3NwGDU5iHe3y8ZmCz2eBJCcrA_lUEXTZ--rh3WkrPWVkGSGUSjK7Z8nf=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "Member (2 months)", "accessibility": {"accessibilityData": {"label": "Member (2 months)"}}}}], "authorExternalChannelId": "UCfpe01waDf8tA8ySKZgZhbA", "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:40"}, "trackingParams": "CAEQl98BIhMI2-GtveSWigMVA2EPAh3HPBXm"}}, "clientId": "CO_QtfLI5_sCFUUafQodhEgOCQ"}}], "videoOffsetTimeMsec": "220295"}}
{"replayChatItemAction": {"actions": [{"addChatItemAction": {"item": {"liveChatTextMessageRenderer": {"message": {"runs": [{"text": "いええええええい！！！！"}]}, "authorName": {"simpleText": "♡綴華(とじげ)(top Jesus get away)♡"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/KaEYhNEU6CfzwM08hkZRVCzv7-MnHRGxyOxqx73esUCl2rT5qydX1Zt7AIhL5rYE4CIBWsHb=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/KaEYhNEU6CfzwM08hkZRVCzv7-MnHRGxyOxqx73esUCl2rT5qydX1Zt7AIhL5rYE4CIBWsHb=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "contextMenuEndpoint": {"commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMDF5ZERoUVRFazFYM05EUmxWVllXWlJiMlJvUldkUFExRWFLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlEyeHVhbEpDUTBWZmIyTm1SbWt4Tm1kdVlWbEhTSGM0QWtnQlVBRSUzRA=="}}, "id": "ChwKGkNNcnQ4UExJNV9zQ0ZVVWFmUW9kaEVnT0NR", "timestampUsec": "1670418249153192", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/5F9IiTptjtKJBY7wXsb9YcBS3tZLDtNcRG0mUX-YZ74v4-pFXPk7LY3aw-3uVB4tcUgP-6azTQ=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/5F9IiTptjtKJBY7wXsb9YcBS3tZLDtNcRG0mUX-YZ74v4-pFXPk7LY3aw-3uVB4tcUgP-6azTQ=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "Member (6 months)", "accessibility": {"accessibilityData": {"label": "Member (6 months)"}}}}], "authorExternalChannelId": "UClnjRBCE_ocfFi16gnaYGHw", "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:41"}}}, "clientId": "CMrt8PLI5_sCFUUafQodhEgOCQ"}}], "videoOffsetTimeMsec": "221275"}}
{"replayChatItemAction": {"actions": [{"addChatItemAction": {"item": {"liveChatTextMessageRenderer": {"message": {"runs": [{"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}, {"emoji": {"emojiId": "UCFG6teapZaN6J1oVXl7MYPA/cIt5YdHOMKXQ8gTGxrrwDw", "shortcuts": [":_けーぴー:", ":けーぴー:"], "searchTerms": ["_けーぴー", "けーぴー"], "image": {"thumbnails": [{"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w24-h24-c-k-nd", "width": 24, "height": 24}, {"url": "https://yt3.ggpht.com/7reEmc_TZpS5V4_lkUunwvkX3vnTuN-vK-APZ2u2Cwp8qFm7ILNfS6BMNpHP0NnDVD_-boxarA=w48-h48-c-k-nd", "width": 48, "height": 48}], "accessibility": {"accessibilityData": {"label": "けーぴー"}}}, "isCustomEmoji": true}}]}, "authorName": {"simpleText": "アﾁｬばぶ"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/RtFshEcMZvLr433-YFXlWCIgfSF6b7HjI7rdKf9peg1dLuUspb610UiRf3Ro8iRVp12e0IfXpg=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/RtFshEcMZvLr433-YFXlWCIgfSF6b7HjI7rdKf9peg1dLuUspb610UiRf3Ro8iRVp12e0IfXpg=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "contextMenuEndpoint": {"commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMG8yU0hOUVVFazFYM05EUmxwTlYzSlJXV1J1Y0hOSWNYY2FLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlEzTlJZVGh5Wmt0c2NrTmxkV2ROWDBseFIzZHhjbmM0QWtnQlVBRSUzRA=="}}, "id": "ChwKGkNKNkhzUFBJNV9zQ0ZaTVdyUVlkbnBzSHF3", "timestampUsec": "1670418250180249", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/4np3bhcYL4oAA6LQi3-H3wqS6eJBdcg1Kh5V8wKBKJL1P3dGGInHGG__2ltKoaXJdGwCh8SXGQ=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/4np3bhcYL4oAA6LQi3-H3wqS6eJBdcg1Kh5V8wKBKJL1P3dGGInHGG__2ltKoaXJdGwCh8SXGQ=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "New member", "accessibility": {"accessibilityData": {"label": "New member"}}}}], "authorExternalChannelId": "UCsQa8rfKlrCeugM_IqGwqrw", "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:42"}}}, "clientId": "CJ6HsPPI5_sCFZMWrQYdnpsHqw"}}], "videoOffsetTimeMsec": "222385"}}
{"replayChatItemAction": {"actions": [{"addChatItemAction": {"item": {"liveChatTextMessageRenderer": {"message": {"runs": [{"text": "乾杯"}]}, "authorName": {"simpleText": "かい"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/ytc/AIdro_lRTbQerRfFtuMUaPe5IQjkAWESOLPpoXzl7iabeSAMmgXogXRobKUMDKcPNYkREs7SIqnnMEU2=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/ytc/AIdro_lRTbQerRfFtuMUaPe5IQjkAWESOLPpoXzl7iabeSAMmgXogXRobKUMDKcPNYkREs7SIqnnMEU2=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "contextMenuEndpoint": {"commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMHB4VlhObVVFazFYM05EUmxsdlNUVjNiMlJuVURCRmFIY2FLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlEzaGFlRTQ0TWtwc1VuSnNXVEYwWWtGZlNtMHpiR2M0QWtnQlVBRSUzRA=="}}, "id": "ChwKGkNKcVVzZlBJNV9zQ0ZZb0k1d29kZ1AwRWh3", "timestampUsec": "1670418250133085", "authorExternalChannelId": "UCxZxN82JlRrlY1tbA_Jm3lg", "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:42"}}}, "clientId": "CJqUsfPI5_sCFYoI5wodgP0Ehw"}}], "videoOffsetTimeMsec": "222406"}}
```

`clickTrackingParams` があるデータと無いデータがある。

#### `clickTrackingParams` とは？ by. ChatGPT
---
`clickTrackingParams` は、YouTubeの内部トラッキング用のパラメータです。このパラメータは、ユーザーがどのようなアクションを行ったかを追跡するために使われます。具体的には、以下のような用途が考えられます：

1. クリックイベントの追跡
   ユーザーが特定のボタンやリンクをクリックした際に、それを記録するためのデータです。この情報は、YouTubeがユーザーの行動を分析する際に使用します。

2. 動画やチャットのインタラクション
   動画の再生、チャットへのいいね、返信、またはチャットメニューを開くといった行動を識別するための識別子です。

3. おすすめアルゴリズムの最適化
   トラッキングデータをもとに、ユーザーがどのようなコンテンツに興味を持っているかを分析し、関連するおすすめ動画を表示するために利用される可能性があります。

4. 広告や分析目的
   広告主やコンテンツ制作者に対して、どのコンテンツやインタラクションが効果的だったかを分析するためのデータを提供するのにも役立ちます。

このパラメータ自体は暗号化またはエンコードされているため、直接読み解くことは難しいですが、クリックされた要素やそのコンテキストに関連する情報を含んでいると考えられます。
もし具体的な用途を調べたい場合、GoogleのAPIドキュメントやデバッグツールを確認することをおすすめします。

---

#### データ取得例
```python
chat = data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatTextMessageRenderer"]

chat_text = chat["message"]["runs"][0]["text"] # チャットテキスト
author_name = chat["authorName"]["simpleText"] # チャットの投稿者
timestamp_text = chat["timestampText"]["simpleText"] # 動画時間に対する投稿時間 (例: 3:04)
video_offset_time = data["replayChatItemAction"]["videoOffsetTimeMsec"] # 動画時間に対する投稿時間（ミリ秒）
```


<br>

### スパチャ
1つのスパチャに対して2行出力される。

1行目
```json5
{"clickTrackingParams": "CAEQl98BIhMI9frM29-WigMVnFkPAh1cIRP0", "replayChatItemAction": {"actions": [{"clickTrackingParams": "CAEQl98BIhMI9frM29-WigMVnFkPAh1cIRP0", "addChatItemAction": {"item": {"liveChatPaidMessageRenderer": {"id": "ChwKGkNPVDRxdVBJNV9zQ0Zaa1lyUVlkWkVFSXd3", "timestampUsec": "1670418229336989", "authorName": {"simpleText": "三徹明けの清老頭"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/h6jFBouVDmh6pXYIH_HfOpwQrTqYwusNQRD5Cx7154BKUI8r__glr813h_QMWsc-gJCnLW7k7Ss=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/h6jFBouVDmh6pXYIH_HfOpwQrTqYwusNQRD5Cx7154BKUI8r__glr813h_QMWsc-gJCnLW7k7Ss=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "purchaseAmountText": {"simpleText": "¥1,000"}, "message": {"runs": [{"text": "呑もうぜー"}]}, "headerBackgroundColor": 4294947584, "headerTextColor": 3741319168, "bodyBackgroundColor": 4294953512, "bodyTextColor": 3741319168, "authorExternalChannelId": "UCP-WFX61iCi2XSxO1ebCaMg", "authorNameTextColor": 2315255808, "contextMenuEndpoint": {"clickTrackingParams": "CBAQ7rsEIhMI9frM29-WigMVnFkPAh1cIRP0", "commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMDlVTkhGMVVFazFYM05EUmxwcldYSlJXV1JhUlVWSmQzY2FLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlExQXRWMFpZTmpGcFEya3lXRk40VHpGbFlrTmhUV2M0QWtnQlVBOCUzRA=="}}, "timestampColor": 2147483648, "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:21"}, "trackingParams": "CBAQ7rsEIhMI9frM29-WigMVnFkPAh1cIRP0", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/8e16_tQaCtP4Tppt3NwGDU5iHe3y8ZmCz2eBJCcrA_lUEXTZ--rh3WkrPWVkGSGUSjK7Z8nf=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/8e16_tQaCtP4Tppt3NwGDU5iHe3y8ZmCz2eBJCcrA_lUEXTZ--rh3WkrPWVkGSGUSjK7Z8nf=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "Member (2 months)", "accessibility": {"accessibilityData": {"label": "Member (2 months)"}}}}], "textInputBackgroundColor": 822083583, "creatorHeartButton": {"creatorHeartViewModel": {"creatorThumbnail": {"sources": [{"url": "https://yt3.ggpht.com/7POOUCnAN1dIeBhxaVMJhQ3-IiG-_dYXt9a6eok_Gdj3k6EPri27ZgN_xbcQ1oOw5RxnIdtB19M=s48-c-k-c0x00ffffff-no-rj"}]}, "heartedIcon": {"sources": [{"clientResource": {"imageName": "full_heart-filled"}}]}, "unheartedIcon": {"sources": [{"clientResource": {"imageName": "full_heart"}}], "processor": {"borderImageProcessor": {"imageTint": {"color": 3741319168}}}}, "heartedHoverText": "❤ by 大代真白 /あおぎり高校", "heartedAccessibilityLabel": "Remove heart", "unheartedAccessibilityLabel": "Heart", "engagementStateKey": "EktsaXZlLWNoYXQtbWVzc2FnZS1lbmdhZ2VtZW50LXN0YXRlLUNod0tHa05QVkRSeGRWQkpOVjl6UTBaYWExbHlVVmxrV2tWRlNYZDMgLCgB"}}, "isV2Style": true, "replyButton": {"pdgReplyButtonViewModel": {"replyButton": {"buttonViewModel": {"iconName": "CHAT", "onTap": {"innertubeCommand": {"clickTrackingParams": "CBEQ68ENIhMI9frM29-WigMVnFkPAh1cIRP0", "showEngagementPanelEndpoint": {"identifier": {"surface": "ENGAGEMENT_PANEL_SURFACE_LIVE_CHAT", "tag": "PAreply_thread"}, "globalConfiguration": {"params": "ggm2AQojVWd5N2tlVnVFZFlhWjkzVFl5eDRBYUFCRHFnQmg0blBtQUkSVgopKicKGFVDRkc2dGVhcFphTjZKMW9WWGw3TVlQQRILajA5OG83MDI0U3MQARgBIAE6I1VneTdrZVZ1RWRZYVo5M1RZeXg0QWFBQkRxZ0JoNG5QbUFJGgggALABAPgBACIpKicKGFVDRkc2dGVhcFphTjZKMW9WWGw3TVlQQRILajA5OG83MDI0U3MoATAB"}, "engagementPanelPresentationConfigs": {"engagementPanelPopupPresentationConfig": {"popupType": "PANEL_POPUP_TYPE_DIALOG"}}}}}, "accessibilityText": "Reply", "style": "BUTTON_VIEW_MODEL_STYLE_CUSTOM", "trackingParams": "CBEQ68ENIhMI9frM29-WigMVnFkPAh1cIRP0", "type": "BUTTON_VIEW_MODEL_TYPE_TONAL", "buttonSize": "BUTTON_VIEW_MODEL_SIZE_XSMALL", "customBackgroundColor": 218103808, "customFontColor": 3741319168, "loggingDirectives": {"trackingParams": "CBEQ68ENIhMI9frM29-WigMVnFkPAh1cIRP0", "visibility": {"types": "12"}, "enableDisplayloggerExperiment": true}}}, "replyCountEntityKey": "EiNVZ3k3a2VWdUVkWWFaOTNUWXl4NEFhQUJEcWdCaDRuUG1BSSDxAygB", "replyCountPlaceholder": {"content": "Reply", "styleRuns": [{"startIndex": 0, "length": 5}]}}}}}, "clientId": "COT4quPI5_sCFZkYrQYdZEEIww"}}], "videoOffsetTimeMsec": "201528"}}
```

2行目
```json5
{"clickTrackingParams": "CAEQl98BIhMI9frM29-WigMVnFkPAh1cIRP0", "replayChatItemAction": {"actions": [{"clickTrackingParams": "CAEQl98BIhMI9frM29-WigMVnFkPAh1cIRP0", "addLiveChatTickerItemAction": {"item": {"liveChatTickerPaidMessageItemRenderer": {"id": "ChwKGkNPVDRxdVBJNV9zQ0Zaa1lyUVlkWkVFSXd3", "amountTextColor": 3741319168, "startBackgroundColor": 4294953512, "endBackgroundColor": 4294947584, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/h6jFBouVDmh6pXYIH_HfOpwQrTqYwusNQRD5Cx7154BKUI8r__glr813h_QMWsc-gJCnLW7k7Ss=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/h6jFBouVDmh6pXYIH_HfOpwQrTqYwusNQRD5Cx7154BKUI8r__glr813h_QMWsc-gJCnLW7k7Ss=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}], "accessibility": {"accessibilityData": {"label": "三徹明けの清老頭"}}}, "durationSec": 300, "showItemEndpoint": {"clickTrackingParams": "CAwQsMgEIhMI9frM29-WigMVnFkPAh1cIRP0", "commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "showLiveChatItemEndpoint": {"renderer": {"liveChatPaidMessageRenderer": {"id": "ChwKGkNPVDRxdVBJNV9zQ0Zaa1lyUVlkWkVFSXd3", "timestampUsec": "1670418229336989", "authorName": {"simpleText": "三徹明けの清老頭"}, "authorPhoto": {"thumbnails": [{"url": "https://yt4.ggpht.com/h6jFBouVDmh6pXYIH_HfOpwQrTqYwusNQRD5Cx7154BKUI8r__glr813h_QMWsc-gJCnLW7k7Ss=s32-c-k-c0x00ffffff-no-rj", "width": 32, "height": 32}, {"url": "https://yt4.ggpht.com/h6jFBouVDmh6pXYIH_HfOpwQrTqYwusNQRD5Cx7154BKUI8r__glr813h_QMWsc-gJCnLW7k7Ss=s64-c-k-c0x00ffffff-no-rj", "width": 64, "height": 64}]}, "purchaseAmountText": {"simpleText": "¥1,000"}, "message": {"runs": [{"text": "呑もうぜー"}]}, "headerBackgroundColor": 4294947584, "headerTextColor": 3741319168, "bodyBackgroundColor": 4294953512, "bodyTextColor": 3741319168, "authorExternalChannelId": "UCP-WFX61iCi2XSxO1ebCaMg", "authorNameTextColor": 2315255808, "contextMenuEndpoint": {"clickTrackingParams": "CA4Q7rsEIhMI9frM29-WigMVnFkPAh1cIRP0", "commandMetadata": {"webCommandMetadata": {"ignoreNavigation": true}}, "liveChatItemContextMenuEndpoint": {"params": "Q2g0S0hBb2FRMDlVTkhGMVVFazFYM05EUmxwcldYSlJXV1JhUlVWSmQzY2FLU29uQ2hoVlEwWkhOblJsWVhCYVlVNDJTakZ2Vmxoc04wMVpVRUVTQzJvd09UaHZOekF5TkZOeklBRW9BVElhQ2hoVlExQXRWMFpZTmpGcFEya3lXRk40VHpGbFlrTmhUV2M0QWtnQlVBOCUzRA=="}}, "timestampColor": 2147483648, "contextMenuAccessibility": {"accessibilityData": {"label": "Chat actions"}}, "timestampText": {"simpleText": "3:21"}, "trackingParams": "CA4Q7rsEIhMI9frM29-WigMVnFkPAh1cIRP0", "authorBadges": [{"liveChatAuthorBadgeRenderer": {"customThumbnail": {"thumbnails": [{"url": "https://yt3.ggpht.com/8e16_tQaCtP4Tppt3NwGDU5iHe3y8ZmCz2eBJCcrA_lUEXTZ--rh3WkrPWVkGSGUSjK7Z8nf=s16-c-k", "width": 16, "height": 16}, {"url": "https://yt3.ggpht.com/8e16_tQaCtP4Tppt3NwGDU5iHe3y8ZmCz2eBJCcrA_lUEXTZ--rh3WkrPWVkGSGUSjK7Z8nf=s32-c-k", "width": 32, "height": 32}]}, "tooltip": "Member (2 months)", "accessibility": {"accessibilityData": {"label": "Member (2 months)"}}}}], "textInputBackgroundColor": 822083583, "creatorHeartButton": {"creatorHeartViewModel": {"creatorThumbnail": {"sources": [{"url": "https://yt3.ggpht.com/7POOUCnAN1dIeBhxaVMJhQ3-IiG-_dYXt9a6eok_Gdj3k6EPri27ZgN_xbcQ1oOw5RxnIdtB19M=s48-c-k-c0x00ffffff-no-rj"}]}, "heartedIcon": {"sources": [{"clientResource": {"imageName": "full_heart-filled"}}]}, "unheartedIcon": {"sources": [{"clientResource": {"imageName": "full_heart"}}], "processor": {"borderImageProcessor": {"imageTint": {"color": 3741319168}}}}, "heartedHoverText": "❤ by 大代真白 /あおぎり高校", "heartedAccessibilityLabel": "Remove heart", "unheartedAccessibilityLabel": "Heart", "engagementStateKey": "EktsaXZlLWNoYXQtbWVzc2FnZS1lbmdhZ2VtZW50LXN0YXRlLUNod0tHa05QVkRSeGRWQkpOVjl6UTBaYWExbHlVVmxrV2tWRlNYZDMgLCgB"}}, "isV2Style": true, "replyButton": {"pdgReplyButtonViewModel": {"replyButton": {"buttonViewModel": {"iconName": "CHAT", "onTap": {"innertubeCommand": {"clickTrackingParams": "CA8Q68ENIhMI9frM29-WigMVnFkPAh1cIRP0", "showEngagementPanelEndpoint": {"identifier": {"surface": "ENGAGEMENT_PANEL_SURFACE_LIVE_CHAT", "tag": "PAreply_thread"}, "globalConfiguration": {"params": "ggm2AQojVWd5N2tlVnVFZFlhWjkzVFl5eDRBYUFCRHFnQmg0blBtQUkSVgopKicKGFVDRkc2dGVhcFphTjZKMW9WWGw3TVlQQRILajA5OG83MDI0U3MQARgBIAE6I1VneTdrZVZ1RWRZYVo5M1RZeXg0QWFBQkRxZ0JoNG5QbUFJGgggALABAPgBACIpKicKGFVDRkc2dGVhcFphTjZKMW9WWGw3TVlQQRILajA5OG83MDI0U3MoATAB"}, "engagementPanelPresentationConfigs": {"engagementPanelPopupPresentationConfig": {"popupType": "PANEL_POPUP_TYPE_DIALOG"}}}}}, "accessibilityText": "Reply", "style": "BUTTON_VIEW_MODEL_STYLE_CUSTOM", "trackingParams": "CA8Q68ENIhMI9frM29-WigMVnFkPAh1cIRP0", "type": "BUTTON_VIEW_MODEL_TYPE_TONAL", "buttonSize": "BUTTON_VIEW_MODEL_SIZE_XSMALL", "customBackgroundColor": 218103808, "customFontColor": 3741319168, "loggingDirectives": {"trackingParams": "CA8Q68ENIhMI9frM29-WigMVnFkPAh1cIRP0", "visibility": {"types": "12"}, "enableDisplayloggerExperiment": true}}}, "replyCountEntityKey": "EiNVZ3k3a2VWdUVkWWFaOTNUWXl4NEFhQUJEcWdCaDRuUG1BSSDxAygB", "replyCountPlaceholder": {"content": "Reply", "styleRuns": [{"startIndex": 0, "length": 5}]}}}}}, "trackingParams": "CA0QjtEGIhMI9frM29-WigMVnFkPAh1cIRP0"}}, "authorExternalChannelId": "UCP-WFX61iCi2XSxO1ebCaMg", "fullDurationSec": 300, "trackingParams": "CAwQsMgEIhMI9frM29-WigMVnFkPAh1cIRP0", "authorUsername": {"simpleText": "三徹明けの清老頭"}, "animationOrigin": "ANIMATION_ORIGIN_PDG_TICKER_LIKE", "openEngagementPanelCommand": {"clickTrackingParams": "CAwQsMgEIhMI9frM29-WigMVnFkPAh1cIRP0", "showEngagementPanelEndpoint": {"identifier": {"surface": "ENGAGEMENT_PANEL_SURFACE_LIVE_CHAT", "tag": "PAreply_thread"}, "globalConfiguration": {"params": "ggm2AQojVWd5N2tlVnVFZFlhWjkzVFl5eDRBYUFCRHFnQmg0blBtQUkSVgopKicKGFVDRkc2dGVhcFphTjZKMW9WWGw3TVlQQRILajA5OG83MDI0U3MQARgBIAE6I1VneTdrZVZ1RWRZYVo5M1RZeXg0QWFBQkRxZ0JoNG5QbUFJGgggALABAPgBACIpKicKGFVDRkc2dGVhcFphTjZKMW9WWGw3TVlQQRILajA5OG83MDI0U3MoATAB"}, "engagementPanelPresentationConfigs": {"engagementPanelPopupPresentationConfig": {"popupType": "PANEL_POPUP_TYPE_DIALOG"}}}}}}, "durationSec": "300"}}], "videoOffsetTimeMsec": "201528"}}
```

#### 1行目と2行目の違い by.ChatGPT

---
1. 主な構造の違い
    - 1行目: `addChatItemAction` で通常のライブチャットメッセージを表現しています。これは、ライブチャットの中にテキストメッセージが表示される際の情報を含んでいます。
    - 2つめ: `addLiveChatTickerItemAction` でスーパーチャットのティッカー（画面上部に表示される固定の通知）を表現しています。これは、特別な支援メッセージが一定時間画面に固定される形式を表します。

2. 表示形式の違い
    - 1行目はチャット画面の中に直接表示されるメッセージ。
        - `liveChatPaidMessageRenderer` が使われており、支援メッセージをチャットに通常メッセージとして表示します。
    - 2行目は画面上部のティッカーとして固定表示されるメッセージ。
        - `liveChatTickerPaidMessageItemRenderer` が使われており、支援メッセージをティッカー形式で一定時間固定します。
3. 固有のデータフィールドの違い
    - 1行目:
        - `liveChatPaidMessageRenderer`: チャット内での支援メッセージの詳細（`message` や `purchaseAmountText`）を記述。
        - メッセージがチャット欄に即時反映される。
    - 2行目:
        - `liveChatTickerPaidMessageItemRenderer`: ティッカーに関連するフィールド（`startBackgroundColor`, `durationSec`）が含まれ、ティッカー表示の制御。
        - ティッカーの表示時間（`durationSec: 300`）やアニメーション設定が含まれる。

4. 表示の目的
    - 1行目は、支援メッセージをチャットの中で他のメッセージと同じように表示するためのもの。
    - 2行目は、スーパーチャットや特別な支援メッセージをティッカー形式で目立たせるためのもの。


共通点
- どちらも同じメッセージ「呑もうぜー」や支援額「¥1,000」、送信者「三徹明けの清老頭」に関する情報を含んでいます。
- 共通のID（例: `id: ChwKGkNPVDRxdVBJNV9zQ0Zaa1lyUVlkWkVFSXd3`）や、送信者の情報、タイムスタンプが含まれています。

要するに、1行目は「チャット内での表示」、2行目は「ティッカー形式での表示」という違いです。

---

通常のチャット欄のデータが必要なら1行目、ティッカー情報が必要なら2行目を使うと良い。

#### データ取得例
1行目から取得する場合
```python
chat = data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatPaidMessageRenderer"]

message = chat["message"]["runs"][0]["text"] # スパチャのメッセージ
author_name = chat["authorName"]["simpleText"] # スパチャの投稿者
timestamp_text = chat["timestampText"]["simpleText"] # 動画時間に対する投稿時間 (例: 3:04)
video_offset_time = data["replayChatItemAction"]["videoOffsetTimeMsec"] # 動画時間に対する投稿時間（ミリ秒）
purchase_amount = chat["purchaseAmountText"]["simpleText"] # スパチャの価格
```

2行目から取得する場合
```python
chat = data["replayChatItemAction"]["actions"][0]["addLiveChatTickerItemAction"]["item"]["liveChatTickerPaidMessageItemRenderer"]["showItemEndpoint"]["showLiveChatItemEndpoint"]["renderer"]["liveChatPaidMessageRenderer"]

message = chat["message"]["runs"][0]["text"]  # スパチャのメッセージ
author_name = chat["authorName"]["simpleText"]  # スパチャの投稿者
timestamp_text = chat["timestampText"]["simpleText"]  # 動画時間に対する投稿時間 (例: 3:04)
video_offset_time = data["replayChatItemAction"]["videoOffsetTimeMsec"]  # 動画時間に対する投稿時間（ミリ秒）
purchase_amount = chat["purchaseAmountText"]["simpleText"]  # スパチャの価格
```


### その他チャットの種類

#### 通常コメント
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatTextMessageRenderer"]
```

####  スパチャ (コメント欄)
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatPaidMessageRenderer"]
```

#### スパチャ（コメント欄上部）
```python
data["replayChatItemAction"]["actions"][0]["addLiveChatTickerItemAction"]["item"]["liveChatTickerPaidMessageItemRenderer"]
```

#### メーバーシップ入会通知
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatMembershipItemRenderer"]
```

#### コメント撤回通知
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatPlaceholderItemRenderer"]
```

#### メンバーシップギフト1
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatSponsorshipsGiftPurchaseAnnouncementRenderer"]
```

#### メンバーシップギフト2
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatSponsorshipsGiftRedemptionAnnouncementRenderer"]
``` 

メンバーシップギフト1とメンバーシップギフト2の違いはよくわからない

#### ステッカー
```python
data["replayChatItemAction"]["actions"][0]["addChatItemAction"]["item"]["liveChatPaidStickerRenderer"]
```
