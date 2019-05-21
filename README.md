# Flow

This simple extension provides Proxy-like view along with search filter capabilities for all Burp sources. Some users might find Parameters count table column handy.

Request without responses received are also being shown and they are later updated as soon as response is received. This might be helpful to troubleshoot e.g. scanning issues.

Request and response are splitted into separate columns (Repeater-like view).

If required, extension window can be detached from Burp UI.

This extension _DOES NOT_ require Burp Suite Professional

![flow-example](https://cloud.githubusercontent.com/assets/4956006/9799914/4f812d0e-580a-11e5-9309-658996517a07.png)

## Known issues

* If Burp "Platform Authentication" is in use, or "Match and Replace" in request is used, Flow is unable to match responses to related requests. This is caused by Burp API limitations (lack of unique identifiers in HttpRequestResponse). Problem was reported to Portswigger. As a workaround I suggest to perform platform authentication / requests altering in upstream proxy.

* ~~Gnome-shell related issue: Filter popup appears correctly only on first use. Resizing Burp window helps.~~ Fixed

## Changelog

2017-03-10 - 1.10
- added "Reflect" column (analysis result is available in tooltip)

2017-03-09 - 1.09
- "display only requests with responses" should now work properly
- url field is now wider by default
- url field contains query pararameters when present
- "populate with requests from proxy history" option added

2016-10-17 - 1.06
- updated filter popup UI, extension is now initialized with current Proxy history. Detach window button have current extension version in its tool tip.

## Download

https://github.com/hvqzao/burp-flow/releases/download/1.06/flow.jar

## License

[MIT License](LICENSE)
