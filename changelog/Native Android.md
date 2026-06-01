# Native Android Changelog

{% updates format="full" %}
{% update date="2026-05-02" tags="improved" %}

## v2.1.8 - Latest

#### Improved

* Updated backend endpoint from AWS infrastructure to Akamai infrastructure.
* Retained all SDK size optimizations introduced in v2.1.7.
* TapMind SDK size remains approximately ~35 KB.
* Custom Adapter size remains approximately ~130 KB.

{% endupdate %}
{% update date="2026-04-28" tags="improved" %}

## v2.1.7

#### Improved

* Reduced overall SDK footprint to approximately ~165 KB:

  * TapMind SDK size reduced to approximately ~35 KB.
  * Custom Adapter size reduced to approximately ~130 KB.
* Continued using the existing AWS backend endpoint.

{% endupdate %}
{% update date="2026-04-13" tags="fixes,removed" %}

## v2.1.5

#### Fixed

* Banner size is now fetched directly from the publisher application and passed to Google Ad Manager (GAM).
* If `placementName` is unavailable in request parameters, an empty value is passed.

#### Removed

* Deprecated `placementName` logic.

{% endupdate %}
{% update date="2026-04-10" tags="added" %}

## v2.1.4

#### Added

* Added placement flag support for placement name tracking in the Bid Request API.

{% endupdate %}
{% update date="2026-03-30" tags="fixes" %}

## v2.1.3

#### Fixed

* Resolved an issue where a missing context caused application crashes within the adapter.

{% endupdate %}
{% update date="2026-03-26" tags="added" %}

## v2.1.2

#### Added

* Added support for dynamic ad size configuration.
* Dynamic ad size identifiers are now submitted to the backend for tracking.

{% endupdate %}
{% update date="2026-03-24" tags="fixes" %}

## v2.1.1

#### Fixed

* Resolved SDK version mismatch issues.

{% endupdate %}
{% update date="2026-03-20" tags="added,improved" %}

## v2.1.0

#### Added

* Standardized adapter architecture across all supported mediation partners.

#### Improved

* Unified naming conventions for improved clarity and consistency.
* Optimized ad request-to-response flow for faster and more reliable mediation handling.
* Enhanced placement handling to support more flexible and scalable configurations.

{% endupdate %}
{% endupdates %}
