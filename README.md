# domain1securearchitecture
Domain 1 Secure Architecture Project
## Progress Log

### Phase 1 — S3 Setup ✅
- Created private S3 bucket (cduff-secure-project)
- Blocked all public access (all 4 BPA settings)
- Enabled versioning and AES-256 encryption
- Uploaded index.html and error.html

### Phase 2 — CloudFront + OAC ✅
- Created Origin Access Control (OAC) scoped to this distribution
- Created CloudFront distribution with HTTPS enforced
- Applied bucket policy granting only this CloudFront distribution access to S3
- Verified: CloudFront 200, direct S3 403, HTTP→HTTPS 301, edge cache Hit
