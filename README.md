[![Release](https://img.shields.io/github/release/imBenjamin741/RRule.svg?style=flat)](https://jitpack.io/#imBenjamin741/RRule)


# RRule
Kotlin implementation for conveniently handling and modifying iCalendar (RFC 5545) recurrence rules.

## Dependency

Add the following to your **build.gradle** file:
```groovy
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}

dependencies {
    implementation 'com.github.imBenjamin741:RRule:1.0.4'
}
```

Or add the following to your **pom.xml**:

```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>

<dependency>
    <groupId>com.github.imBenjamin741</groupId>
    <artifactId>RRule</artifactId>
    <version>1.0.4</version>
</dependency>
```

## Sample Usage

Transform iCalendar RFC 5545 String to RRule object:

```kotlin
val rrule = RRule("RRULE:FREQ=MONTHLY;INTERVAL=2;COUNT=10;BYDAY=1SU,-1SU")

// convenient property access
rrule.freq 
rrule.until
rrule.count
rrule.interval
rrule.byDay
// ...
```

Transform RRule object to iCalendar RFC 5545 String:

```kotlin
val rfc5545String = rrule.toRFC5545String()
```
