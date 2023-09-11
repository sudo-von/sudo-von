<img src="svg/header.svg"  alt="Header image" />

# To-do: Use the same component like my portfolio.

```javascript
curl -X GET \
    -H "Content-Type: application/json" \
    "https://sudo-von.com/api/v1/user/username/sudo-von"
```

```typescript
{
    "id": "60603a5aaa037f0008ed81f9",
    "name": "Jesús Ángel Rodríguez Martínez",
    "email": "sudo.von.contact@gmail.com",
    "username": "sudo_von",
    "workplaces": [
        {
            "id": "649b478da7e8c4033849e8a7",
            "company": "Intel Corporation",
            "positions": ["Full stack engineer", "Cybersecurity researcher", "Frontend subject matter expert"]
        },
        {
            "id": "649b4806d1a3e5ddcdbd4c00",
            "company": "Tredicom",
            "positions": ["Full stack developer"]
        },
        {
            "id": "649b4806d1a3e5ddcdbd4c00",
            "company": "Evotek",
            "positions": ["Full stack developer"]
        },
    ],
    "about": {
        "title": "Computer systems engineer",
        "position": "Software engineer",
        "certifications": ["Certified ethical hacker and security professional (C|EHSP)"],
        "interests": ["Javascript fanatic", "Typescript enthusiast", "Passionate about ethical hacking"],
        "quote": "At first, dreams seem impossible, then improbable, and eventually inevitable"
    }
}
```

```tsx
import { FC } from 'react';
import { useUser } from '@user/hooks';
import { Loader, Error } from '@common/components';
import { Profile, Workplaces, About } from '@user/components';

type UserProps = {
    id: string;
};

const User: FC<UserProps> = ({ id }) => {
    const { data, isLoading, error } = useUser(id);

    if (isLoading) return <Loader />;

    if (error) return <Error message={error} />;

    const { name, email, username, workplaces, about } = data;

    return(
        <>
            <Profile name={name} email={email} username={username} />
            <Workplaces workplaces={workplaces} />
            <About about={about} />
        </>
    );
};

export default User;
```
