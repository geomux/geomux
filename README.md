![geomux banner](images/geomux_banner.jpg)

### *Geospatial Data Engineer*
<sub>*Building and deploying AI-integrated systems on AWS*</sub>

**GIS, AWS, FME, CAD, Python, Linux, ETL pipelines, MCP, LLM agentic workflows.**


<sub>*...how it all fits together:*</sub>

```mermaid
flowchart LR
    U([you]):::me --> C["mcp-client-console"]:::pkg
    C -->|HTTPS| N["nginx"]:::infra
    N --> S["mcp-server-remote"]:::pkg
    S --> T["tools<br/>shell · files"]:::edge
    D["docker · ansible · terraform"]:::iac -.->|provisions| N

    classDef me fill:none,stroke:#4DA3FF,stroke-width:2px,color:#4DA3FF
    classDef pkg fill:#0B3D91,stroke:#4DA3FF,stroke-width:2px,color:#FFFFFF
    classDef infra fill:#16233D,stroke:#4DA3FF,stroke-width:1px,color:#CFE3FF
    classDef edge fill:#A8321B,stroke:#FC3D21,stroke-width:2px,color:#FFFFFF
    classDef iac fill:none,stroke:#5A7BA6,stroke-width:1px,color:#8FB3D9
```


**Packages live on [PyPI](https://pypi.org/)** 
<sub>*...install with `pipx` and launch as apps straight from CLI!*</sub>

[`mcp-server-remote`](https://pypi.org/project/mcp-server-remote/)
[`mcp-client-console`](https://pypi.org/project/mcp-client-console/)


**Stacks accessible on [GitHub](https://github.com/)** 
<sub>*...designed for IaC deployment via `terraform`*</sub>

[`mcp-sandbox-setup`](https://github.com/geomux/mcp-sandbox-setup)
[`mcp-host-configuration`](https://github.com/geomux/mcp-host-configuration)
[`mcp-host-provision`](https://github.com/geomux/mcp-host-provision)

[`terraform-backend`](https://github.com/geomux/terraform-backend)
