+++
title = 'Assign roles'
weight = 7
+++

To allow the registered users specific tasks, the tenant admin needs to assign them specific roles. The KatApp uses a Role Based Access Control (RBAC). This means that each user is assigned a specific role. Each role has a set of access rights. Based on those access rights the KatApp-backend can verify, whether a user can perform a certain operation. These roles are listed as follows:

Role name           | Description                                    | Rights    
--------------------|------------------------------------------------|-----------
DashboardUser       | A user with access to the dashboard            | "AccessDashboard", "WebSocket", "ActionViewDisaster","ActionViewPatient", "ActionViewTriage"
DeviceUser          | A user with access to the app                  | "ActionViewPatient", "ActionViewTriage", "ActionCreateDisaster", "ActionCreatePatient", "ActionCreateTriage"
TenantAdmin         | A user with access to the tenant admin console | "AccessTenantConsole", "AccessDashboard", "ActionViewUser", "ActionDeleteUser", "ActionActivateUser", "ActionViewRole", "ActionCreateRole", "ActionAssignRole", "ActionCreateDevice", "ActionCreateDeviceToken"
KatAppOperator      | The global system operator. This role has access to the management console (only relevant for the operator clinic and not scope of the tenant admin console) | "AccessManagementConsole", "ActionViewTenant", "ActionActivateTenant"


The tenant has the option of assigning additional roles to the user on the [User management](/manageUsers) page. As you learned on the User activation page, the user was automatically assigned the "DashboardUser" user role when activating him. In the following example, the additional role "TenantAdmin" has been chosen to assign it to the user. Clicking on the Assign role button, the assignment is confirmed.

![assign-role-to-user](/assign-role-to-user.png)

