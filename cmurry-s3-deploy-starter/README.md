# cmurry-s3-deploy (starter)

Lightweight static site to deploy to an S3 bucket using GitHub Actions.

## Quick Start
1. Create an S3 bucket (e.g., `cmurry-site`) and enable **Static website hosting**.
2. Add a bucket policy that allows public `s3:GetObject` on `arn:aws:s3:::<bucket>/*`.
3. In this repo's settings, add GitHub **Actions secrets**:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_REGION` (e.g., `us-east-1`)
   - `S3_BUCKET` (your bucket name, e.g., `cmurry-site`)
4. Push to `main` with changes in the `site/` folder. The workflow syncs the files to S3.
5. Visit your **Bucket website endpoint** to view the site.
