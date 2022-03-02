# SeldonIO

Seldon core converts your ML models (Tensorflow, Pytorch, H2o, etc.) or language wrappers (Python, Java, etc.) into production REST/GRPC microservices.

Seldon handles scaling to thousands of production machine learning models and provides advanced machine learning capabilities out of the box including Advanced Metrics, Request Logging, Explainers, Outlier Detectors, A/B Tests, Canaries and more.



#### Deploy your model using pre-packaged model servers[¶](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/github-readme.html#deploy-your-model-using-pre-packaged-model-servers) <a href="#deploy-your-model-using-pre-packaged-model-servers" id="deploy-your-model-using-pre-packaged-model-servers"></a>

We provide optimized model servers for some of the most popular Deep Learning and Machine Learning frameworks that allow you to deploy your trained model binaries/weights without having to containerize or modify them.



**Send API requests to your deployed model**[**¶**](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/github-readme.html#send-api-requests-to-your-deployed-model)

Every model deployed exposes a standardised User Interface to send requests using our OpenAPI schema.

This can be accessed through the endpoint `http://<ingress_url>/seldon/<namespace>/<model-name>/api/v1.0/doc/` which will allow you to send requests directly through your browser





These are Seldon Core main components:

* Reusable and non-reusable [model servers](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#e2e-serving-with-model-servers)
* [Language Wrappers](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#language-wrappers) to containerise models
* [SeldonDeployment](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#seldondeployment-crd) CRD and [Seldon Core Operator](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#seldon-core-operator)
* [Service Orchestrator](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#service-orchestrator) for advanced inference graphs

as well as integration with third-party systems:

* Kubernetes Ingress integration with [Ambassador](https://www.getambassador.io) and [Istio](https://istio.io)
* [Metrics](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#metrics-with-prometheus) with [Prometheus](https://prometheus.io)
* [Tracing](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#distributed-tracing-with-jaeger) with [Jaeger](https://www.jaegertracing.io)
* [Endpoint Documentation](https://docs.seldon.io/projects/seldon-core/en/latest/workflow/overview.html#endpoint-documentation) with [OpenApi](https://swagger.io/docs/specification/about/)

To learn more about Seldon refer below links:

[https://docs.seldon.io/projects/seldon-core/en/latest/index.html\
docs.seldon.io\
https://github.com/SeldonIO/seldon-core\
https://github.com/SeldonIO/MLServer\
](https://docs.seldon.io/projects/seldon-core/en/latest/index.htmldocs.seldon.iohttps://github.com/SeldonIO/seldon-corehttps://github.com/SeldonIO/MLServer)
