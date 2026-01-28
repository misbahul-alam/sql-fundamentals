# GRANT & REVOKE

GRANT and REVOKE control user access to database objects.

## GRANT

- Gives a user permission to perform actions (SELECT, INSERT, etc.).
- Example:

```sql
GRANT SELECT, INSERT ON employees TO misbahul_user;
```

_Allows misbahul_user to view and add employees._

## REVOKE

- Removes permissions from a user.
- Example:

```sql
REVOKE INSERT ON employees FROM misbahul_user;
```

_misbahul_user can no longer add employees._

## Why Use Permissions?

- Protects sensitive data
- Prevents accidental or malicious changes

## Common Mistakes

- Granting too many permissions
- Forgetting to revoke access when no longer needed

## Best Practices

- Grant only the permissions needed (principle of least privilege)
- Review permissions regularly

## Practice Challenge

1. Grant SELECT permission on the employees table to a user named misbahul_user.
2. Revoke INSERT permission from the same user.
