# Django Terraform UI Application

Create a Django application that provides a web-based user interface for configuring, managing, and executing Terraform deployments.

## Requirements

1. Create a Django application that can be deployed as a Docker container in AWS Elastic Beanstalk.
2. Implement a dynamic UI system that can adapt to arbitrary Terraform module inputs and outputs.
3. Support the following user flows:
   - Module selection
   - Configuration of all module parameters with appropriate input validation
   - Plan preview before execution
   - Plan approval/rejection workflow
   - Apply execution with real-time status updates
   - State inspection and resource exploration
4. Integrate with AWS CodeBuild for executing Terraform operations:
   - One job for `terraform plan`
   - Separate job for `terraform apply`
5. Create a RESTful API to interact with the Terraform Operations API service.
6. Implement user authentication and authorization with role-based access control.
7. Support WebSocket connections for real-time updates on plan and apply operations.

## Docker Configuration

1. Create a Dockerfile that sets up the Django application.
2. Ensure the container can access AWS services via instance profile.
3. Include health check endpoints for Elastic Beanstalk.
4. Configure proper environment variable handling for production settings.

## User Interface

1. Develop a responsive, modern UI using Django templates with Bootstrap or a similar framework.
2. Implement dynamic form generation based on Terraform module input variables.
3. Create visualization components for displaying Terraform plans and state.
4. Design dashboard views for monitoring active and completed Terraform operations.
5. Create UI components for approval workflows with comments and audit trail.

## Security Considerations

1. Implement secure handling of AWS credentials.
2. Ensure proper validation of all user inputs.
3. Implement CSRF protection and other Django security best practices.
4. Create logging for all Terraform operations for audit purposes.

## Testing

1. Write unit tests for core functionality.
2. Create integration tests for AWS service interactions.
3. Implement end-to-end tests for critical user flows.
