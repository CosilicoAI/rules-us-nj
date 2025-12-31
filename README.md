# rules-us-nj

New Jersey rules encoded in Akoma Ntoso XML format.

## Structure

```
rules-us-nj/
├── statutes/                        # NJ Revised Statutes
│   ├── akn/                         # Akoma Ntoso XML format
│   │   ├── title-30/                # Institutions and Agencies
│   │   ├── title-43/                # Pensions and Retirement
│   │   ├── title-44/                # Poor (welfare programs)
│   │   ├── title-54/                # Taxation
│   │   └── title-54A/               # NJ Gross Income Tax Act
│   ├── title-54-taxation/           # Legacy placeholder
│   └── title-44-poor/               # Legacy placeholder
└── regulations/                     # NJ Administrative Code
```

## Titles

| Title | Name | Description |
|-------|------|-------------|
| 30 | Institutions and Agencies | Social services, welfare administration |
| 43 | Pensions and Retirement | Unemployment compensation, retirement |
| 44 | Poor | Public assistance, welfare programs |
| 54 | Taxation | Property tax, sales tax, other taxes |
| 54A | NJ Gross Income Tax Act | State income tax |

## Sources

- **NJ Statutes**: [NJ Legislature](https://lis.njleg.state.nj.us/nxt/gateway.dll?f=templates&fn=default.htm)
- **NJ Administrative Code**: [NJ Office of Administrative Law](https://www.state.nj.us/oal/)

## Format

All documents are encoded in [Akoma Ntoso](http://www.akomantoso.org/) XML format, the OASIS standard for legislative documents.

### Akoma Ntoso URIs

Documents follow the AKN URI pattern:
- Work: `/akn/us-nj/act/njrs/{section_id}`
- Expression: `/akn/us-nj/act/njrs/{section_id}/eng@{date}`
- Manifestation: `/akn/us-nj/act/njrs/{section_id}/eng@{date}/main.xml`

## Related Repositories

- [CosilicoAI/arch](https://github.com/CosilicoAI/arch) - Source document archive
- [CosilicoAI/rac](https://github.com/CosilicoAI/rac) - Rules as Code DSL
- [CosilicoAI/rac-us](https://github.com/CosilicoAI/rac-us) - US federal rules

## Contributing

To add new statute sections:

1. Fetch statute content from the NJ Legislature website
2. Convert to Akoma Ntoso XML using the `arch` converter
3. Place in appropriate `statutes/akn/title-{N}/` directory
4. Submit a pull request
