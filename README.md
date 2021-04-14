<h1> Hi, I'm Sudo V̵O̵N̵!</h1>
<h4> ̶"̶T̶h̶e̶ ̶s̶p̶h̶i̶n̶x̶ ̶m̶e̶m̶b̶e̶r̶ ̶9̶"̶</h4>
<h2 align="center">About Me</h2>
<br>

```javascript
import React, { useState, useEffect } from 'react'
import Von from '../components/Profile/Von';
import Navbar from '../components/Main/Navbar';
import Footer from '../components/Main/Footer';
import Container from '../components/Main/Container';

const getMember = ( { number } ) => {

  const [ member, setMember ] = useState({
      bio : {
        name : 'Jesús Rodríguez',
        age : 23,
        titles : ['Computer Systems Engineer','Ethical Hacker'],
        certifications : ['C|EHSP de Ethical Hacking & Security Professional'],
        company : 'Tredicom',
        location : 'Saltillo, Coahuila'
      },
      skills: {
        languages : ['Javascript', 'Typescript', 'PHP', 'Python', 'Golang'],
        tools : ['ReactJS','ReactNative','Angular','Express','Flask','Docker','SCSS','Webpack','Linux'],
        databases : ['MySQL', 'MongoDB'],
        cyber_security_tech: ['Linux','Python','Golang','Offensive Web','Forensics', 'OSINT']
      }
  })
  
  const fetchMember = number => fetch(`http://localhost:3000/sphinx/member/${number}`).then(res => res.json()).then(member => setMember(member).catch(err => console.log(err))

  useEffect(() => fetchMember(number), [])
  
  return { member }
}

const SphinxMember = ({ number }) {

    const { member } = getMember(number)
    const { bio, skills } = member
    
    return(
      <Container>
        <Navbar title='Profile'/>
        <h1>The spinx member {number}</h1>
        { member && 
          <Von bio={bio} skills={skills}/>
        }
        <Footer/>
      </Container>
    );
  }
}
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
