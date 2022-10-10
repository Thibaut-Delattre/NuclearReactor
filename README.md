# NuclearReactor
Thermal homogeneous nuclear reactor modeling (fuel consumption and reactor power) on MATLAB

This live editor script in MATLAB models fuel consumption and reactor power depending on a few parameters in a thermal homogeneous nuclear reactor. This model depends mainly on :
- Efficiency of the reactor
- UOX or/and MOX fuel, enrichments and mass of fuel
- Volume, temperature and pressure in the reactor core
- Moderator (light water, heavy water, graphite...)
- Neutron flux
- Cycle time of fuel in reactor

The models takes into account :
- Criticality of the reactor (k=1). It means that neutrons flux are always constant so that nuclear fuel sustains a fission chain reaction
- Energy groups : To simplify computations, the model splits some parameters into 3 differents energy groups (thermal, resonance and fast). It uses the multi-group diffusion theory.
- Thermal expansion of the moderator
- Control roads to absorb the excess of neutrons
- Neutron sources to give extra neutrons
- Fission, absorption and scattering reactions
- Simplification of the nuclear chain reaction :                                                                        
For capture reactions,                                                 
U235+n -> U236                                                                                              
U238+n -> Pu239                                                                                  
          +n   -> Pu240                                                                        
                  +n   -> Pu241                                                                        
                          +n   -> Pu242                                                       
                                  +n   -> Ma                                                 
                                          +n -> Ma ...                                        
For fission reaction, all isotopes release 2 fissions products and some neutrons

However, the models doens't take account :
- The shape and geometry of the reactor core. So neutron flux are constant in time but also in space
- The neutrons leakage
- Some neutron poisons like isotopes like Xenon 135
- Spontaneous fissions

More precisely, the model computes and show (by plotting) depending on time :
- Volume of fuel, moderator and control roads. The sum of this volumes have to be lower than the core reactor volume, otherwise the model is not good...
- Fuel consumption (with production of fission products and minor actinide). It permits to see the exact composition of the fuel at any moment.
- Fission reactions rate. It allows to compare fissions reaction rate of all isotopes.
- Burnup. This is the thermal energy produced per unit of initial fuel mass.
- Thermal and electrical power of the reactor.

To get this results, I had to solve multi-group diffusion equation for a homogeneous nuclear reactor and to solve differencial equations of the rate of change of isotopes density. All parameters allowed me to get numerical values of coefficients of previous equations.

This model is available for thermal reactor like PWR, BWR, PHWR... but is less accurate for fast reactor.
