# Email Magic Link
Outline supports authentication via email “magic link”. Using this method users will enter their email address on the login page and be sent a single-use, time-restricted link to their email address which they can click to sign-in without a password.

This is primarily intended for guests, however there are no additional restrictions on users that sign-in using this method and you could use this for all users if preferred.

## Configuration

Email authentication is enabled by default if you have correctly setup an [SMTP provider](https://app.getoutline.com/doc/smtp-cqCJyZGMIB) to send emails from the app. (Required in the KubeSail Setup)

You must also ensure the "Allow email authentication” is enabled under **Settings → Security**, it should look like the following:

![](https://outline-production-attachments.s3-accelerate.amazonaws.com/uploads/292079f8-0319-4111-bb5b-315e8ae8f14e/28615484-5cef-41e7-8360-c4fe65478292/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4EOUDTOVUICLPZ4P%2F20220901%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220901T192710Z&X-Amz-Expires=3600&X-Amz-Signature=919515c13734d70d2a99af516286da6cd2de71f92d54712e5b084d3615d4fd28&X-Amz-SignedHeaders=host&response-content-disposition=attachment)