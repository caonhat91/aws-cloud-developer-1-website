# Deploy Static Website on AWS

In this project, you will deploy a static website to AWS using S3, CloudFront, and IAM.

The files included are: 

index.html - The Index document for the website.
/img - The background image file for the website.
/vendor - Bootssrap CSS framework, Font, and JavaScript libraries needed for the website to function.
/css - CSS files for the website.


## Project

1. AWS Region
- US East (N. Virginia) us-east-1

2. S3:

- **Bucket name**: my-17f1810c37fe-bucket
- **Destination**: s3://my-17f1810c37fe-bucket

```json
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Sid":"AddPerm",
      "Effect":"Allow",
      "Principal": "*",
      "Action":["s3:GetObject"],
      "Resource":["arn:aws:s3:::my-17f1810c37fe-bucket/*"]
    }
  ]
}
```

- **Bucket website endpoint**: [http://my-17f1810c37fe-bucket.s3-website-us-east-1.amazonaws.com](http://my-17f1810c37fe-bucket.s3-website-us-east-1.amazonaws.com)

3. CloudFront

- **Origin domain**: my-17f1810c37fe-bucket.s3-website-us-east-1.amazonaws.com
- **Name**: my-17f1810c37fe-bucket.s3-website-region.amazonaws.com
- **Distribution domain name**: [https://d3omv0qt931b1v.cloudfront.net](https://d3omv0qt931b1v.cloudfront.net)


## Test URL

- **CloudFront domain name**: [https://d3omv0qt931b1v.cloudfront.net](https://d3omv0qt931b1v.cloudfront.net)

- **Bucket website endpoint**: [http://my-17f1810c37fe-bucket.s3-website-us-east-1.amazonaws.com](http://my-17f1810c37fe-bucket.s3-website-us-east-1.amazonaws.com)

- **S3 object URL**: [https://my-17f1810c37fe-bucket.s3.amazonaws.com/index.html](https://my-17f1810c37fe-bucket.s3.amazonaws.com/index.html)