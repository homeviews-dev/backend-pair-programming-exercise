# Backend Pair Programming Exercise

## Overview
In this exercise, we will be pair-programming on a Laravel project, focusing on adding a new endpoint and solving a bug. You will be given access to this repository 48 hours before your interview. During this time, please clone the project and set up your local environment. Do not complete the task ahead of time, as we will solve it together. This will assess your collaboration skills and give you an opportunity to demonstrate your problem-solving abilities. At the end of the session, we will review our work and dive deeper into the concepts discussed during the exercise.

## Installation Instructions

To complete this exercise, you will need a Laravel PHP development environment with **PHP 8.2** or higher. **Laravel Sail** is already set up by default, allowing you to easily use Docker for this project.

1. **Clone the repository**  
   Clone this repository to your local machine.  
   ```bash
   git clone <repository-url>
   cd <repository-directory>

2. **Set up environment variables**  
   Copy the example environment file to create a new `.env` file:
   ```bash
   cp .env.example .env

3. **Install dependencies**  
   Run the following command to install the necessary dependencies:  
   ```bash
   composer install

4. **Start the development environment**  
   Use Laravel Sail to initialize the local development environment, including the required database, by running:
   ```bash
   ./vendor/bin/sail up -d --build
   ```
   > Note: The --build flag ensures that Docker containers are rebuilt if necessary. It is recommended to include this flag during the first setup to avoid any potential issues with outdated images.

5. **Run the tests**  
   Once your environment is up and running, you can run the project tests by using the following command:
   ```bash
   ./vendor/bin/sail test
   ```
   
   At this point, you should see a test failure that looks like this:
   ```
   FAILED  Tests\Feature\DevelopmentServiceInterfaceTest > development service returns by postcode
   BindingResolutionException
   Target [App\Contracts\DevelopmentServiceInterface] is not instantiable.
   ```

   **This error is expected and indicates that your environment is correctly set up.** This will be our starting point for the pair programming session.
