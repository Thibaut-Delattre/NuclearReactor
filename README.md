# NuclearReactor
Nuclear reactor modeling (fuel consumption and reactor power) on MATLAB

This live editor script in MATLAB models fuel consumption and reactor power by a few parameters. This models depends mainly on :
- Efficiancy of the reactor
- UOX or/and MOX fuel with enrichments and mass of fuel
- Volume, temperature and pressure in the reactor core
- Moderator
- Neutron flux
- Cycle time of fuel in reactor

The models take into account diffents physics phenomenons like :
- Criticality of the reactor (k=1). It means that neutrons flux are always constant so that nuclear fuel sustains a fission chain reaction
- Energy groups : To simplify computations, the model splits some parameters into 3 differents energy groups (thermal, resonance and fast)
- Thermal expansion of the moderator
- Control roads to absorb the excess of neutrons
- Neutron sources to give extra neutrons
- Fission, absorption and scattering

More precisely, the model computes and show (by plotting) depending on time :
- Volume of fuel, moderator and control roads
- Fuel consumption (with production of fission products and minor actinide)
- Fission reactions rate
- Burnup
- Thermal and electrical power of the reactor
