# SEO Schema Templates (JSON-LD)

Ready-to-use [schema.org](https://schema.org) JSON-LD templates for the structured data types that matter most for Google rich results, local SEO and AI search (Google AI Overviews, ChatGPT, Perplexity).

Copy a template, replace the example values with your real business data, and add it to your page.

## Templates

| File | Schema type | Use it on |
|---|---|---|
| [local-business.json](templates/local-business.json) | `LocalBusiness` | Home or contact page of a local business (plumber, dentist, roofer, salon) |
| [organization.json](templates/organization.json) | `Organization` | Home page of a brand, SaaS or online company |
| [article.json](templates/article.json) | `Article` | Blog posts and guides |
| [faq.json](templates/faq.json) | `FAQPage` | Pages with a visible question and answer section |
| [product.json](templates/product.json) | `Product` | Ecommerce product pages |
| [breadcrumb.json](templates/breadcrumb.json) | `BreadcrumbList` | Any page below the home page |

## How to add it to a page

Wrap the JSON in a script tag inside `<head>` or `<body>`:

```html
<script type="application/ld+json">
{ ...paste the template here... }
</script>
```

**WordPress:** use a header/footer code plugin, or the custom schema option in Rank Math or Yoast. Don't add a type your SEO plugin already outputs, or you'll get duplicates.

**Shopify / Wix:** most themes already output `Product` and `Organization`. Check the page source first, then add only what is missing.

## Rules that keep schema valid

1. Every value in the schema must also be visible on the page. Don't mark up reviews, prices or FAQs that users can't see.
2. Use the same business name, address and phone (NAP) as your Google Business Profile and citations.
3. Use one `@id` per entity and reuse it, so Google can connect your pages to one business.
4. Only use `aggregateRating` for reviews collected on your own site. Google ignores self-serving review markup for `LocalBusiness` and `Organization`.
5. `FAQPage` rich results are now limited to well-known government and health sites. The markup is still valid and helps search engines and AI tools understand your answers.

## Test before you publish

1. [Google Rich Results Test](https://search.google.com/test/rich-results): checks eligibility for rich results.
2. [Schema Markup Validator](https://validator.schema.org/): checks the schema.org syntax.
3. Google Search Console → **Enhancements**: shows errors on live pages after Google crawls them.

## License

MIT. Free to use for client and personal projects.
