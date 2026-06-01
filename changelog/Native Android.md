# Native Android Changelog

{% updates format="full" %}
{% update date="2026-06-01" tags="added,improved,fixes" %}

## v2.1.9 - Latest

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)

#### Added

* Introduced SDK Crash Prevention Guard Layer to improve SDK stability and prevent common initialization failures.
* Added the following crash prevention guards:
  * OS Version Check
  * Double Initialization Protection
  * Parameter Validation
  * Google Play Services Availability Check
  * Mediation SDK Compatibility Check
  * Demand Partner Class Availability Check
  * Initialization Thread Validation
* Added backend error logging for SDK guard failures to improve diagnostics and monitoring.
* Added Test Mode support to enable testing with dedicated test ad unit IDs.
* Added privacy consent collection and propagation support for downstream ad network integrations.
* Added new Google Ad Manager (GAM) adapter class names.

#### Improved

* Updated ad request handling to use Core Engine–provided ad sizes for Google Ad Manager (GAM) requests and demand partner ad fetching.
* Reduced ad request response payload size to optimize bandwidth usage and lower backend serving costs.
* Updated SDK serving APIs to use the latest backend serving domain infrastructure.
* Updated Unity LevelPlay integration classes for improved compatibility.
* Improved SDK initialization flow by skipping Google Mobile Ads (GMA) initialization when running under GAM or AdMob mediation to prevent duplicate initialization.
* Enhanced SDK stability through proactive validation and runtime safeguards.

#### Fixed

* Prevented SDK crashes caused by invalid initialization states, unsupported environments, missing dependencies, and configuration issues.
* Improved error handling and reporting across SDK initialization and mediation setup flows.

{% endupdate %}
{% update date="2026-05-02" tags="improved" %}

## v2.1.8

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)

#### Improved

* Updated backend endpoint from AWS infrastructure to Akamai infrastructure.
* Retained all SDK size optimizations introduced in v2.1.7.
* TapMind SDK size remains approximately ~35 KB.
* Custom Adapter size remains approximately ~130 KB.

{% endupdate %}
{% update date="2026-04-28" tags="improved" %}

## v2.1.7

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)

#### Improved

* Reduced overall SDK footprint to approximately ~165 KB:

  * TapMind SDK size reduced to approximately ~35 KB.
  * Custom Adapter size reduced to approximately ~130 KB.
* Continued using the existing AWS backend endpoint.

{% endupdate %}
{% update date="2026-04-13" tags="fixes,removed" %}

## v2.1.5

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)
* AppLovin MAX
* LevelPlay

#### Fixed

* Banner size is now fetched directly from the publisher application and passed to Google Ad Manager (GAM).
* If `placementName` is unavailable in request parameters, an empty value is passed.

#### Removed

* Deprecated `placementName` logic.

{% endupdate %}
{% update date="2026-04-10" tags="added" %}

## v2.1.4

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)
* AppLovin MAX
* LevelPlay

#### Added

* Added placement flag support for placement name tracking in the Bid Request API.

{% endupdate %}
{% update date="2026-03-30" tags="fixes" %}

## v2.1.3

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)
* AppLovin MAX
* LevelPlay

#### Fixed

* Resolved an issue where a missing context caused application crashes within the adapter.

{% endupdate %}
{% update date="2026-03-26" tags="added" %}

## v2.1.2

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)
* AppLovin MAX
* LevelPlay

#### Added

* Added support for dynamic ad size configuration.
* Dynamic ad size identifiers are now submitted to the backend for tracking.

{% endupdate %}
{% update date="2026-03-24" tags="fixes" %}

## v2.1.1

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)
* AppLovin MAX
* LevelPlay

#### Fixed

* Resolved SDK version mismatch issues.

{% endupdate %}
{% update date="2026-03-20" tags="added,improved" %}

## v2.1.0

#### Supported Mediations

* AdMob
* Google Ad Manager (GAM)
* AppLovin MAX
* LevelPlay

#### Added

* Standardized adapter architecture across all supported mediation partners.

#### Improved

* Unified naming conventions for improved clarity and consistency.
* Optimized ad request-to-response flow for faster and more reliable mediation handling.
* Enhanced placement handling to support more flexible and scalable configurations.

{% endupdate %}
{% endupdates %}
