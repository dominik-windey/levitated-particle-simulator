# Levitated Particle Simulator

This is a toolbox to simulate the stochastic motion of a nanoparticle 
levitated by an optical tweezer.
The equation of motion of the particle is given by a driven harmonic or Duffing
oscillator, depending on the choice of setup parameters. In addition to a 
deterministic drive, the motion is coupled to the surrounding gas molecules,
which represent a stochastic drive. To solve the equation of motion we use the
sdeint (https://pypi.org/project/sdeint/) library.

The physics module contains all equations describing the interactions or
relations within the system. Upon first execution all equations are solved for
all parameters. The solutions are then stored in a binary file (solutions_np.pkl)
to be read in fast later.

The module simulation can be used to define system parameter and the equation
of motion. Missing information is automatically completed with by the physics
module.