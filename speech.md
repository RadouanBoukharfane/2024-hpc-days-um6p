
### Slide 01
------------

It is my pleasure to give this talk.

Firstly, I would like to express my gratitude to the organizers of this workshop, particularly to Mr. Imad. I also want to extend my thanks to all the speakers who have accepted to join us here in Benguerir. I hope that this workshop will spark fruitful discussions to advance the field of HPC and its applications at our university and, of course, in Morocco as a whole.

The purpose of my talk is to showcase the applications of HPC, specifically in the field of CFD.

At this stage, I would like to make a disclaimer: my focus will not be on HPC as a broad topic, but rather as a tool used in CFD. Therefore, I will not discuss HPC innovations but will instead describe how we use some of the HPC tools to study the physics that require its computational ressources.


### Slide 03
------------

The outline of my presentation is as follows:

Firstly, I will address the general audience, especially those who may be hearing about CFD for the first time. In this part, I will demonstrate why CFD is considered one of the top three fields benefiting from advancements in HPC capacities.

In the second part, I will provide an example of how HPC could play a major role in advancing the new generation of wind turbines used in power generation from wind. This part will be slightly more technical, and those of you who are already working on CFD may find it novel/interesting.


### Slide 04
------------

Let's start at the very beginning and ask, what is Fluid dynamics?

Fluid dynamics is the branch of mathematics and physics concerned with describing and studying the flow of liquids and gases.

Traditionally, there are three main methods to achieve this: either by developing analytical formulas to predict their behavior, or by performing experiments, such as those conducted in wind tunnels to measure the pressure around airfoils or cars, or by numerical simulations using computers, typically known as Computational Fluid Dynamics (CFD).

CFD is the science of using computers to predict liquid and gas flows based on the governing equations of conservation. Since fluids are all around us and sustain our lives in endless ways, understanding their behavior is crucial. For instance, the vibrations in your vocal cords generate pressure waves in the air that make speech possible, and hearing the spoken words. Without fluids, airplanes that transported our eestemed speakers wouldn’t generate any lift. Through CFD, we can analyze, understand, and predict the behavior of the fluids that make up nearly every part of our world.

There are various methods used in CFD, such as Finite Difference Method (FDM), Finite Volume Method (FVM), Finite Element Method (FEM), Discontinuous Galerkin (DG), Lattice Boltzmann (LB), and others.


### Slide 05
------------

In a more visual way, CFD encompasses a multidisciplinary fusion of applied mathematics with numerical methods, computer science with programming for massively parallel supercomputing, and, the physics of turbulence and fluid mechanics.


### Slide 06
------------


One may ask why we should consider using CFD.

Well, the reason is quite simple. The analytical approach that consists of finding analytical solutions to the conservation equations that govern most flows, is only possible for very simple cases involving 1 or 2D geometries with a limited range of turbulence.

Secondly, performing experiments is often costly and may not provide access to many quantities of interest. Even the most powerful experimental tools are limited in the amount of data they can provide, and the post-processing of this data can be quite challenging.

This is where CFD becomes a very interesting alternative. It is not as expensive as experimental methods and benefits greatly from the significant development of computing resources.

CFD also offers the possibility to investigate various flow scenarios and can measure any quantity or flow parameter of interest in a more simplified fashion.

### Slide 07
------------

Where is CFD used?

Basically, CFD has been vital in aerospace and aviation, This is where CFD was initially used and continues to see its most significant advancements to date.
One should know that Today the design of more efficient and aerodynamically stable aircraft and or more efficients fuel mixing or reduction of aircraft nose is deeply deepending on more efficient CFD simulatons. 



CFD also plays a crucial role in optimizing engine performance and analyzing heat transfer characteristics. Additionally, it finds applications in automotive engineering, energy, power generation, and biomedical engineering, which contributre significantly to advancements in various sectors.

Please enjoy the mosaic of all this simulations! I spent more than 30 minutes collecting all these images.


### Slide 07
------------

Given all these applications, we need HPC to pave the way for new innovations. In order to investigate real-world problems, we need more computing power to improve processing speed, which is critical for many computing operations, applications, and workloads.

We need HPC capabilities for storage, as large CFD computations typically cannot fit into the memory of a single machine.



### Slide 08
------------

You have probably heard of it before, but for those who haven't, NASA established a 2030 roadmap for Computational Fluid Dynamics (CFD) in 2014. This roadmap aims to provide all CFD researchers with a knowledge-based forecast of the future computational capabilities required for simulating turbulent, transitional, and reacting flows.

One of the cornerstones of this vision is the development of truly enabling technologies, such as high-order entropy-stable schemes, combined with innovative solvers on large-scale HPC hardware.

As a consequence, yhe success of the strategy relies heavily on High-Performance Computing (HPC) advancement.

### Slide 08
------------

As I mentioned earlier, CFD involves solving partial differential equations (PDEs) that describe the motion of fluid substances. These PDEs are nonlinear and, in the case of turbulent modeling, involve numerous terms, as shown in this slide. The first system of equations represents the conservation of mass, momentum, and energy. The second system is just one example of many others that represent the closure of turbulent terms. 


### Slide 09
------------


In computational fluid dynamics (CFD), turbulence modeling relies on three fundamental approaches, each varying in computational cost and accuracy. Direct Numerical Simulation (DNS) offers high accuracy by resolving all spatial and temporal scales of the computational domain. However, due to its immense computational demands, DNS is primarily a research tool for fundamental scientific problems. An alternative, the Reynolds-Averaged Navier-Stokes Equations (RANS) that reduces the cos by averaging fluctuating values over time or LES that solvers only big-scale flow. 


### Slide 10
------------

The differences in accuracy can be observed in this simulation of a flame. As you can see, DNS provides much more detailed results compared to RANS simulation, but at the cost of higher computational resources.


Now that I have introduced CFD and the role of HPC in CFD, I will present an example of how CFD is applied in more advanced applications. This example is related to the developpement of new generation of wind turbine.


### Slide 12
------------

The context of this project is that Morocco, like many other countries, is facing a major challenge: ensuring energy stability and keeping the light on while addressing the urgent task of combating climate change.

Wind energy emerges as a crucial ressources, with some countries achieving penetration levels in power generation of over 30%.

To extend these benefits globally, one of the main factor that should be reduced is the levelized cost of energy (LCOE) to make wind sources more competitive with traditional fossil fuel-based sources of electricity.

As far as Morocco is concerned, a challenging plan was initiated a decade ago to produce over 52% of its electricity through renewable sources by 2030. 

This initiative is underpinned by Morocco's geographic location and favorable climate conditions, which provide a strong foundation for harnessing wind energy in particular.

As a matter of fact, the wind generation potential is measured at approximately 5000 TWh per year, and a potential useful capacity, which measures the maximum amount of electricity that can be consistently produced and supplied to meet the demand, of 25,000 MW.

Now, in response to the growing demand, wind turbines are increasing in size with rotor diameters exceeding 200 meters.

We are talking about colossal turbines whose overall perforamnce is significantly depending on different atmospheric conditions.

Therefore, it's essential to study how airflow behaves around wind turbines with flexible blades, especially considering complex factors like aero-servo-elasticity coupling.

Among the various numerical approaches to achieve this goal, Large Eddy Simulation (LES) stands out as a powerful tool. 

It provides a high-fidelity representation of the unsteady flow field at the wind farm scale and serves as an affordable tool to calibrate wind farm layout optimization models and engineering numerical models of complex phenomena, such as dynamic wake meandering, wake steering, blade loading cycles (including wake turbulence), and the blockage effect due to the turbine row.

### Slide 04
------------

The use of this approach is still quite challenging due to the wide range of length and time scales that are required to be resolved as the Reynolds numbers involved are so high. 

In light of these limitations, an efficient massively parallel implementation becomes necessary to make it computationally achievable. 

That's why, in this first-year project, the goal is to develop a massively parallel framework that combines Large Eddy Simulation (LES) and the Actuator Line Modeling (ALM) technique. The focus is on achieving optimal workload balancing of the numerical simulator and minimizing return time using state-of-the-art methods.


### Slide 05
------------

The numerical solver I have been developping in the last nine month is an unstrucutred finite volume solver designed for low-Mach number Large-Eddy Simulation. 

The guiding principle of the solver is the highly parallel aspect capacities as attested by the IO handling that can support to few billions of cells.

The resolution of the NS equations is based on classical projection methods, in which the critical step of solving the Poisson equation is handled through highly efficient and stable Deflated Preconditioned Conjugate Gradient in combination with a residual recycling strategy and and an efficient adaptation of the convergence criteria to reduce the number of iteration to convergence. 

Several turbulence models are now integrated into the numerical solver, including the Constant Smagorinsky, Localized Dynamic Smagorinsky, Vreman, WALE, and the $\sigma$-model. 

Noteworthy to mention that the implementation of these models, especially the Dynamic Smagorinsky variants, is more challenging for unstructured grids compared to structured ones.

The solver now can be used efficiently on thousands CPU cores thanks to its two-layer parallelism technique that allows to avoid the issues of the classical single domain decomposition of the mesh and optimize accesses to memory. 


### Slide 06
------------

The standard Single Domain Decomposition consists of a simple splitting of the domain into a number of subdomains equal to the number of processors used for the computation, which is performed thanks to the Metis and Scotch Library.

The variables on the subdomain are stored in the local memory, and MPI communication protocol is used for the exchange of values at the frontiers between subdomains. 

Even though this technique gives interesting results, but it holds several drawbacks for massively parallel solving, especially regarding the issues of accesing data in the cache, load balancing and local mesh refinement. 

Moreover, if there are too many cells for each processor as it is generally the case for realistic wind turbine simulations, the computation is slowed down by cache memory overlappings.


### Slide 07
------------

To avoid this issues, an additional level of subdomains is introduced, splitting the subdomain assigned to a given processor into groups, which are small enough to fit into L3 or even L2 cache. 

The inter-element groupe communication are either local and based on openMP intra-processure request. 

This approach not only mitigates the challenges associated with load balancing and cache memory overlaps but also enhances the capabilities of the DPCG algorithm, making it faster.


### Slide 08
------------

As I mentionned, one of the main advantages of the double  domain decomposition is to enhance dynamic load blanacing and dynamic mesh refiment. 

The solver now incroporate a fully parallel dynamic mesh adaptation technique to improve the resolution in physically-relevant zones to mitigate the computational cost that works for the moment only in the 2D simulation. 

This dynamic mesh adaptation is based on the MMG3D libary. 

This library is based on local mesh modiﬁcations that is conducted at the element groupe level and allows to reach some very interesting precision for a given cell count as illustrated in this slide, where the adaptation is based on the local vorticity. 


### Slide 09
------------

The flow here is a simple flow around a cylinder at Reynolds number of 500. All the main carateristics that I have described can be show here. Typically, the double domain decomposition, and the dynamic mesh refinement. 


### Slide 10
------------

Without going into the mathematical formalism of the ALM method, I would like to emphasize that the method is fully implemented in the solver, incorporating various optimizations and corrections.

It is important to note that the primary challenge arises from the fact that all the steps are conducted on a non-cartesian grid, making the implementations considerably more complex when compared to structured grids, as is the case in most open-source solvers.

Furthermore, in light of several improvements made to the solver, various corrections have been implemented to account for 3D stall delay, tip/hub losses, dynamic stall, and filtered lifting line.


### Slide 11
------------

As the implementation is designed with the spirit of a massively parallel framework, the final step of the ALM, involving the mollification process, is applied to a small and reduced number of cells in the mesh to reduce CPU costs.

In the case of a structured mesh, this process is straightforward as all the nodes are easily identified. However, in the case of an unstructured grid, I have developed a novel three-step methodology to optimally identify the nodes where the optimization is applied, considering the double domain decomposition.

In terms of MPI exchange communication, currently, each turbine is recognized by every processor involved in the computation, leading to duplication of information, which results in a relatively high costs. However, this cost increase remains around two percent even with the addition of two turbines in the computational domain. Nevertheless, I need to refine this aspect further to optimize the process.


### Slide 12
------------

Another optimization that is implemented now in the solver concerns the modification of the limiting time step when using the actuator line method. 

Similar to the classical definition of CFL, a corresponding number can be introduced to quantify the actuator element displacement based on the local cell size during the time step, given by CFL_rotor.


If CFL_rotor >> 1, this will introduce discontinuities in the projected forces of the trailing timesteps and therewith introduces purely numerical fluctuations in the velocity field.

To prevent this numerical fluctuations, a time mollification mollify the forces with a substeping process.

This methodology has been proved to reduce the computational time without reducing the fidelity of the simulation while keeping the code stable. 


### Slide 13
------------

The latest improvement that I have incorporated into the solver is the ability to account for any geometric detail of the wind turbine. 

By this, I mean that the control of tilt, yaw, azimuth angle, and pitch angle can all be modified and adjusted consistently during the time steps, which will offer the possibility to investigate several aspect of flows past wind turbines. 


### Slide 14
------------

To validate all the previous implementations and optimizations, the 5MW reference wind turbine designed by the National Renewable Energy Laboratory with a rotor radius 63m and a hub height of 90m is simulated in uniform laminar background
flow operating at three tip speed ratio. 

Each of the three cases consists of approximately 623 million cells, setting a new record in the ASCC supercomputers and uses around 4080 process for each computation.


### Slide 15
------------


The focus is just to ensure that everything work well and that the overall topology of the flow is well restituted compared to previous studies, which is quite the case. Indeed, the generated helicoidal wake structure observed here through instantaneous
contours of Qcriterion. 

For the different tip speed ratios, a three vortex helicoidal structure is
observed in the wake and the tip speed ratio induces a different spacing between the helicoidal vortex. 



### Slide 16
------------


To wrap things up, I have introduced a new solver that models wind turbines using the ALM method, and incorporated several improvement and optimization that can be used for more realistic configurations. The initailinitial results are promising.

The next steps involve parallelizing the ALM methods, creating a more comprehensive list of verification and validation, and then addressing the main problem, which is simulating an entire wind farm in the next year. 



