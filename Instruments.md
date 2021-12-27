# Instruments 

The following measures are provided through the Environmental Data Agent’s APIs and contain the environmental impact data from the physical infrastructure that is providing the resources consumed a server-side software application (compute, memory, storage, network capacity).

## CO2-eq 

This measure is calculated from the following data points and represents the current CO2-equivalents from the underlying infrastructure. The instrument combines both operational CO2-eq (e.g. from electricity) and embedded CO2-eq, e.g. from server hardware.

The Environmental Data Agent enriches data points, such as electricity consumption, with the current CO2-eq, based on available information, e.g. the CO2 concentration of the power grid in which the data center running the host server is located in.

### Active CO2-eq (operational CO2-eq)

The following data is collected with the Environmental Data Agent to provide the instrument for measuring the active CO2-equivalents.

* Total power consumption (kWh)
* Total on-site power production (kWh)
	* Fuel Type for Production
	* % of active on-site production from physically connected renewable power generation (e.g. solar)
* Grid Region / Geospatial Zone of the physical facility 
* Green power procurement type: PPA, RACs, GOO, others
	* % of annual consumption covered by green certificates or PPAs _(does not lead to decrease in calculated total operational CO2-eq)_
	* % of hourly consumption covered by green certificates or PPAs _(does not lead to decrease in calculated total operational CO2-eq)_
* Total Pollution
	* Total SOx pollution (from on-site generation)
		* Active hours of backup power generation (h)
		* Hours of maintenance runs of backup power generation per year (h)
		* Fuel type (gas/diesel, etc.)
		* Total fuel consumption (l)
		* Own measured/reported SOx concentration per l of fuel (SOx)
* Total NOx pollution (from own generation)
	* Active hours of backup power generation (h)
	* Hours of maintenance runs of backup power generation per year (h)
	* Fuel type (gas/diesel, etc.)
	* Total fuel consumption (l)
	* Own measured/reported NOx concentration per l of fuel (NOx)
* Total PM pollution (from own generation)
	* Active hours of backup power generation (h)
	* Hours of maintenance runs of backup power generation per year (h)
	* Fuel type (gas/diesel, etc.)
	* Total fuel consumption (l)
	* Own measured/reported PM concentration per l of fuel (PM)

### Passive CO2-eq (embedded CO2-eq)

The following data is collected with the Environmental Data Agent to provide the instrument for measuring the passive CO2-equivalents which are embedded in the infrastructure, e.g. from manufacturing server hardware or cement.

* Total use of GWP-rated gases (m3)
	* GWP Gas 1 (m3)
	* GWP Gas 2 (m3)
* Average GWP across data center infrastructure (GWP)
	* GWP Gas 1 (GWP)
	* GWP Gas 2 (GWP)
* Total embedded CO2-eq in equipment
	* Total CO2-eq embedded in server hardware
	* Total CO2-eq embedded in electrical infrastructure (incl. cabling, switchgear, etc.)
	* Total CO2-eq embedded in uninterruptible power infrastructure (incl. diesel gen-sets and batteries)
	* Total CO2-eq embedded in the building & construction infrastructure 
	* Total CO2-eq embedded in fire suppression systems
* New embedded CO2 added through equipment change in the last year
* CO2 removed through equipment replacement in the last year

### Electronic Waste Potential (WEEE)

* Total electronic waste potential (Metric Tonne’s)
	* metric tones of electronic equipment installed (excl. hardware)
	* Total electronic waste disposed (Metric Tonne’s)
	* Avg annual recycling rate (%)
	* Electronic waste disposed that was recycled in the last year (mt)
	* Avg annual refurbishment rate (%)
	* Disposed electronic waste that was refurbished in the last year (mt)

### Total adiabatic depletion potential (ADP, Resource Consumption)

* Total water consumption (l)
* % of water coming from fresh drinking water

### Total Societal Impact

Missing metrics

