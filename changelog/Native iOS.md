# Native iOS Changelog

{% updates format="full" %}
{% update date="2026-01-01" tags="added,improved,fixes,admob,google-ad-manager" %}

## v2.1.11 - Latest

#### Added

* Introduced SDK Crash Prevention Guard Layer to improve SDK stability and prevent common initialization failures.
* Added the following crash prevention guards:
  * OS Version Check
  * Double Initialization Protection
  * Parameter Validation
  * Mediation SDK Compatibility Check
  * Demand Partner Class Availability Check
  * Initialization Thread Validation
  * iOS Background Suspension Check
* Added backend error logging for SDK guard failures to improve diagnostics and monitoring.
* Added Test Mode support to enable testing with dedicated test ad unit IDs.
* Added privacy consent collection and propagation support for downstream ad network integrations.

#### Improved

* Updated ad request handling to use Core Engine-provided ad sizes for Google Ad Manager (GAM) requests and demand partner ad fetching.
* Reduced ad request response payload size to optimize bandwidth usage and lower backend serving costs.
* Updated SDK serving APIs to use the latest backend serving domain infrastructure.
* Enhanced SDK stability through proactive validation and runtime safeguards.
* Improved SDK initialization flow by skipping Google Mobile Ads (GMA) initialization when running under GAM or AdMob mediation to prevent duplicate initialization.

#### Fixed

* Prevented SDK crashes caused by invalid initialization states, unsupported environments, missing dependencies, and configuration issues.
* Improved error handling and reporting across SDK initialization and mediation setup flows.

{% endupdate %}
{% update date="2026-01-01" tags="added,admob,google-ad-manager" %}

## v2.1.10

#### Added

* Added compatibility support for iOS 12.0 when using the AWS backend endpoint.

{% endupdate %}
{% update date="2026-01-01" tags="added,admob,google-ad-manager" %}

## v2.1.9

#### Added

* Added compatibility support for iOS 12.0 when using the Akamai backend endpoint.

{% endupdate %}
{% update date="2026-01-01" tags="improved,admob,google-ad-manager" %}

## v2.1.8

#### Improved

* Updated backend endpoint from AWS infrastructure to Akamai infrastructure.
* Resolved issues identified in v2.1.7.

{% endupdate %}
{% update date="2026-01-01" tags="improved,admob,google-ad-manager" %}

## v2.1.7

#### Improved

* Updated backend endpoint from AWS infrastructure to Akamai infrastructure.

#### Notes

* This release encountered issues after publication and was superseded by v2.1.8.

{% endupdate %}
{% update date="2026-01-01" tags="added,admob,google-ad-manager,applovin,ironsource-levelplay" %}

## v2.1.5

#### Added

* Added support for dynamic ad size configuration.

#### Improved

* If `placementName` is unavailable in parameters, an empty value is passed.

{% endupdate %}
{% update date="2026-01-01" tags="fixes,improved,admob,google-ad-manager,applovin,ironsource-levelplay" %}

## v2.1.4

#### Fixed

* Fixed TapMind SDK version resolution within the Swift Package Manager (SPM) distribution.

#### Improved

* Performed internal optimizations and stability enhancements to improve overall SDK performance and reliability.

{% endupdate %}
{% update date="2026-01-01" tags="added,admob,google-ad-manager,applovin,ironsource-levelplay" %}

## v2.1.3

#### Added

* Introduced placement flag configuration to support placement name tracking in the Bid Request API.

{% endupdate %}
{% update date="2026-01-01" tags="added,admob,google-ad-manager,applovin,ironsource-levelplay" %}

## v2.1.2

#### Added

* Added case-insensitive key handling for JSON parsing.
* Ensures reliable data extraction regardless of variations in JSON key casing received from backend services.

{% endupdate %}
{% update date="2026-01-01" tags="fixes,admob,google-ad-manager,applovin,ironsource-levelplay" %}

## v2.1.1

#### Fixed

* Fixed TapMind SDK version management within the Swift Package Manager (SPM) distribution.
* Ensures the designated TapMind SDK version is automatically used when installing the adapter through SPM.

{% endupdate %}
{% update date="2026-01-01" tags="added,improved,admob,google-ad-manager,applovin,ironsource-levelplay" %}

## v2.1.0

#### Added

* Standardized adapter architecture across all supported mediation partners.

#### Improved

* Unified naming conventions for improved clarity and consistency.
* Optimized ad request-to-response flow for faster and more reliable mediation handling.
* Enhanced placement handling to support flexible and scalable configurations.

{% endupdate %}
{% endupdates %}
