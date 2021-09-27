# &#937;: Omega
> Generic Format for OpenTelemetry Analysis<br>
> Inspired by [Sigma](https://github.com/SigmaHQ/sigma)

## What is Omega?

Omega is an exchange format for sharing analysis procedures that work with OpenTelemetry data.
With large in-built flexibility and expressiveness, it offers a tool for the community
to share ways of analyzing collected OpenTelemetry data.

## Why should I care about Omega?

- Analysis procedures are shareable with the community if present in Omega format
- Omega analysis procedures are vendor agnostic and can be used on any observability platform &#8594; no vendor lock-in

## How does it differ from OpenTelemetry?

OpenTelemetry can be seen as an effort to standardize the collection process of observability data - 
but does not deal with the subsequent step of analyzing the collected data.
Nevertheless, given its strict semantic conventions and a high degree of unification it also facilitates
data analysis. This is exactly where Omega comes into play by providing an exchange format for data analysis procedures. It is a tool that builds on the standardized nature of OpenTelemetry,
but is no alternative approach whatsoever compared to OpenTelemetry.

## How does Omega work?

The general approach of Omega can be summarized as follows:

`procedure in Omega format` &#8212; parsing &#8594; `abstract parse tree` &#8212; unparsing &#8594; `platform-specific query`

## Python OpenTelemetry Example

In the `./example` folder a Python OpenTelemetry example is provided.
For more details see the [official tutorial](https://opentelemetry-python.readthedocs.io/en/stable/getting-started.html).

To run the Jaeger backend via Docker:

```
docker run --name omega-jaeger \
    -p 127.0.0.1:16686:16686 \
    -p 127.0.0.1:6831:6831/udp \
    -d jaegertracing/all-in-one
```

## Resources

- [Jaeger data analytics with Jupyter notebooks](https://medium.com/jaegertracing/jaeger-data-analytics-with-jupyter-notebooks-b094fa7ab769)

## Supported Platforms

### In Progress

- Jaeger

## Todo

- Command-line tool to convert procedures to observability platform-specific queries.