<h2 align="center">About Me</h2>
<br>

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
    "company" : "Looking for a great job",
    "location" : "Saltillo, Coahuila"
    "achievements" : {
      "titles" : ["Computer Systems Engineer","Software developer","Ethical Hacker"],
      "certifications" : ["C|EHSP de Ethical Hacking & Security Professional"]
    },
    "skills": {
      "languages" : ["Javascript","Golang","PHP","Python"],
      "development_tools" : ["ReactJS","ReactNative","Express","Docker","DockerCompose","Webpack","Linux","Git","A lot of libraries and frameworks"],
      "databases" : ["MySQL", "MongoDB"],
      "cybersecurity_tools": ["Linux","Python","Golang","Offensive Web","Forensics", "OSINT"]
    }
}
```

```javascript
import PropTypes from 'prop-types'
/* Custom components. */
import Container from 'components/Container'
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

![Javascript](https://img.shields.io/badge/-JavaScript-181717?style=flat-square&logo=javascript)
![NodeJS](https://img.shields.io/badge/-Nodejs-181717?style=flat-square&logo=Node.js)
![ReactJS](https://img.shields.io/badge/-React-181717?style=flat-square&logo=react)
![ReactNative](https://img.shields.io/badge/-ReactNative-181717?style=flat-square&logo=react)
![Webpack](https://img.shields.io/badge/-Webpack-181717?style=flat-square&logo=webpack)
![Golang](https://img.shields.io/badge/-Golang-181717?style=flat-square&logo=go)
![Python](https://img.shields.io/badge/-Python-181717?style=flat-square&logo=Python)
![MongoDB](https://img.shields.io/badge/-MongoDB-181717?style=flat-square&logo=mongodb)
![MySQL](https://img.shields.io/badge/-MySQL-181717?style=flat-square&logo=mysql)
![Docker](https://img.shields.io/badge/-Docker-181717?style=flat-square&logo=docker)
![DockerCompose](https://img.shields.io/badge/-DockerCompose-181717?style=flat-square&logo=docker)
![DigitalOcean](https://img.shields.io/badge/-DigitalOcean-181717?style=flat-square&logo=digitalocean)
![Git](https://img.shields.io/badge/-Git-181717?style=flat-square&logo=git)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github)
![GitLab](https://img.shields.io/badge/-GitLab-181717?style=flat-square&logo=gitlab)
![GitHub](https://img.shields.io/badge/-Linux-181717?style=flat-square&logo=linux)
