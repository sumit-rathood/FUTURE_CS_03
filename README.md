# Task 3: API Security Risk Analysis

**Assessment date:** 23 October 2026  
**Target:** JSONPlaceholder public demo API  
**Assessment type:** Two read-only HTTP GET observations

## Deliverables

- [Assessment report](Report.pdf)
- [Markdown report](Report.md)
- [Sanitized request and response notes](evidence/api-get-evidence.txt)
- [HTTP request definitions](evidence/requests.http)
- [Postman collection](evidence/postman_collection.json)

## Scope and method

One GET request was made to each of /posts/1 and /users/1. Both returned HTTP 200. The responses contained synthetic demo records. Selected response headers and interpretation limits are recorded in the evidence log. Contact-shaped values from the synthetic user record are omitted.

No write methods, authentication or authorization checks, object-ID enumeration, input fuzzing, scanning, rate-limit stress, or load testing were performed.

## Findings

| ID | Observation | Rating |
|---|---|---|
| API-01 | Anonymous reads return documented demo records | Low / Informational |
| API-02 | Demo user schema contains contact-shaped fields | Low / Informational |
| API-03 | X-Powered-By: Express reveals a framework name | Low |

These are scoped observations, not confirmed vulnerabilities in the demo API. The assessment does not establish the security posture of a production service.

## Reproducibility

The included request file and Postman v2.1 collection contain only the two GET requests used for this review. They do not include write, enumeration, or stress-test operations.

## Canva report

Editable report design: [Open in Canva](https://www.canva.com/d/CDnvGezi3XYQpVB)

