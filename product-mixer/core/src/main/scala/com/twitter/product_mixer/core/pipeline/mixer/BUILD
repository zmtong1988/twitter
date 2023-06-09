scala_library(
    sources = ["*.scala"],
    compiler_option_sets = ["fatal_warnings"],
    platform = "java8",
    strict_deps = True,
    tags = ["bazel-compatible"],
    dependencies = [
        "3rdparty/jvm/javax/inject:javax.inject",
        "product-mixer/component-library/src/main/scala/com/twitter/product_mixer/component_library/model/candidate",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/feature/featurestorev1",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/candidate_source",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/common/alert",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/feature_hydrator",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/filter",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/marshaller",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/premarshaller",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/selector",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/side_effect",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/model/common",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/model/marshalling/request",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/pipeline",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/pipeline/candidate",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/quality_factor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/async_feature_map_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/candidate_pipeline_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/domain_marshaller_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/gate_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/pipeline_result_side_effect_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/quality_factor_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/query_feature_hydrator_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/selector_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/transport_marshaller_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/util",
        "stitch/stitch-core",
    ],
    exports = [
        "3rdparty/jvm/javax/inject:javax.inject",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/candidate_source",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/common/alert",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/feature_hydrator",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/filter",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/marshaller",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/premarshaller",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/selector",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/functional_component/side_effect",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/model/common",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/model/marshalling/request",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/pipeline",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/pipeline/candidate",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/quality_factor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/candidate_pipeline_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/domain_marshaller_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/gate_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/pipeline_result_side_effect_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/quality_factor_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/query_feature_hydrator_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/selector_executor",
        "product-mixer/core/src/main/scala/com/twitter/product_mixer/core/service/transport_marshaller_executor",
        "stitch/stitch-core",
    ],
)
