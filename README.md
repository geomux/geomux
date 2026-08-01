![geomux banner](images/geomux_banner.jpg)

### *Geospatial Data Engineer*
<sub>*Building and deploying AI-integrated systems on AWS*</sub>

**GIS, AWS, FME, CAD, Python, Linux, ETL pipelines, MCP, LLM agentic workflows.**


<sub>*...how it all fits together:*</sub>

```mermaid
flowchart LR
    subgraph RHOST["remote host"]
        direction LR
        N["nginx"]:::plumb --> S["mcp-server-remote"]:::pkg --> T["tools<br/>shell · files"]:::tools
    end

    subgraph LHOST["local host"]
        direction LR
        U([user]):::me --> C["mcp-client-console"]:::pkg
        M(["<b>ollama<b><br/>local model"]):::model <-->|provider = local| C
    end

    API(["<b>Anthropic API"<b><br/>frontier model]):::cloud
    C <-->|HTTPS| N
    C <-.->|provider = api| API
    IAC[["<b>IaC<b><br/>docker · ansible · terraform"]]:::iac -.->|provisions| RHOST

    classDef me fill:none,stroke:#4A4F4A,stroke-width:2px,color:#4A4F4A
    classDef pkg fill:#FFFDE7,stroke:#5A6B7A,stroke-width:2px,color:#424242
    classDef plumb fill:#757575,stroke:#4A4F4A,stroke-width:2px,color:#FFFFFF
    classDef tools fill:#FFF8E1,stroke:#8A7A60,stroke-width:2px,color:#424242
    classDef iac fill:#E0E0E0,stroke:#BDBDBD,stroke-width:6px,color:#424242
    classDef model fill:#E3F2FD,stroke:#476B50,stroke-width:2px,color:#263238
    classDef cloud fill:#E3F2FD,stroke:#5A6B7A,stroke-width:2px,color:#263238
    style RHOST fill:#EDE7F6,stroke:#2E4034,stroke-width:2px,color:#263238
    style LHOST fill:#E8EAF6,stroke:#2E4034,stroke-width:2px,color:#263238
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
