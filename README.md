<h2> Hi, I'm V̵O̵N̵!</h2>
<h5> ̶"̶T̶h̶e̶ ̶s̶p̶h̶i̶n̶x̶ ̶m̶e̶m̶b̶e̶r̶ ̶9̶"̶</h5>
<img src="https://64.media.tumblr.com/ae04468c064954188d57dd3a75916043/tumblr_n9zrj52cBP1s8jr81o3_500.gif"/>

```javascript
import React from 'react'
import Von from '../components/Von';

class SphinxMember extends React.Component {
  constructor(props){
    super(props);
    this.state = {
      bio : {
        name : 'Jesús Rodríguez',
        age : 23,
        titles : ['Computer Systems Engineer','Ethical Hacker'],
        certifications : ['C|EHSP de Ethical Hacking & Security Professional'],
        company : 'Tredicom',
        location : 'Saltillo, Coahuila'
      },
      skills: {
        languages : ['Javascript', 'Typescript', 'PHP', 'Python'],
        tools : ['ReactJS','ReactNative','Angular','Express','Flask','Docker','SCSS','Webpack','Linux'],
        databases : ['MySQL', 'MongoDB'],
        cyber_security_tech: ['Linux','Python','Offensive Web','Forensics']
      }
    }
  }
  render(){
    return(
      <Von bio={this.state.bio} skills={this.state.skills}/>
    );
  }
}
```
[![Linkedin](https://img.shields.io/badge/-von-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/jes%C3%BAs-%C3%A1ngel-rodr%C3%ADguez-mart%C3%ADnez-84991a1b4/)](https://www.linkedin.com/in/jes%C3%BAs-%C3%A1ngel-rodr%C3%ADguez-mart%C3%ADnez-84991a1b4/)
[![Instagram](https://img.shields.io/badge/-von-yellow?style=flat-square&logo=Instagram&logoColor=white&link=https://www.instagram.com/developerjesus/)](https://www.instagram.com/developerjesus/)
[![GitHub](https://img.shields.io/github/followers/sudo-von?label=follow&style=social)](https://github.com/sudo-von)

<p>
  <img height="180em" src="https://github-readme-stats-eight-theta.vercel.app/api?username=sudo-von&show_icons=true&theme=material-palenight&include_all_commits=true&count_private=true" alt="sudo-von" />
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sudo-von&layout=compact&theme=material-palenight" alt="sudo-von" />
</p>
