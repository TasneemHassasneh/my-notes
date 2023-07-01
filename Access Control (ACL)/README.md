# Access Control (ACL)

RBAC (Role-Based Access Control) is a method of access control that provides a flexible and scalable approach to managing permissions and access rights within a system. It assigns roles to users based on their responsibilities and authorizes their access to various resources and functionalities based on those roles.

Authentication determines the identity of a user, ensuring that they are who they claim to be. Authorization, on the other hand, determines what actions and resources a user can access or perform once they are authenticated.

In RBAC, roles are defined based on the user's job functions or responsibilities. Permissions are associated with each role, specifying what actions and resources the role is allowed to access. Users are then assigned one or more roles, and their access is determined by the permissions associated with those roles.

Three primary rules defined for RBAC are:

1. Role Assignment: Users are assigned one or more roles that align with their responsibilities and job functions.
2. Role Authorization: Roles are authorized to access certain resources and perform specific actions based on the permissions associated with those roles.
3. User Authorization: Users inherit the permissions associated with the roles they are assigned. They can access resources and perform actions based on the permissions granted to their roles.

To explain RBAC to a non-technical friend, you can use the analogy of a movie production set. Imagine a movie with various roles such as actors, directors, producers, and camera operators. Each role has specific responsibilities and access rights. The director can access the shooting location and give instructions to the actors, while the camera operator can access the camera equipment and capture the scenes. RBAC ensures that each person has the right role and access to perform their specific tasks, and they cannot access resources or perform actions outside their designated role.