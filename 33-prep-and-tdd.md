# Read33:   Login /> and Auth />
* what is role based access control? .
* react-cookies component .
* react-cookie library.

### *what is role based access control?(RBAC)*

- Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of 
the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

- EXAMPLES OF ROLE-BASED ACCESS CONTROL

Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an 
administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the 
organization. Permissions are allocated only with enough access as needed for employees to do their jobs.

- Some of the designations in an RBAC tool can include:

1. Management role scope – it limits what objects the role group is allowed to manage.
2. Management role group – you can add and remove members.
3. Management role – these are the types of tasks that can be performed by a specific role group.
4. Management role assignment – this links a role to a role group.

- Other options for user access may include:

1. Primary – the primary contact for a specific account or role.
2. Billing – access for one end-user to the billing account.
3. Technical – assigned to users that perform technical tasks.
4. Administrative – access for users that perform administrative tasks.

- BENEFITS OF RBAC :

1. Reducing administrative work and IT support.
2. Maximizing operational efficiency. 
3. Improving compliance.

- BEST PRACTICES FOR IMPLEMENTING RBAC

Implementing a RBAC into your organization shouldn’t happen without a great deal of consideration. There are a series of broad steps to bring the team onboard without causing unnecessary confusion and possible workplace irritations. Here are a few things to map out first.

1. Current Status: Create a list of every software, hardware and app that has some sort of security. For most of these things, it will be a password. However, you may also want to list server rooms that are under lock and key. Physical security can be a vital part of data protection. Also, list the status of who has access to all of these programs and areas. This will give you a snapshot of your current data scenario.
2. Current Roles: Even if you do not have a formal roster and list of roles, determining what each individual team member does may only take a little discussion. Try to organize the team in such a way that it doesn’t stifle creativity and the current culture (if enjoyed).
3. Write a Policy: Any changes made need to be written for all current and future employees to see. Even with the use of a RBAC tool, a document clearly articulating your new system will help avoid potential issues.
4. Make Changes: Once the current security status and roles are understood (not to mention a policy is written), it’s time to make the changes.
5. Continually Adapt: It’s likely that the first iteration of RBAC will require some tweaking. Early on, you should evaluate your roles and security status frequently. Assess first, how well the creative/production process is working and secondly, how secure your process happens to be.


For more details see [what is role based access control?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more).

### *react-cookies component*

- Install

           npm install react-cookies --save

To be able to access user cookies while doing server-rendering, you can use plugToRequest or setRawCookie.

#### API

- .load(name, [doNotParse])

Load the cookie value.

Returns undefined if the cookie does not exist.

Deserialize any cookie starting with { or [ unless dotNotParse is true.

- .loadAll()

Load all available cookies.

Returns an object containing all cookies.

- .select([regex])

Find all the cookies with a name that match the regex.

Returns an object with the cookie name as the key.

- .remove(name, [options])

Remove a cookie.

For more details see  [react-cookies component](https://www.npmjs.com/package/react-cookies).

### *react-cookie library*

- Getting started

         npm install react-cookie

- <CookiesProvider />

Set the user cookies

On the server, the cookies props must be set using req.universalCookies or new Cookie(cookieHeader)

- useCookies([dependencies])

Access and modify cookies using React hooks.

                  const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);

- dependencies (optional)

Let you optionally specify a list of cookie names your component depend on or that should trigger a re-render. If unspecified, it will render on every cookie change.

- cookies

Javascript object with all your cookies. The key is the cookie name.

- setCookie(name, value, [options])

Set a cookie value                  

- removeCookie(name, [options])

Remove a cookie

For more details see [react-cookie library](https://www.npmjs.com/package/react-cookie).


