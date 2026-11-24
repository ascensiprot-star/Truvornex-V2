# Target Repository Structure

Logical target only; inspect existing repo and use ADRs for material changes.

```text
truvornex/
├── apps/mobile_flutter/{lib/app,lib/core,lib/design_system,lib/features,lib/platform,test}
├── services/{api,worker,scheduled_jobs}
├── packages/{api_contracts,domain_shared,country_profiles,provider_adapters}
├── backend/src/{modules,application,infrastructure,api,jobs}
├── database/{migrations,seeds,integrity_checks}
├── intelligence/{simon_orchestrator,retrieval,tools,evaluations}
├── integrations/{identity,payments,invoicing,notifications,maps}
├── infrastructure/{environments,deployment,observability,security}
├── contracts/{openapi,events,schemas}
├── docs/{adr,runbooks,compliance_evidence}
└── tools/
```

Do not create empty directories merely to match this diagram. Every module needs owner, interface, tests, dependency policy. Folder names do not mandate new technologies or processes.
