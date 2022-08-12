```javascript
Request URL: https://sudo-von.com:3000/users/username/von
Request Method: GET
Status Code: 200 OK
Response:
{   
    "id" : "60603a5aaa037f0008ed81f9",
    "username": "sudo-von",
    "name" : "Jesús Ángel Rodríguez Martínez",
    "age" : 25,
    "job": {
        "company" : "Intel Corporation",
        "positions": ["Software developer", "Software application development engineer", "Cyber security researcher"],
        "location" : "Guadalajara, Jalisco"
    },
    "title": "Computer systems engineer",
    "certifications" : ["C|EHSP de Ethical Hacking & Security Professional"]
}
```

```typescript
import { FC } from 'react';
import { UserProps } from '@props';
import {
    User,
    Workplace,
    Achievements
} from '@components';

interface ProfileProps {
    user: UserProps;
};

const Profile:FC<ProfileProps> = ({ user }): JSX.Element => {
    const { username, name, age, job, title, certifications } = user;
    return(
        <>
            <User
                username={username}
                name={name}
                age={age}
            />
            <Workplace
                job={job}
            />
            <Achievements
                title={title}
                certifications={certifications}
            />
        </>
    );
};

export default Profile;
```
