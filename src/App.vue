<template>
  <div class="main-wrapper">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Jesper Bang</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/avatar.jpg" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">{{ mabout[Locale] }}</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">{{ mexperience[Locale] }}</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">{{ meducation[Locale] }}</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">{{ mskills[Locale] }}</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">{{ minterests[Locale] }}</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">{{ mawards[Locale] }}</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">

      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">{{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">{{ address }}
            <a href="mailto:jesper.xenia@gmail.com">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe[Locale] }}</p>
          <ul class="list-inline list-social-icons mb-0">
          <!--
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle  fa-stack-2x"></i>
                  <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            -->
              <li class="list-inline-item">
                <a href="https://www.linkedin.com/in/jesperbang/">
                  <span class="fa-stack fa-lg">
                    <i class="fa fa-circle fa-stack-2x"></i>
                    <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                  </span>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="https://github.com/Jesperbang">
                  <span class="fa-stack fa-lg">
                    <i class="fa fa-circle fa-stack-2x"></i>
                    <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                  </span>
                </a>
              </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">{{ mexperience[Locale] }}</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="job in experience[Locale]" :key="job.description">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p>{{ job.description }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>

        </div>

      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">{{ meducation[Locale] }}</h2>
          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ edu3[Locale].title }}</h3>
              <div class="subheading mb-3">{{ edu3[Locale].subtitle }}</div>
              <div>{{ edu3[Locale].subject }}</div>
              <a href="	http://cn.inside.dtu.dk/cnnet/Grades/Public.aspx?Id=EPPH2V82AE">Karakterer</a>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ edu3[Locale].fromto }}</span>
            </div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
              <div class="resume-content mr-auto">
                <h3 class="mb-0">{{ edu2[Locale].title }}</h3>
                <div class="subheading mb-3">{{ edu2[Locale].subtitle }}</div>
                  <div>{{ edu2[Locale].subject }}</div>
                    <p>{{ edu2[Locale].finish }}</p>
                  </div>
                <div class="resume-date text-md-right">
                  <span class="text-primary">{{ edu2[Locale].fromto }}</span>
                </div>
              </div>

            <div class="resume-item d-flex flex-column flex-md-row">
              <div class="resume-content mr-auto">
                <h3 class="mb-0">{{ edu1[Locale].title }}</h3>
                <div class="subheading mb-3">{{ edu1[Locale].subtitle }}</div>
                <p>{{ edu1[Locale].subject }}</p>
              </div>
              <div class="resume-date text-md-right">
                <span class="text-primary">{{ edu1[Locale].fromto }}</span>
              </div>
            </div>
            <p></p>
            <div class="resume-item d-flex flex-column flex-md-row">
                <div class="resume-content mr-auto">
                  <h3 class="mb-0">{{ edu0[Locale].title }}</h3>
                  <div class="subheading mb-3">{{ edu0[Locale].subtitle }}</div>
                </div>
                <div class="resume-date text-md-right">
                  <span class="text-primary">{{ edu0[Locale].fromto }}</span>
                </div>
              </div>
          </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">{{ mskills[Locale] }}</h2>

          <div class="subheading mb-1s">{{ skilllang.title[Locale] }}</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <font size="4">{{ skilllang.native[Locale] }}&emsp;</font><br/>
              <flag iso="dk" style="font-size:30px"/>
            </li>
            <li class="list-inline-item">
              <font size="4">{{ skilllang.fluent[Locale] }}&emsp;</font><br/>
              <flag iso="gb" style="font-size:30px"/>
            </li>
            <li class="list-inline-item">
              <font size="4">{{ skilllang.understand[Locale] }}</font><br/>
              <flag iso="de" style="font-size:30px"/>
              <flag iso="se" style="font-size:30px"/>
            </li>
          </ul>

          <div class="subheading mb-3">{{ prolang[Locale] }}</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item" title="HTML5">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item" title="CSS3">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item" title="Java Script">
              <i class="devicons devicons-javascript"></i>
            </li>
            <li class="list-inline-item" title="jquery">
              <i class="devicons devicons-jquery"></i>
            </li>
            <li class="list-inline-item" title="bootstrap">
              <i class="devicons devicons-bootstrap"></i>
            </li>
            <li class="list-inline-item" title="npm">
              <i class="devicons devicons-npm"></i>
            </li>
            <li class="list-inline-item" title="Android">
              <i class="devicons devicons-android"></i>
            </li>
            <li class="list-inline-item" title="IOS - Swift">
              <i class="devicons devicons-swift"></i>
            </li>
            <li class="list-inline-item" title="Amazon cloud">
              <i class="devicons devicons-aws"></i>
            </li>
            <li class="list-inline-item" title="Scrum">
              <i class="devicons devicons-scrum"></i>
            </li>
            <li class="list-inline-item" title="React">
              <i class="devicons devicons-react"></i>
            </li>
            <li class="list-inline-item" title="Python">
              <i class="devicons devicons-python"></i>
            </li>
            <li class="list-inline-item" title="PHP">
              <i class="devicons devicons-php"></i>
            </li>
            <li class="list-inline-item" title="nodejs">
              <i class="devicons devicons-nodejs"></i>
            </li>
            <li class="list-inline-item" title="MySQL">
              <i class="devicons devicons-mysql"></i>
            </li>
            <li class="list-inline-item" title="Java">
              <i class="devicons devicons-java"></i>
            </li>
            <li class="list-inline-item" title="Git">
              <i class="devicons devicons-git"></i>
            </li>
            <li class="list-inline-item" title="Firebase">
              <i class="devicons devicons-firebase"></i>
            </li>
            <li class="list-inline-item" title=".Net">
              <i class="devicons devicons-dotnet"></i>
            </li>
            <li class="list-inline-item" title="Jenkins">
              <i class="devicons devicons-jenkins"></i>
            </li>
          </ul>

          <div class="subheading mb-3">Workflow</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check" style="color:rgb(53, 241, 6)"></i>
              Mobile-First, Responsive Design</li>
            <li>
              <i class="fa-li fa fa-check" style="color:rgb(53, 241, 6)"></i>
              Cross Functional Teams</li>
            <li>
              <i class="fa-li fa fa-check" style="color:rgb(53, 241, 6)"></i>
              Agile Development &amp; Scrum</li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">{{ minterests[Locale] }}</h2>
          <p>{{ interests1[Locale] }}</p>
          <p>{{ interests2[Locale] }}</p>
          <p class="mb-0">{{ interests3[Locale] }}</p>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">{{ cert[Locale].title }}</h2>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              {{ cert[Locale].course1 }}</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              {{ cert[Locale].course2 }}</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              {{ cert[Locale].course3 }}</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              {{ cert[Locale].course4 }}</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              {{ cert[Locale].course5 }}</li>
            <!--
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              2<sup>nd</sup>
              somthing</li>
              -->
          </ul>
        </div>
      </section>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    this.Locale = 'dk'
    return {
      mabout: {
        dk: 'Omkring',
        en: 'About'
      },
      mexperience: {
        dk: 'Erfaring',
        en: 'Experience'
      },
      meducation: {
        dk: 'Uddannelse',
        en: 'Education'
      },
      mskills: {
        dk: 'Færdigheder',
        en: 'Skills'
      },
      minterests: {
        dk: 'Interesser',
        en: 'Interests'
      },
      mawards: {
        dk: 'Kurser',
        en: 'Courses'
      },
      may: {
        dk: 'Maj',
        en: 'May'
      },
      present: {
        dk: 'Nu',
        en: 'Present'
      },
      title: 'Jesper Bang Portfolio',
      name: 'Jesper',
      surname: 'Bang',
      address: 'Persillehaven 40 · 2730, Herlev · (+45) 22402817 ·',
      aboutMe: {
        dk: 'Jeg er 23 år, yderst innovativ og tech minded, og mit mål er, at blive en bedre softwareudvikler. Når jeg ikke studerer på DTU, bruger jeg tid på at udvikle software løsninger. Jeg deltager ofte i foredrag uden for mit normale studie for at holde mig opdateret om den nyeste teknologi. Og jeg kan arbejde med et udvalg af software løsninger og teknologier fra cloud services, databaser, Agile udviklingsmetoder som SCRUM, OOAD til høj og lav niveau programmeringssprog.',
        en: 'I am a 23 year old innovative tech mind, who always strive to become a better software developer. When i am not studying at DTU, I spend time developing new solutions. I often attend talks, outside my normal study, to stay up to date on the newest tech. Capable of working with an assortment of software solutions and technology, from database management, Agile development methods particularly OOAD and SCRUM to high and low-level programming languages.'
      },
      email: 'jesper.xenia@gmail.com',
      interests1: {
        en: 'Apart from being a software developer student, I enjoy most of my time with friends and family. As a prior elite swimmer and Team Danmark student a lot of my time is spend on workouts, both in fitness and in the swimming pool to stay fit.',
        dk: 'Udover at studere software udvikling bruger jeg meget af min tid med venner og familie. Som tidligere elitesvømmer og Team Danmark elev, er træning en del af min hverdag, hvor jeg ofte træner fitness og svømnmer for at holde mig i form.'
      },
      interests2: {
        en: 'I often go to the cinema with friends and enjoy watching good movies.',
        dk: 'Jeg går ofte i biografen med gode venner og kan godt lide, at se nogle gode film.'
      },
      interests3: {
        en: 'I like to explore the newest tech, programs and tools to supplement and prepare my knowledge for the future. It\'s exciting to try different ideas and learn new methods while doing so.',
        dk: 'Jeg kan godt lide, at udforske den nyeste teknologi, programmer og værktøjer, for at supplerer og forbedere min viden til fremtiden. Det er spændende, at prøve forskellige ideer af, og lære nye ting i den forbindelse.'
      },
      prolang: {
        en: 'Programming Languages & Tools',
        dk: 'Programmeringssprog & Værktøjer'
      },
      skilllang: {
        title: {
          en: 'Languages',
          dk: 'Sprog'
        },
        native: {
          en: 'Native',
          dk: 'Modersmål'
        },
        fluent: {
          en: 'Fluent in',
          dk: 'Flydende i'
        },
        understand: {
          en: 'Understand',
          dk: 'Forstår'
        }
      },
      cert: {
        en: {
          title: 'CERTIFICATIONS & COURSES',
          course1: 'Svimming Coach - DGI 2012',
          course2: 'Unity Game Engine - Ungdommens Naturvidenskabelige Forening 2011',
          course4: 'Network security & hacking - Ungdommens Naturvidenskabelige Forening 2011',
          course3: 'Android App Programming - Ungdommens Naturvidenskabelige Forening 2011',
          course5: 'Oxford University 3 weeks summer course - English A, Social skills B 2010'
        },
        dk: {
          title: 'CERTIFIKATIONER & KURSER',
          course1: 'Svømmetræner - DGI 2012',
          course2: 'Unity Game Engine - Ungdommens Naturvidenskabelige Forening 2011',
          course4: 'Netværkssikkerhed & hacking - Ungdommens Naturvidenskabelige Forening 2011',
          course3: 'Android App Programmering - Ungdommens Naturvidenskabelige Forening 2011',
          course5: 'Oxford University 3 ugers sommer kursus - Engelsk 12, sociale færdigheder 10, 2010'
        }
      },
      edu3: {
        en: {
          title: 'TECHNICAL UNIVERSITY OF DENMARK - DTU',
          subtitle: 'B Eng.',
          subject: 'Software Technology',
          fromto: 'September 2016 - December 2019'
        },
        dk: {
          title: 'Danmarks Tekniske Universitet - DTU',
          subtitle: 'Diplomingeniør',
          subject: 'Softwareteknologi',
          fromto: 'September 2016 - December 2019'
        }
      },
      edu2: {
        en: {
          title: 'TECHNICAL UNIVERSITY OF DENMARK - DTU',
          subtitle: 'Msc (Eng.)',
          subject: 'Network Technology and IT',
          fromto: 'September 2014 - May 2016',
          finish: 'Changed study'
        },
        dk: {
          title: 'Danmarks Tekniske Universitet - DTU',
          subtitle: 'Civilingeniør',
          subject: 'NETVÆRKSTEKNOLOGI OG IT',
          fromto: 'September 2014 - Maj 2016',
          finish: 'Studieskift'
        }
      },
      edu1: {
        en: {
          title: 'Rungsted Gymnasium',
          subtitle: 'Mathematics A, Physics B, Chemistry B, Innovation C',
          subject: 'STX',
          fromto: '2011 - 2014'
        },
        dk: {
          title: 'Rungsted Gymnasium',
          subtitle: 'Matematik A, Fysik B, Kemi B, Innovation C',
          subject: 'STX',
          fromto: '2011 - 2014'
        }
      },
      edu0: {
        en: {
          title: 'NORDSJÆLLANDS GRUNDSKOLE OG GYMNASIUM - NGG',
          subtitle: 'Primary School',
          fromto: '2002 - 2011'
        },
        dk: {
          title: 'NORDSJÆLLANDS GRUNDSKOLE OG GYMNASIUM - NGG',
          subtitle: 'Folkeskole',
          fromto: '2002 - 2011'
        }
      },
      experience: {
        en: [
          {
            position: 'Developer',
            company: 'Netcompany',
            description: 'Som Developer hos Netcompany er jeg til daglig i direkte kontakt med kunden og holder mig altid opdateret på de nyeste trends indenfor udvikling af software løsninger. ',
            startDate: '2019',
            endDate: 'Present'
          },
          {
            position: 'Frivillig Indkøber & Bartender',
            company: 'Café studiestoppet–kælderbaren',
            description: 'Som frivillig indkøber sørger jeg for at baren altid er fyldt og der er ekstra varer på lageret. Jeg står for bestillingerne hos bl.a. Carlsberg og Catering, når der skal fyldes op. Derudover står jeg også selv som frivillig bartender for at holde studenter baren kørende.',
            startDate: '2017',
            endDate: 'Present'
          },
          {
            position: 'Stagehand',
            company: 'Live Nation',
            description: 'Working during shows and setting up scenery, lights, sound, props, rigging and special effects before shows for big concerts mainly in Copenhagen. Examples. AC/DC, Coldplay, Adele, Rihanna, Muse, Beyoncé and so forth. It\'s really exciting learning what it takes to setup and run big shows like these.',
            startDate: '2015',
            endDate: 'Present'
          },
          {
            position: 'Lifeguard',
            company: 'Hørsholm Svømmehal',
            description: 'As a prior elite swimmer i worked as a spare lifeguard when additional personal was needed. Opening in the mornings and closing at evenings. Guarding pools, cleaning changing room and monitoring water values. As a lifeguard you must keep your first aid up to date and attend the yearly lifeguard test.',
            startDate: '2017',
            endDate: '2018'
          },
          {
            position: 'Swimming instructor',
            company: 'Hørsholm Svømmeforening & Søllerød Svømmeklub',
            description: 'Responsible coach for designing training programs to teaching kids and adults swimming techniques. This has given me great insight into working with different people and different ways to get the job done.',
            startDate: '2010',
            endDate: '2014'
          }
        ],
        dk: [
          {
            position: 'Developer',
            company: 'Netcompany',
            description: 'Som Developer hos Netcompany er jeg til daglig i direkte kontakt med kunden og holder mig altid opdateret på de nyeste trends indenfor udvikling af software løsninger. ',
            startDate: '2019',
            endDate: 'Nu'
          },
          {
            position: 'Frivillig Indkøber & Bartender',
            company: 'Café studiestoppet–kælderbaren',
            description: 'Som frivillig indkøber sørger jeg for at baren altid er fyldt og der er ekstra varer på lageret. Jeg står for bestillingerne hos bl.a. Carlsberg og Catering, når der skal fyldes op. Derudover står jeg også selv som frivillig bartender for at holde studenter baren kørende.',
            startDate: '2017',
            endDate: 'Nu'
          },
          {
            position: 'Stagehand',
            company: 'Live Nation',
            description: 'Arbejder med opsætning af koncerter som inkluderer scene, lys, lyd, rekvisitter, riggings og special effects før shows. Arbejder hovedsageligt for store koncerter i København som eksempel; AC/DC, Coldplay, Adele, Rihanna, Muse, Beyoncé osv. Det er utrolig spændende, at få indsigt i, hvad det kræver af teknik for at få så store shows op at køre.',
            startDate: '2015',
            endDate: 'Nu'
          },
          {
            position: 'Livredder',
            company: 'Hørsholm Svømmehal',
            description: 'Som tidligere konkurrencesvømmer, har jeg i mange år arbejdet som livredder, når der var behov for ekstra peronale. Dette inkludere at åbne svømmehallen om morgenen, lukke den om aftenen, overvåge bassinerne, rengøre omklædningsrummene og tjekke vandværdierne samt vandkvaliteten. Som livredder betyder det, at man altid er opdateret på førstehjælp og tager den årlige livredderprøve.',
            startDate: '2017',
            endDate: '2018'
          },
          {
            position: 'Svømme instruktør',
            company: 'Hørsholm Svømmeforening & Søllerød Svømmeklub',
            description: 'Jeg har arbejdet som ansvarshavende træner, hvor jeg designede træningsprogrammer og underviste børn og voksene i forskellige svømmeteknikker. Dette har givet mig stor indsigt i, at arbejde med forskellige mennesker og lært mig, forskellige metoder til, at få tingene til at lykkedes.',
            startDate: '2010',
            endDate: '2014'
          }
        ]
      }
    }
  },
  mounted () {
    const $ = this.jquery
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function () {
        if (location.pathname.replace(/^\//, '') === this.pathname.replace(/^\//, '') && location.hostname === this.hostname) {
          var target = $(this.hash)
          target = target.length ? target : $('[name=' + this.hash.slice(1) + ']')
          if (target.length) {
            $('html, body').animate({
              scrollTop: (target.offset().top)
            }, 1000, 'easeInOutExpo')
            return false
          }
        }
      })
      // Closes responsive menu when a scroll trigger link is clicked
      $('.js-scroll-trigger').click(function () {
        $('.navbar-collapse').collapse('hide')
      })
      // Activate scrollspy to add active class to navbar items on scroll
      $('body').scrollspy({
        target: '#sideNav'
      })
    })
  },
  methods: {
    dklang: function (event) {
      this.Locale = 'dk'
      this.$forceUpdate()
    },
    enlang: function (event) {
      this.Locale = 'en'
      console.log('en')
      this.$forceUpdate()
      console.log('Force update')
      return this.Locale
    }
  }
}
</script>

<style>
body {
  font-family: 'Open Sans', serif;
  padding-top: 54px;
  color: #868e96;
}
@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Saira Extra Condensed', serif;
  font-weight: 700;
  text-transform: uppercase;
  color: #343a40;
}
h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}
h2 {
  font-size: 3.5rem;
}
.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: 'Saira Extra Condensed', serif;
  font-size: 1.35rem;
}
.list-social-icons a {
  color: #495057;
}
.list-social-icons a:hover {
  color: rgb(56, 125, 189);
}
.list-social-icons a .fa-lg {
  font-size: 1.75rem;
}
.list-icons {
  font-size: 3rem;
}
.list-icons .list-inline-item i:hover {
  color: rgb(56, 125, 189);
}
#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
  text-transform: uppercase;
}
#img-button-dk {
  background-image: url('.\assets\Flag_denmark.png');
  position: relative;
  padding: 0px;
  width: 40px;
  height: 30px;
  background-size: 100%;
  background-size: 35px auto;
}
#img-button-en {
  background-image: url('.\assets\Flag_kingdom.png');
  position: relative;
  padding: 0px;
  width: 40px;
  height: 40px;
  background-size: 100%;
  background-size: 35px auto;
}
@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.5rem solid rgba(255, 255, 255, 0.2);
  }
  #sideNav .navbar-collapse {
    display: flex;
    align-items: flex-start;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}
section.resume-section {
  border-bottom: 1px solid #dee2e6;
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
}
section.resume-section .resume-item .resume-date {
  min-width: none;
}
@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}
@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}
.bg-primary {
  background-color: rgb(56, 148, 220) !important;
}
.text-primary {
  color: rgb(56, 148, 220) !important;
}
a {
  color: rgb(56, 125, 189);
}
a:hover, a:focus, a:active {
  color: #274b82;
}
</style>
