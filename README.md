A web-based tool for simulating and analyzing superconducting compounds based on material properties, doping, pressure, and operating temperature. Built with HTML, CSS, JavaScript, and Chart.js for visualization.

UsageSet Operating Conditions:Enter the operating temperature (in Kelvin, ≥ 0).
Enter the pressure (in GPa, ≥ 0).

Add Materials:Select a material from the dropdown (categorized by type, e.g., Element, Alloy, Cuprate).
Specify the percentage (0–100%).
Choose a doping option (None, 5% SiC, 10% SiC, or 15% Oxygen).
Click "Add Material" to include additional components (at least one required).

Remove Materials:Click "Remove" next to a material entry (minimum one material must remain).

Calculate:Click "Calculate Compound" to analyze the compound.
Ensure percentages sum to 100% (displayed in real-time with color-coded feedback).

View Results:A detailed analysis includes:Compound formula.
Table of material properties (Tc, Hc, Jc, crystal structure).
Predicted properties (Tc, Hc, Jc, crystal compatibility).
Stability warnings (if applicable).
Superconductivity verdict based on operating conditions.

A line chart shows Jc and Hc vs. temperature.

Material DatabaseThe simulator includes a comprehensive database of materials, each with:Properties: Name, type, atomic mass, critical temperature (Tc), valence electrons, crystal structure, critical magnetic field (Hc), critical current density (Jc), Debye temperature.
Categories:Elemental Superconductors (e.g., Nb, Pb, Hg).
High-Pressure Elements (e.g., Si, Bi).
Alloys & Intermetallics (e.g., NbTi, MgB2).
Cuprates (e.g., YBCO, Hg1223).
Iron-Based Superconductors (e.g., SmFeAsO).
Fullerides, Borocarbides, and others.
High-Pressure Hydrides (e.g., LaH10, YH9).

Crystal Structures: BCC, FCC, HCP, A15, Tetragonal, Orthorhombic, etc., with a compatibility matrix for multi-material compounds.

Calculation ModelsCritical Temperature (Tc):Uses a simplified BCS model: Tc ~ θ_D * exp(-1/(N(0)V)).
Incorporates Matthias's rules for alloys based on valence electrons.
Adjusts for doping (SiC enhances Jc, oxygen boosts Tc for cuprates) and pressure (enhances Tc for high-pressure materials).

Critical Current Density (Jc):Weighted average of material Jc, scaled by doping effects.

Critical Magnetic Field (Hc):Calculated with temperature dependence: Hc(T) = Hc(0) * (1 - (T/Tc)^2).

Crystal Compatibility:Uses a predefined matrix to score structural compatibility between materials.

Stability Checks:Flags toxic materials (e.g., Hg, Tl) and pressure mismatches for hydrides.

DependenciesChart.js: Used for visualizing Jc and Hc vs. temperature.Included via CDN: https://cdn.jsdelivr.net/npm/chart.js.

No additional installations required.

LimitationsSimplified Models: The simulator uses approximations (BCS theory, Matthias's rules) and does not account for all real-world factors (e.g., lattice dynamics, defects).
Static Database: Material properties are hardcoded and may not reflect the latest experimental data.
Theoretical Predictions: Results are estimates and require experimental validation.
Valence Electrons: Some materials (e.g., cuprates) lack valence electron data, limiting Matthias's rule applicability.
Browser Compatibility: Requires a modern browser with JavaScript enabled.

ContributingContributions are welcome! To contribute:Fork the repository.
Create a feature branch (git checkout -b feature/your-feature).
Commit changes (git commit -m 'Add your feature').
Push to the branch (git push origin feature/your-feature).
Open a pull request with a description of changes.

Please include:Clear commit messages.
Documentation updates for new features.
Tests or examples for new functionality.

LicenseThis project is licensed under the MIT License. See the LICENSE file for details.

