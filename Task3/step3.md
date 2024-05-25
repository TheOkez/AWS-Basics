1. **Log in to the AWS Management Console**: Go to the AWS Management Console and log in to your AWS account.

2. **Open the Lambda Console**: Once logged in, navigate to the Lambda service by either searching for "Lambda" in the AWS services search bar or by finding it under "Compute" in the services menu.

3. **Create a Function**: Click on the "Create function" button.

4. **Choose Authoring Option**: You'll be prompted to choose an authoring option. You can author your Lambda function from scratch or choose from existing blueprints or samples. Let's choose "Author from scratch" for this example.

5. **Configure Function**: Fill in the following details:
   - **Function name**: Give your function a descriptive name.
   - **Runtime**: Choose the runtime for your function (e.g., Python 3.8, Node.js 12.x, etc.).
   - **Execution role**: Choose an existing role with necessary permissions or create a new role.

6. **Write Code**: In the code editor, you can write your Lambda function code. For example, if you're using Python, you can write something like this:
   ```python
   def lambda_handler(event, context):
       # Your code here
       return {
           'statusCode': 200,
           'body': 'Hello from Lambda!'
       }

7. **Configure Function:** Scroll down to configure additional settings such as environment variables, timeout, memory, etc.

8. **Review and Create:** Review your configuration settings, and then click "Create function" to create your Lambda function.

9.** Testing:** Once your function is created, you can test it using the Lambda console's built-in testing feature or by invoking it using the AWS SDK or CLI.
