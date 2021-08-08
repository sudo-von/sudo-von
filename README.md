<h2 align="center">About Me</h2>
<br>

```javascript
/* TODO: Remove commented code. */
const useDataResponseExample = {
    bio : {
      name : 'Jesús Rodríguez',
      age : 24,
      titles : ['Computer Systems Engineer','Ethical Hacker'],
      certifications : ['C|EHSP de Ethical Hacking & Security Professional'],
      company : 'Looking for a great job',
      location : 'Saltillo, Coahuila'
    },
    skills: {
      languages : ['Javascript', 'Golang','PHP', 'Python'],
      tools : ['ReactJS','ReactNative','Express','Docker','DockerCompose','Webpack','Linux','A lot of libraries and frameworks'],
      databases : ['MySQL', 'MongoDB'],
      cyber_security_tech: ['Linux','Python','Golang','Offensive Web','Forensics', 'OSINT']
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
[![Linkedin](https://img.shields.io/badge/-von-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/jes%C3%BAs-%C3%A1ngel-rodr%C3%ADguez-mart%C3%ADnez-84991a1b4/)](https://www.linkedin.com/in/jes%C3%BAs-%C3%A1ngel-rodr%C3%ADguez-mart%C3%ADnez-84991a1b4/)
[![Instagram](https://img.shields.io/badge/-von-yellow?style=flat-square&logo=Instagram&logoColor=white&link=https://www.instagram.com/developerjesus/)](https://www.instagram.com/developerjesus/)
[![GitHub](https://img.shields.io/github/followers/sudo-von?label=follow&style=social)](https://github.com/sudo-von)


<p>
  <img height="180em" src="https://github-readme-stats-eight-theta.vercel.app/api?username=sudo-von&show_icons=true&theme=material-palenight&include_all_commits=true&count_private=true" alt="sudo-von" />
</p>
<p>
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sudo-von&layout=compact&theme=material-palenight&count_private=false" alt="sudo-von" />
</p><br>
<h4>Visitor's count</h4>
<p><img src="https://profile-counter.glitch.me/{sudo-von}/count.svg" alt="sudo-von :: Visitor's Count" /></p>
