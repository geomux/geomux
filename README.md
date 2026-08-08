![geomux banner](images/geomux_banner.jpg)

## *Building and deploying AI-integrated systems on AWS*

### **<sub>AWS • MCP • LLM agentic workflows • Python • Linux</sub>**
<sub>*Deploying with - Terraform • Ansible • Docker*</sub>

<sub>*GIS foundation - Python geoprocessing • ETL pipelines • system automation*</sub>

> [!NOTE]
> Currently building MCP server/client systems and IaC stacks to deploy them.

**Agentic AI tooling, cloud-deployed**
<sub>*...a local CLI client, a remote MCP server, and the IaC that deploys it*</sub>

```mermaid
flowchart TB
    subgraph IAC["<b>IaC</b>"]
        direction LR
        P[["mcp-host-provision<br/><i>terraform</i>"]]:::iac
        CF[["mcp-host-configure<br/><i>ansible</i>"]]:::iac
        SB[["mcp-sandbox-setup<br/><i>docker</i>"]]:::iac
    end

    subgraph LHOST["<b>local host</b>"]
        direction LR
        U([user]):::me --> C["mcp-client-console"]:::pkg
        M(["<b>ollama</b><br/>local model"]):::model <-->|provider = local| C
    end

    subgraph RHOST["<b>remote host</b>"]
        direction LR
        N["nginx"]:::plumb --> S["mcp-server-remote"]:::pkg --> T["tools<br/>shell · files"]:::tools
    end

    API(["<b>Cloud API</b><br/>frontier model"]):::cloud

    IAC -.->|provisions & configures| RHOST
    C <-->|HTTPS| N
    C <-.->|provider = api| API

    classDef me fill:none,stroke:#4A4F4A,stroke-width:2px,color:#4A4F4A
    classDef pkg fill:#FFFDE7,stroke:#5A6B7A,stroke-width:2px,color:#424242
    classDef plumb fill:#757575,stroke:#4A4F4A,stroke-width:2px,color:#FFFFFF
    classDef tools fill:#FFF8E1,stroke:#8A7A60,stroke-width:2px,color:#424242
    classDef iac fill:#F5F5F5,stroke:#9E9E9E,stroke-width:2px,color:#424242
    classDef model fill:#E3F2FD,stroke:#476B50,stroke-width:2px,color:#263238
    classDef cloud fill:#E3F2FD,stroke:#5A6B7A,stroke-width:2px,color:#263238
    style RHOST fill:#EDE7F6,stroke:#2E4034,stroke-width:2px,color:#263238
    style LHOST fill:#E8EAF6,stroke:#2E4034,stroke-width:2px,color:#263238
    style IAC fill:#E0E0E0,stroke:#BDBDBD,stroke-width:6px,color:#424242

```

**Packages live on [PyPI](https://pypi.org/user/geomux/)** 
<sub>*...install with `pipx` and launch as apps straight from CLI!*</sub>

[`mcp-server-remote`](https://pypi.org/project/mcp-server-remote/)
[`mcp-client-console`](https://pypi.org/project/mcp-client-console/)


**Stacks accessible on [GitHub](https://github.com/geomux)** 
<sub>*...designed for IaC deployment via `terraform`•`ansible`•`docker`*</sub>

[`mcp-sandbox-setup`](https://github.com/geomux/mcp-sandbox-setup)
[`mcp-sandbox-pentest`](https://github.com/geomux/mcp-sandbox-pentest)
[`mcp-host-configure`](https://github.com/geomux/mcp-host-configure)
[`mcp-host-provision`](https://github.com/geomux/mcp-host-provision)

[`tf-state-backend`](https://github.com/geomux/tf-state-backend)

