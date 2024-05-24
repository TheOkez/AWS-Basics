## Set Up a Static Website Using Amazon S3

### Step 1: Prepare Your Website Files
Ensure your website is designed as a collection of HTML, CSS, JavaScript, images, and any other assets. These files should be ready to upload to Amazon S3.

### Step 2: Create an S3 Bucket
1. Go to the Amazon S3 console: [https://console.aws.amazon.com/s3](https://console.aws.amazon.com/s3)
2. Click "Create bucket".
3. Enter a unique bucket name and choose the region.
4. Click "Create".

### Step 3: Upload Your Website Files to the Bucket
1. Open the bucket you created.
2. Click "Upload".
3. Select the files and folders from your local machine.
4. Click "Upload".

### Step 4: Enable Static Website Hosting
1. In the bucket properties, navigate to the "Static website hosting" section.
2. Choose "Use this bucket to host a website".
3. Enter the index document (e.g., `index.html`) and error document if applicable.
4. Click "Save".

### Step 5: Set Bucket Policy for Public Access
1. Still in the bucket properties, click on the "Permissions" tab.
2. Under "Bucket policy", click "Edit".
3. Add the following policy (replace `your-bucket-name` with your actual bucket name):

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        }
    ]
}

### Step 6:Access your website
After saving the bucket policy, you'll see a website endpoint URL in the "Static website hosting" section. It will be in the format of http://your-bucket-name.s3-website-region.amazonaws.com. Visit this URL in your browser to see your static website.

