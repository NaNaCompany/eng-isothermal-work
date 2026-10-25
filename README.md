# 이상기체 등온팽창일 계산기

가역 등온 과정에서 이상기체가 한 압력-체적 일 계산

- Plan ID: E076
- App: https://nanalab.kr/eng-isothermal-work/
- Repository: https://github.com/NaNaCompany/eng-isothermal-work
- Formula: `W = nRT ln(V₂/V₁)`
- Output: 기체가 외부에 한 일 W

## Model

n,T,V₁,V₂>0. 가역·준정적 등온 이상기체 모델이다. 팽창은 양수, 압축은 음수이며 열교환량을 추가 출력하지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `1728.94389649319`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
