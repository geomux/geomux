![geomux banner](images/geomux_banner.jpg)

### *Geospatial Data Engineer*
<sub>*Building and deploying AI-integrated systems on AWS*</sub>

**GIS, AWS, FME, CAD, Python, Linux, ETL pipelines, MCP, LLM agentic workflows.**


<sub>*...how it all fits together:*</sub>

```mermaid
flowchart LR
    subgraph HOST["remote host"]
        direction LR
        N["nginx"]:::plumb --> S["mcp-server-remote"]:::pkg --> T["tools<br/>shell · files"]:::tools
    end

    U([you]):::me --> C["mcp-client-console"]:::pkg
    C -->|HTTPS| N
    IAC["docker · ansible · terraform"]:::iac -.->|provisions| HOST

    classDef me fill:none,stroke:#4A4F4A,stroke-width:2px,color:#4A4F4A
    classDef pkg fill:#33414F,stroke:#5A6B7A,stroke-width:2px,color:#E8EAE6
    classDef plumb fill:#24272A,stroke:#4A4F4A,stroke-width:2px,color:#D6D8D2
    classDef tools fill:#6E5F49,stroke:#8A7A60,stroke-width:2px,color:#F2EEE6
    classDef iac fill:#2E4034,stroke:#476B50,stroke-width:2px,color:#E2EAE0
    style HOST fill:#1C241E,stroke:#2E4034,stroke-width:2px,color:#C9CFC4
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
