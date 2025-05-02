# secure-website-hosting-with-SSL-certificats-using-S3-Route-53-ACM-and-cloud-front
Host a satic web site on a s3 bucket 
purchace a domain from amazon or third party domain provider. here I used hostinger as my domain provider.( I have created a acount in hostinger and purchase domain with the name similer to my S3 bucket name. )
Change the bucketpolicy to get public access.
Then go to the route 53 and creat hosted zone. enter the domain name, select public hosted tone and create hosted zone.
copy the name server in route 53 in to the hostinger by editing name server in hostinger and save the changes.
now go to AWS certificate manager to craete SSL certificate. Here request a certificate and select validation with DNS validation.
to validate certificate, have to create CNAME record in route 53.
now go to the cloud front and create cloudfront  distribution and attach the SSL certificate in to cloudfront distribution.
once it deployd you can loard the website using cloudfront ARN.
go to the route 53 and craet a new record which is A record to use our Alias and route traffic to cloudfront distribution.
once it success go to route 53 and copy the record name and using that you can loard the secure website. in my case it is   niroshajayasundaracloudresumechallenge.site
