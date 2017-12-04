# Authorization

<!--
Strictly speaking, this is not true. In fact, we need to clamp down on
authorization for all tokens.
-->
FOSSA allows users to create API tokens to access the API. Each token will only
allow access to projects belonging to the user's organization.

To create a token, visit your Account Settings > Integrations > API.

FOSSA uses the `token` scheme for authorization:

`Authorization: token $YOUR_TOKEN_HERE`
