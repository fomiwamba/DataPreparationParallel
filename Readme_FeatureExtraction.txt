
ViSA
TD_Analysis
	- Config da?
		- Tacho da?
			SignalGleichSetzen ChX, Tacho
			TimeAnalysis mit Tacho
		- Sonst
			TimeAnalysis ohne Tacho
		- DataStorage:
			Date_Time, mv, max, min, peak, peak2peak, crest, kurtosis, iqr, median, outliers

Orbit_Analysis
	- Config da?
		- Tacho da?
			SignalGleichSetzen ChX, Tacho
			OrbitAnalysis mit Tacho
		- Sonst
			OrbitAnalysis ohne Tacho
		- DataStorage:
			Date_Time, x0, y0, S0, phi0, xm, ym, Sm, phim, Sgmax, phigmax


Envelope_Analysis
	- Config da?
		Hüllkurvenberechnung -> ChxEnv
		SignalGleichSetzen ChX, ChXEnv
		- DataStorage:
			ChxEnv


FD_Analysis of ChX or ChxEnv
	- Config da?
		- Tacho da?
			SignalGleichSetzen ChX, Tacho
			FFTAnalysis mit Tacho
		- Sonst
			FFTAnalysis ohne Tacho
		- DataStorage Chx/ChxEnv:
			Date_Time, Ax, All, lf, iso, hf, 1x, 2x, 3x, 4x, SumAll, Harmonics, Subsynchronous, Synchronous, NonSynchronous


Order_Analysis of Chx or ChxEnv
	- Config da?
		- Tacho da?
			- Speed > 1 rpm?
				SignalGleichSetzen ChX, Tacho
				OrderAnalysis
		- DataStorage Chx:
			ChXrev, ChPulsrev, OAx, OPx, OAx_avg, OPx_avg, OSpeed, BodeO1, BodeO2, BodeO3, BodeO4, BodeO5
		- DataStorage ChxEnv:
			ChXEnvrev, ChPulsrev, OAxEnv, OAxEnv_avg, OSpeed


ESA
TD_Analysis
	- Config da?
		U_sig and I_sig da?
			TimeAnalysis
			DataStorage: 
				V_sig
				V_sig_demoduliert				
				V_RMS	[Phase1, Phase2, Phase3, Total, Deviation, Unbalance]
				V_Peak 
				V_CF
				V_Variation
				V_VDF
				
				C_sig
				C_sig_demoduliert	
				C_RMS
				C_Peak
				C_CF
				C_Variation
				C_THDF

				Power Factor
				Impedance
				Real Power W
				Apparent Power VA
				Reactive Power VARS

				DemandPower W
				Load [%]
				Efficiency [%]
				OutputPower W
				OutputTorque Nm

ESA
FD_Analysis
	- Config da?
		U_sig and I_sig da?
			FFTAnalysis
			DataStorage:
				V_sig_spec
				V_sig_demoduliert_spec
 
				V_THD All	[Phase1, Phase2, Phase3, Total, Deviation, Unbalance]
				V_THD Odd
				V_THD Even
				V_THD pve
				V_THD nve
				V_THD Zero

				C_sig_spec
				C_sig_demoduliert_spec
				C_THD All
				C_THD Odd
				C_THD Even
				C_THD pve
				C_THD nve
				C_THD Zero

				Line Frequency
				Running Speed
				Slip Frequency
				Pole Pass Frequency
				Static Eccentricity
				Dynamic Eccentricity
				Stator  Damage
				Bearing Damage
				Imbalance & Misalignment
				Rotor damage

