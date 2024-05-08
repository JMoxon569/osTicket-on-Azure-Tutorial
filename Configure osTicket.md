**Configure osTicket**

**Introduction**

This section provides detailed instructions on how to configure osTicket after its installation on a virtual machine. We will cover the administrative setup, including how to add users, agents, and teams.

**Accessing the Administrative Panel**

- After installing osTicket, access the administrative dashboard by navigating to your osTicket URL followed by **/scp**. For example, **http://<Your-VM-IP>/scp**.
- Log in using the admin credentials you created during the installation process.

**Step 1: Configuring System Settings**

- Once logged in, navigate to **Admin Panel > Settings**.
- Here, you can configure general settings for your help desk, such as the default system email, system language, and operational hours.
- Save your changes by clicking the **Save Changes** button at the bottom of the page.

**Step 2: Adding Departments**

- Go to **Admin Panel > Manage > Departments**.
- Click on **Add New Department**.
- Enter the necessary information such as department name and the manager of the department.
- Assign an outgoing email for communication from this department.
- Save your department by clicking **Add**.

**Step 3: Adding Agents**

- Navigate to **Admin Panel > Agents**.
- Click on **Add New Agent**.
- Fill in the agent's details including their name, email, and assigned department.
- Set permissions for the agent based on their role and responsibilities.
- Click **Create** to add the agent to your system.

**Step 4: Creating Teams**

- Go to **Admin Panel > Manage > Teams**.
- Click on **Add New Team**.
- Provide a name for the team and select the team lead from existing agents.
- Assign members to the team by selecting agents.
- Click **Save** to finalize the creation of the team.

**Step 5: Setting Up Email Settings**

- Navigate to **Admin Panel > Emails**.
- Click on **Add New Email** to set up a new email address that osTicket will use to communicate with users.
- Configure SMTP settings if you are using an external mail service.
- Verify the email setup to ensure that outgoing and incoming emails are functioning correctly.

**Conclusion**

You have now successfully configured the basic settings of osTicket. Your ticketing system is ready to handle tickets with your customized settings and user roles. The system is set up with departments, agents, and teams that reflect your organizational structure.

