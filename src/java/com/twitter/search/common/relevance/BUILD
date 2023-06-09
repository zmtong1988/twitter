java_library(
    name = "utils",
    sources = ["utils/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/com/google/guava",
        "3rdparty/jvm/com/google/inject:guice",
        "3rdparty/jvm/com/twitter/elephantbird:core",
        "3rdparty/jvm/org/apache/hadoop:hadoop-client-default",
        "3rdparty/jvm/org/apache/thrift:libthrift",
        "src/java/com/twitter/common/base",
        "src/java/com/twitter/common/text/language:locale-util",
        "src/java/com/twitter/search/common/partitioning/snowflakeparser",
        "src/java/com/twitter/search/common/relevance/features",
        "src/java/com/twitter/search/common/schema/earlybird",
        "src/java/com/twitter/search/common/tweetypie",
        "src/thrift/com/twitter/search:earlybird-java",
        "src/thrift/com/twitter/search/common:schema-java",
    ],
)

java_library(
    name = "ranking",
    sources = ["ranking/**/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        ":utils",
        "3rdparty/jvm/com/google/guava",
        "3rdparty/jvm/com/google/inject:guice",
        "3rdparty/jvm/com/twitter/elephantbird:core",
        "3rdparty/jvm/org/apache/hadoop:hadoop-client-default",
        "3rdparty/jvm/org/apache/thrift:libthrift",
        "3rdparty/jvm/org/apache/zookeeper:zookeeper-client",
        "3rdparty/jvm/org/slf4j:slf4j-api",
        "src/java/com/twitter/common/base",
        "src/java/com/twitter/search/common/logging",
        "src/java/com/twitter/search/common/metrics",
        "src/java/com/twitter/search/common/relevance/features",
        "src/thrift/com/twitter/search:earlybird-java",
    ],
)

TRENDS_DATA_SERVICE_SOURCES = [
    "TrendsThriftDataServiceManager.java",
    "NGramCache.java",
]

java_library(
    name = "trends-data-service",
    sources = TRENDS_DATA_SERVICE_SOURCES,
    platform = "java8",
    provides = artifact(
        org = "com.twitter.search.common.relevance",
        name = "trends-data-service",
        repo = artifactory,
    ),
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/com/google/guava",
        "3rdparty/jvm/com/google/inject:guice",
        "3rdparty/jvm/io/netty:netty4-tcnative-boringssl-static",
        "3rdparty/jvm/org/apache/thrift:libthrift",
        "3rdparty/jvm/org/apache/zookeeper:zookeeper-client",
        "finagle-internal/mtls/src/main/scala/com/twitter/finagle/mtls/authentication",
        "finagle-internal/mtls/src/main/scala/com/twitter/finagle/mtls/client",
        "finagle/finagle-core/src/main",
        "finagle/finagle-thrift/src/main/java",
        "finagle/finagle-thriftmux/src/main/scala",
        "src/java/com/twitter/common/base",
        "src/java/com/twitter/common_internal/text/version",
        "src/java/com/twitter/penguin/search/filter",
        "src/java/com/twitter/search/common/metrics",
        "src/thrift/com/twitter/trends/plus:trends-plus-java",
        "src/thrift/com/twitter/trends/service/gen:trends_service-java",
        "src/thrift/com/twitter/trends/trending_content:trending-content-service-java",
        "trends/trends_metadata/thrift/src/main/thrift/com/twitter/trends/trends_metadata:thrift-java",
        "twitter-server-internal/src/main/scala",
        "util/util-core:scala",
        "util/util-stats/src/main/scala",
    ],
)

java_library(
    name = "feature-update-reader",
    sources = ["readers/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/org/apache/bookkeeper:bookkeeper-server",
        "3rdparty/jvm/org/apache/bookkeeper:bookkeeper-twitter-science-provider",
        "3rdparty/jvm/org/apache/hadoop:hadoop-client-default",
        "3rdparty/jvm/org/apache/thrift:libthrift",
        "3rdparty/jvm/org/apache/zookeeper:zookeeper-client",
        "3rdparty/jvm/org/slf4j:slf4j-api",
        "src/java/com/twitter/common/base",
        "src/java/com/twitter/common/util:system-mocks",
        "src/java/com/twitter/search/common/metrics",
        "src/java/com/twitter/search/common/util/io:record-reader-api",
        "src/java/com/twitter/search/common/util/thrift:text-protocol",
        "src/thrift/com/twitter/search/common:schema-java",
    ],
)

target(
    dependencies = [
        ":feature-update-reader",
        ":trends-data-service",
        "src/java/com/twitter/search/common/relevance/features",
    ],
)

java_library(
    name = "config",
    sources = ["config/**/*.java"],
    platform = "java8",
    provides = artifact(
        org = "com.twitter.search.common.relevance",
        name = "config",
        repo = artifactory,
    ),
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/org/apache/zookeeper:zookeeper-client",
        "src/java/com/twitter/search/common/config",
        "src/resources/com/twitter/search/common/relevance/config",
    ],
)

java_library(
    name = "classifiers",
    sources = ["classifiers/**/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        ":config",
        ":entities_and_filters",
        ":trends-data-service",
        "3rdparty/jvm/com/google/guava",
        "3rdparty/jvm/com/google/inject:guice",
        "3rdparty/jvm/com/twitter/elephantbird:core",
        "3rdparty/jvm/commons-lang",
        "3rdparty/jvm/geo/google:geoGoogle",
        "3rdparty/jvm/org/apache/hadoop:hadoop-client-default",
        "3rdparty/jvm/org/apache/thrift:libthrift",
        "3rdparty/jvm/org/apache/zookeeper:zookeeper-client",
        "finagle-internal/mtls/src/main/scala/com/twitter/finagle/mtls/authentication",
        "src/java/com/twitter/common/base",
        "src/java/com/twitter/common/collections",
        "src/java/com/twitter/common/text/language:locale-util",
        "src/java/com/twitter/common/text/token",
        "src/java/com/twitter/common/text/transformer",
        "src/java/com/twitter/common_internal/text:text-penguin7",
        "src/java/com/twitter/common_internal/text/version",
        "src/java/com/twitter/search/common/config",
        "src/java/com/twitter/search/common/metrics",
        "src/java/com/twitter/search/common/relevance/features",
        "src/java/com/twitter/search/common/util/io/periodic",
        "src/java/com/twitter/search/common/util/text",
        "twitter-text/lib/java/src/main/java/com/twitter/twittertext",
    ],
)

java_library(
    name = "text",
    sources = ["text/**/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        ":entities_and_filters",
        "3rdparty/jvm/com/google/guava",
        "src/java/com/twitter/common/text/token",
        "src/java/com/twitter/common/text/util:char-seq-util",
        "src/java/com/twitter/common_internal/text:text-penguin7",
        "src/java/com/twitter/common_internal/text/version",
        "src/java/com/twitter/search/common/relevance/features",
        "src/java/com/twitter/search/common/util/text",
        "src/java/com/twitter/search/common/util/text/regex",
        "src/thrift/com/twitter/search/common:indexing-java",
    ],
)

java_library(
    name = "scorers",
    sources = ["scorers/**/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        ":classifiers",
        ":config",
        ":entities_and_filters",
        "3rdparty/jvm/com/google/guava",
        "3rdparty/jvm/com/google/inject:guice",
        "3rdparty/jvm/com/twitter/elephantbird:core",
        "3rdparty/jvm/org/apache/hadoop:hadoop-client-default",
        "3rdparty/jvm/org/apache/zookeeper:zookeeper-client",
        "src/java/com/twitter/common/base",
        "src/java/com/twitter/common_internal/text/version",
        "src/java/com/twitter/search/common/encoding/features",
        "src/java/com/twitter/search/common/metrics",
        "src/java/com/twitter/search/common/relevance/features",
        "src/java/com/twitter/search/common/schema/base",
        "src/java/com/twitter/search/common/schema/earlybird",
    ],
)

java_library(
    name = "entities_and_filters",
    sources = [
        "entities/**/*.java",
        "filters/**/*.java",
    ],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/com/google/code/findbugs:jsr305",
        "3rdparty/jvm/com/google/guava",
        "3rdparty/jvm/com/google/inject:guice",
        "3rdparty/jvm/commons-lang",
        "3rdparty/jvm/geo/google:geoGoogle",
        "3rdparty/jvm/org/apache/commons:commons-lang3",
        "3rdparty/jvm/org/apache/lucene:lucene-core",
        "3rdparty/jvm/org/apache/thrift:libthrift",
        "3rdparty/jvm/org/slf4j:slf4j-api",
        "cuad/projects/ner/thrift/src/main/thrift:thrift-java",
        "decider/src/main/scala",
        "src/java/com/twitter/common/text/extractor",
        "src/java/com/twitter/common/text/language:locale-util",
        "src/java/com/twitter/common/text/pipeline",
        "src/java/com/twitter/common/text/token",
        "src/java/com/twitter/common/text/transformer",
        "src/java/com/twitter/common_internal/text:text-penguin7",
        "src/java/com/twitter/common_internal/text/version",
        "src/java/com/twitter/search/common/decider",
        "src/java/com/twitter/search/common/encoding/features",
        "src/java/com/twitter/search/common/metrics",
        "src/java/com/twitter/search/common/partitioning/snowflakeparser",
        "src/java/com/twitter/search/common/relevance/features",
        "src/java/com/twitter/search/common/schema/earlybird",
        "src/java/com/twitter/search/common/util/text",
        "src/thrift/com/twitter/search/common:indexing-java",
        "src/thrift/com/twitter/service/spiderduck/gen:metadata-store-java",
        "src/thrift/com/twitter/tweetypie:tweet-java",
        "util/util-core:scala",
    ],
)

java_library(
    name = "scores",
    sources = ["scores/**/*.java"],
    platform = "java8",
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/com/google/guava",
    ],
)
