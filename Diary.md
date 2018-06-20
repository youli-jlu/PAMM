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
  
  And for judgment of distance, xxcutoff, I'll use more detail  careful cutoff data as Rcd may be larger than 4.5 A.But in current test,
I still use 4.5A except Rcd.

  OMG, I used whole night handling bug of selecting atoms. I finally find my stupid fault in reading part. Now, I have to test the convergence step and grid number in PAMM algorithm.

2018.6.20

  I find that we should use "-l" option to set initial QS length step, or it will automatically set a cutoff based on point density.I try to find a proper length step, but don't have good result.When I use relatively large ls, I get only two clusters, and one of them is the enantiomer of the other one. When I use smaller ls, more and more clusters appear, but none or them have the same scale as  foregoing two. Which result is beter? And should I change some arguments?
