# OMEGA
> Generic Format for OpenTelemetry Analysis

## Python Example

In the `./example` folder a Python OpenTelemetry example is provided.
For more details see the [official tutorial](https://opentelemetry-python.readthedocs.io/en/stable/getting-started.html).

To run the Jaeger backend via Docker:

```
docker run --name omega-jaeger \
    -p 127.0.0.1:16686:16686 \
    -p 127.0.0.1:6831:6831/udp \
    -d jaegertracing/all-in-one
```

## Todo

...