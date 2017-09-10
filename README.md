# Organization Flapdoodle OSS
[![Build Status](https://travis-ci.org/flapdoodle-oss/de.flapdoodle.embed.mongo.downloader.svg?branch=master)](https://travis-ci.org/flapdoodle-oss/de.flapdoodle.embed.mongo.downloader)

We are now a github organization. You are invited to participate. :)

# Embedded MongoDB Downloader

Based on Embedded MongoDB and the work of [Laurent Gaertner](https://github.com/laurentgaertner) and [Ittai Zeidman](https://github.com/ittaiz)

## License

We use http://www.apache.org/licenses/LICENSE-2.0

### Build on top of

- Embed Process Util [de.flapdoodle.embed.mongo](https://github.com/flapdoodle-oss/de.flapdoodle.embed.mongo)

### Using in a hermetic environment

Some build tools strongly encourages you to have tests which are isolated from the internet.  
To support such a use-case you can use the `de.flapdoodle.embed.mongo.download-and-extract` utility.  
It produces a runnable jar (`de.flapdoodle.embed.mongo.download-and-extract-2.0.1-SNAPSHOT-jar-with-dependencies.jar`) which you can call with `java -jar de.flapdoodle.embed.mongo.download-and-extract-2.0.1-SNAPSHOT-jar-with-dependencies.jar $dbVersion` and it will download and extract the needed installer for you.  
Additionally you should pass the download directory to your test so that it can configure your `DownloadConfig#withCacheDir` to use that directory instead of downloading it from the internet.

### Maven

Stable (Maven Central Repository, Released: 10.09.2017 - wait 24hrs for [maven central](http://repo1.maven.org/maven2/de/flapdoodle/embed/de.flapdoodle.embed.mongo.downloader/maven-metadata.xml))

	<dependency>
		<groupId>de.flapdoodle.embed</groupId>
		<artifactId>de.flapdoodle.embed.downloader</artifactId>
		<version>2.0.0</version>
	</dependency>

Snapshots (Repository http://oss.sonatype.org/content/repositories/snapshots)

	<dependency>
		<groupId>de.flapdoodle.embed</groupId>
		<artifactId>de.flapdoodle.embed.mongo.downloader</artifactId>
		<version>2.0.1-SNAPSHOT</version>
	</dependency>


### Build from source

When you fork or clone our branch you should always be able to build the library by running

	mvn package

### Changelog

[Changelog](Changelog.md)

