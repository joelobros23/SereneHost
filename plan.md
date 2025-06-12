# Project Plan: SereneHost

**Description:** A simple and user-friendly web hosting platform built on Rails, providing domain management and basic hosting features.


## Development Goals

- [ ] Configure tailwindcss-rails gem and set up basic styling in application.tailwind.css, including colors, fonts, and basic layouts.
- [ ] Add model validations to the Domain model to enforce rules such as unique domain names per user, acceptable plan values (e.g., 'Basic', 'Premium', 'Enterprise'), and valid domain name format.
- [ ] Customize the domains scaffold views (index.html.erb, show.html.erb, _form.html.erb) to utilize Tailwind CSS classes for improved aesthetics and responsiveness.
- [ ] Implement authorization using Devise. Ensure only logged-in users can create, view, update, or delete their own domains. Modify the Domain model and controller to associate domains with the currently logged-in user.
- [ ] Restrict domain creation, editing, and deletion to only the associated user by adding `before_action` filters in the DomainsController and updating the view templates. Also, ensure domains are only displayed for the current user.
- [ ] Add a 'status' column to the domains table with possible values like 'Active', 'Inactive', 'Pending'. Implement functionality to change the status of a domain.
- [ ] Implement a basic pricing plan selection mechanism (e.g., a dropdown in the domain creation form) with associated resource limits (e.g., storage, bandwidth). Store resource limit data as constants or in a configuration file.
- [ ] Create a dashboard view for users to manage their domains and view resource usage. Use Tailwind CSS to style the dashboard.
- [ ] Implement a cron job or background worker (using Active Job or a gem like Sidekiq) to periodically check the status of domains and update their status based on certain criteria (e.g., payment status, resource usage).
- [ ] Add basic error handling and logging to improve the platform's stability and debuggability.
- [ ] Use dotenv-rails to manage environment variables for sensitive information like API keys or database credentials.
- [ ] Set up basic security measures, such as protecting against CSRF attacks and using strong password policies.
