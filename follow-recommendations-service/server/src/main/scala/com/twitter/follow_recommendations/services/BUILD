scala_library(
    compiler_option_sets = ["fatal_warnings"],
    tags = ["bazel-compatible"],
    dependencies = [
        "finatra/inject/inject-app/src/main/scala",
        "finatra/inject/inject-core/src/main/scala",
        "finatra/inject/inject-server/src/main/scala",
        "finatra/inject/inject-thrift-client",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/base",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/candidate_sources/crowd_search_accounts",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/candidate_sources/real_graph",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/candidate_sources/recent_engagement",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/candidate_sources/sims",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/candidate_sources/stp",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/candidate_sources/top_organic_follows_accounts",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/clients/impression_store",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/feature_hydration/sources",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/predicates/sgs",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/rankers/ml_ranker/ranking",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/rankers/ml_ranker/scoring",
        "follow-recommendations-service/common/src/main/scala/com/twitter/follow_recommendations/common/utils",
        "follow-recommendations-service/server/src/main/scala/com/twitter/follow_recommendations/assembler/models",
        "follow-recommendations-service/server/src/main/scala/com/twitter/follow_recommendations/configapi/deciders",
        "follow-recommendations-service/server/src/main/scala/com/twitter/follow_recommendations/logging",
        "follow-recommendations-service/server/src/main/scala/com/twitter/follow_recommendations/products",
        "follow-recommendations-service/thrift/src/main/thrift:thrift-scala",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/pipeline/product",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/product/registry",
        "twitter-server/server/src/main/scala",
        "util/util-app/src/main/scala",
        "util/util-core:scala",
        "util/util-slf4j-api/src/main/scala",
    ],
)
