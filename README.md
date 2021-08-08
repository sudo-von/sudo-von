<h2 align="center">About Me</h2>
<br>

```javascript
{   
    "id" : "60603a5aaa037f0008ed81f9",
    "bio" : {
      "name" : "Jesús Rodríguez",
      "age" : 24,
      "titles" : ["Computer Systems Engineer","Software developer", "Ethical Hacker"],
      "certifications" : ["C|EHSP de Ethical Hacking & Security Professional"],
      "company" : "Looking for a great job",
      "location" : "Saltillo, Coahuila"
    },
    "skills": {
      "languages" : ["Javascript", "Golang","PHP", "Python"],
      "tools" : ["ReactJS","ReactNative","Express","Docker","DockerCompose","Webpack","Linux","A lot of libraries and frameworks"],
      "databases" : ["MySQL", "MongoDB"],
      "cyber_security_tech": ["Linux","Python","Golang","Offensive Web","Forensics", "OSINT"]
    }
}
```

```javascript
/* Custom components. */
import Container from 'components/Container'
import Profile from './Components/Profile'
import Skills from './Components/Skills'
/* Custom hooks. */
import { useData } from 'hooks/useData'

const User = ( { username='von' } ) => {

    const { data, loading, error } = useData(`users/username/${username}`)  
    const { bio, skills } = data

    if(loading){
        return <Loader message='Loading profile'/>
    }

    if(error){
        return <Error message={error}/>
    }

    return(
        <Container>
            <Profile data={bio}/>
            <Skills data={skills}/>
        </Container>
    )
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

<p>
  <img height="180em" src="https://github-readme-stats-eight-theta.vercel.app/api?username=sudo-von&show_icons=true&theme=material-palenight&include_all_commits=true&count_private=true" alt="sudo-von" />
</p>
<p>
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sudo-von&layout=compact&theme=material-palenight&count_private=false" alt="sudo-von" />
</p><br>
