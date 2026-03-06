# Bruno - samtykke

Hjelpeprosjekt for å komme i gang med **Samtykke i Altinn 3** ved bruk av Bruno.

Før du kommer i gang, les deg opp på guiden til hvordan du skal ta i bruk Samtykke i Altinn 3:
https://docs.altinn.studio/nb/authorization/getting-started/consent/

Dette prosjektet inneholder ferdige API-forespørsler for å teste samtykkeflyten. For at forespørslene skal fungere mot Maskinporten, må du konfigurere miljøvariabler i Bruno basert på informasjonen fra din integrasjon i Samarbeidsportalen.

For detaljert veiledning om hvordan du henter disse verdiene og setter opp integrasjonen, se den offisielle dokumentasjonen:
[Altinn Studio - Maskinporten Developer Guide](https://docs.altinn.studio/nb/correspondence/getting-started/developer-guides/maskinporten/)

## Konfigurasjon

Du må angi følgende miljøvariabler i Bruno-miljøet ditt for å kunne generere tokens:

* **CLIENT_ID**: Din unike identifikator for integrasjonen fra Samarbeidsportalen.
* **KID**: Key ID for den offentlige nøkkelen som er registrert hos Maskinporten.
* **PEM**: Din private nøkkel (Private Key) i PEM-format.

## Hvordan bruke prosjektet

1. Importer mappen i Bruno.
2. Velg miljø "TT02"
3. Huk av "developer" mode, ellers får du ikke kjørt bakgrunnsscript. 
4. Legg til variablene `CLIENT_ID`, `KID`, og `PEM`.
5. Sørg for at `PEM`-variabelen inneholder hele nøkkelen, inkludert `-----BEGIN PRIVATE KEY-----` og `-----END PRIVATE KEY-----`.
