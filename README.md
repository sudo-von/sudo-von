```typescript
{
    "request": {
        "url": "https://sudo-von.com/api/v1/user/username/sudo-von",
        "method": "GET",
    },
    "response": {
        "status": {
            "code": 200,
            "message": "OK",
        },
    },
    "data": {
        "id": "60603a5aaa037f0008ed81f9",
        "name": "Jesús Ángel Rodríguez Martínez",
        "email": "sudo.von.contact@gmail.com",
        "username": "sudo-von",
        "age": 26,
        "workplace": {
            "company": "Intel Corporation",
            "location": "Mexico",
            "positions": [
                "Full stack engineer",
                "Cybersecurity researcher",
                "Frontend subject matter expert",
            ],
        },
        "title": "Computer systems engineer",
        "certifications": [
            "Certified ethical hacker and security professional (C|EHSP)"
        ],
    }
}
```

```typescript
import { FC } from 'react';
import { useUser } from '@user/hooks';
import { Loader, Error } from '@components';
import { Profile, Workplace, Achievements } from '@user/components';

type UserProps = {
    id: string;
};

const User: FC<UserProps> = ({ id }) => {
    const { data, isLoading, error } = useUser(id);

    if (isLoading) return <Loader />;

    if (error) return <Error message={error} />;

    const { name, email, username, age, workplace, title, certifications } = data;

    const { company, location, positions } = workplace;

    return(
        <>
            <Profile
                age={age}
                name={name}
                email={email}
                username={username}
            />
            <Workplace
                company={company}
                location={location}
                positions={positions}
            />
            <Achievements
                title={title}
                certifications={certifications}
            />
        </>
    );
};

export default User;
```
