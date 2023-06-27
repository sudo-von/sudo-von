<img src="svg/header.svg"  alt="header" />

```javascript
curl -X GET \
    -H "Content-Type: application/json" \
    "https://sudo-von.com/api/v1/user/username/sudo-von"
```

```typescript
{
    "result": {
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
                "Frontend subject matter expert"
            ]
        },
        "title": "Computer systems engineer",
        "certifications": [
            "Certified ethical hacker and security professional (C|EHSP)"
        ]
    }
}
```

```tsx
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

<img src="https://lanyard.kyrie25.me/api/691166644395048960?waveColor=8B8BFA&waveSpotifyColor=B48EF7&gradient=7E37F9-B48EF7-E568C4&imgStyle=square"  />
