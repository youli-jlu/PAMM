# Programming diary

2018.6.8

  Today, I start to change this program. I read part of choosing atom and calculating distance between chosen atoms, from where I learn sth
about bitwise operation and some special logical function. As reading deeply , I find that some code could be more general when changing 
descriptors, but I don't do this job because its difficulty and timecost. I'm a chemist first so why not just test a system and put this 
optimizing problem down untill I have enough time. For this reason , I just add some new variable and didn't change their framwork. 


  In my infantile opinion , I believe that Rdh and Rac is changeless in C-A...H-D system. All I have to do is just add another four distance degree and change some variable dimension. I have already rebuild the reading part and distance part, maybe I could get some information  while I finish remainning things.
  
2018.6.10

  They use 
  
          'IF (IAND(masktypes(id),TYPE_DONOR).EQ.0 .OR. ih.EQ.id) CYCLE '
          
  as a sececting algorithm, but to be honest, in most case, ih!= id, so I'll delete this judgement.
  
  And for judgment of distance, xxcutoff, I'll use more detail  careful cutoff data as Rcd may be larger than 4.5 \angstrom
