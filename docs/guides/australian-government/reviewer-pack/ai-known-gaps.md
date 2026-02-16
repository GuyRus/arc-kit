# Remaining Known Gaps

1. **Defence-specific public policy gap**
   - No public Defence-wide equivalent to UK JSP 936 identified in corpus.
   - Handling: AU defence pathway template includes explicit `SOURCE_GAP` entries and requires internal Defence policy overlay before production use.

2. **BuyICT extraction limitation**
   - BuyICT AI procurement page is JS-rendered and not fully captured by static extraction.
   - Handling: AU templates rely on DTA/Finance/OAIC/PSPF sources with explicit TODO where organisation-specific procurement detail is required.

3. **Automated test tooling availability**
   - `pytest` not installed in current environment.
   - Handling: syntax/parse checks completed; runtime test limitation documented.
