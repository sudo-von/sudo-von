<h2 align="center">About Me</h2>

![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white)

![Webpack](https://img.shields.io/badge/webpack-%238DD6F9.svg?style=for-the-badge&logo=webpack&logoColor=black)

![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)


```javascript
Request URL: http://sudovon.com:3000/users/username/von
Request Method: GET
Status Code: 200 OK
Response:
{   
    "id" : "60603a5aaa037f0008ed81f9",
    "username": "von",
    "name" : "Jesús Rodríguez",
    "age" : 24,
    "company" : "Software developer for Intel Corporation",
    "location" : "Monclova, Coahuila"
    "achievements" : {
      "titles" : ["Computer Systems Engineer","Software developer","Ethical Hacker"],
      "certifications" : ["C|EHSP de Ethical Hacking & Security Professional"]
    },
    "skills": {
      "languages" : ["Javascript","Golang","PHP","Python","C#"],
      "development_tools" : ["ReactJS","ReactNative","Express","Docker","DockerCompose","Webpack","Linux","Git","A lot of libraries and frameworks", ...rest],
      "databases" : ["MySQL", "MongoDB"],
      "cybersecurity_tools": ["Linux","Python","Golang","Offensive Web","Forensics", "OSINT"]
    }
}
```

```javascript
import PropTypes from 'prop-types'
/* Custom components. */
import Container from 'components/Container'
import Loader from 'components/Loader'
import Error from 'components/Error'
import Profile from './Components/Profile'
import Workplace from './Components/Workplace'
import Achievements from './Components/Achievements'
import Skills from './Components/Skills'
/* Custom hooks. */
import { useData } from 'hooks/useData'

const User = ( { username } ) => {

    const { data, loading, error } = useData(`users/username/${username}`)  
    const { username, name, age, company, location, achievements, skills } = data

    if(loading){
        return <Loader message='Loading profile'/>
    }

    if(error){
        return <Error message={error}/>
    }

    return(
        <Container>
            <Profile username={username} name={name} age={age}/>
            <Workplace company={company} location={location}/>
            <Achievements achievements={achievements}/>
            <Skills skills={skills}/>
        </Container>
    )
}

User.propTypes = {
    username: PropTypes.string
}

User.defaultProps = {
    username: 'von',
}

export default User
```
