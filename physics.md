# Physics

↑ **Parent:** [Natural science](science.md#natural-science)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Physics)

Physics (like all well done [science](science.md)) is the [art](art.md) of predicting the future by modelling the world with [mathematics](mathematics.md).

And predicting the future is the first step towards [controlling](calculus.md#control-engineering) it, i.e.: [engineering](technology.md#engineering).

[Ciro Santilli](ciro-santilli.md) doesn't know physics. He writes about it partly to start playing with some scientific content for: [OurBigBook.com](ourbigbook-com.md), partly because this stuff is just amazingly beautiful.

Ciro's main intellectual [physics](physics.md) [fetishes](brain.md#fetish) are to learn [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics) (understanding the point of [Lie groups](geometry.md#lie-group) being a subpart of that) and [condensed matter physics](condensed-matter-physics.md).

Every science [is Physics in disguise](science.md#reductionism), but the number of objects in the real world is so large that we can't solve the real equations in practice.

Luckily, due to [emergence](science.md#emergence), we can use uglier higher level approximations of the world to solve many problems, with the complex limits of applicability of those approximations.

Therefore, such higher level approximations are highly specialized, and given different names such as:
- [chemistry](chemistry.md)
- [biology](biology.md)

As of 2019, all known physics can be described by two theories:
- the [Standard Model](standard-model.md)
- [general relativity](relativity.md#general-relativity)

Unifying those two into the [theory of everything](standard-model.md#theory-of-everything) one of the major goals of modern physics.

<a id="image-xkcd-435-fields-arranged-by-purity"></a>
![](https://web.archive.org/web/20190925220347if_/https://imgs.xkcd.com/comics/purity.png)

**[Figure 1](#image-xkcd-435-fields-arranged-by-purity). xkcd 435: Fields arranged by purity**. [Source](https://xkcd.com/435/). [Reductionism](science.md#reductionism) comes to mind.

<a id="image-physically-accurate-genie-by-psychomic"></a>
<img src="https://archive.ph/rXzBu/c4f9e6589c6b9a6ea675bc883f3f28495c0de365.jpg" alt="" height="1000">

**[Figure 2](#image-physically-accurate-genie-by-psychomic). Physically accurate genie by Psychomic**. [Source](https://www.webtoons.com/en/canvas/psychomic-/genie/viewer?title\_no=473571&episode\_no=26&webtoonType=CHALLENGE). This sane square composition from: [https://www.reddit.com/r/funny/comments/u08dw3/nice_guy_genie/](https://www.reddit.com/r/funny/comments/u08dw3/nice_guy_genie/).

**Table of contents**

- [How to teach and learn physics](#how-to-teach-and-learn-physics)
  - [Physics education needs more focus on understanding experiments and their history](#physics-education-needs-more-focus-on-understanding-experiments-and-their-history)
    - [There is value in tutorials written by early pioneers of the field](#there-is-value-in-tutorials-written-by-early-pioneers-of-the-field)
  - [Doing physics means calculating a number](#doing-physics-means-calculating-a-number)
    - [Physics is a way to predict the future](#physics-is-a-way-to-predict-the-future)
  - [It is OK to treat things as black boxes](#it-is-ok-to-treat-things-as-black-boxes)
- [The most important physics experiments](#the-most-important-physics-experiments)
  - [Physics experiment without a decent modern video](#physics-experiment-without-a-decent-modern-video)
  - [Aharonov-Bohm effect](#aharonov-bohm-effect)
  - [Compton scattering](#compton-scattering)
  - [Photoelectric effect](#photoelectric-effect)
- [System of units](system-of-units.md)
  - [Intrinsic standards](system-of-units.md#intrinsic-standards)
  - [Physical constant](system-of-units.md#physical-constant)
  - [Metrology](system-of-units.md#metrology)
    - [Metrology institute](system-of-units.md#metrology-institute)
  - [Unit of measurement](system-of-units.md#unit-of-measurement)
    - [Dimension (system of units)](system-of-units.md#dimension-system-of-units)
  - [List of systems of units](system-of-units.md#list-of-systems-of-units)
    - [International System of Units](system-of-units.md#international-system-of-units)
      - [International Bureau of Weights and Measures](system-of-units.md#international-bureau-of-weights-and-measures)
      - [Origins of Precision by Machine Thinking (2017)](system-of-units.md#origins-of-precision-by-machine-thinking-2017)
      - [Versions of the international System of Units](system-of-units.md#versions-of-the-international-system-of-units)
        - [2019 redefinition of the SI base units](system-of-units.md#2019-redefinition-of-the-si-base-units)
          - [2019 redefinition of the Kilogram](system-of-units.md#2019-redefinition-of-the-kilogram)
      - [Unit of the International System of Units](system-of-units.md#unit-of-the-international-system-of-units)
        - [Ampere](system-of-units.md#ampere)
          - [Ampere in the 2019 redefinition of the SI base units](system-of-units.md#ampere-in-the-2019-redefinition-of-the-si-base-units)
        - [Kilogram](system-of-units.md#kilogram)
          - [Avogadro project](system-of-units.md#avogadro-project)
          - [Kibble balance](system-of-units.md#kibble-balance)
      - [Dimension of the International System of Units](system-of-units.md#dimension-of-the-international-system-of-units)
        - [Luminous intensity](system-of-units.md#luminous-intensity)
          - [Candela](system-of-units.md#candela)
            - [Lumen (unit)](system-of-units.md#lumen-unit)
              - [Candela vs lumen](system-of-units.md#candela-vs-lumen)
        - [Weight](system-of-units.md#weight)
        - [Time](system-of-units.md#time)
          - [Frequency](system-of-units.md#frequency)
            - [Period (physics)](system-of-units.md#period-physics)
            - [Hertz](system-of-units.md#hertz)
              - [Megahertz](system-of-units.md#megahertz)
          - [Clock](system-of-units.md#clock)
            - [Quartz clock](system-of-units.md#quartz-clock)
            - [Atomic clock](system-of-units.md#atomic-clock)
              - [Caesium standard](system-of-units.md#caesium-standard)
          - [Unit of time](system-of-units.md#unit-of-time)
            - [Decimal time](system-of-units.md#decimal-time)
            - [Second](system-of-units.md#second)
            - [Day](system-of-units.md#day)
              - [Calendar](system-of-units.md#calendar)
            - [Year](system-of-units.md#year)
              - [2025](system-of-units.md#2025)
              - [2024](system-of-units.md#2024)
              - [2023](system-of-units.md#2023)
        - [Length](system-of-units.md#length)
          - [Meter](system-of-units.md#meter)
            - [Micrometer](system-of-units.md#micrometer)
            - [Nanometer](system-of-units.md#nanometer)
            - [Angstrom](system-of-units.md#angstrom)
            - [Picometer](system-of-units.md#picometer)
          - [Gauge block](system-of-units.md#gauge-block)
          - [Light year](system-of-units.md#light-year)
      - [Geiger counter](system-of-units.md#geiger-counter)
      - [Natural units](system-of-units.md#natural-units)
        - [Planck units](system-of-units.md#planck-units)
    - [Imperial units](system-of-units.md#imperial-units)
- [Particle physics](particle-physics.md)
  - [Electromagnetism](electromagnetism.md)
    - [Maxwell's equations](electromagnetism.md#maxwell-s-equations)
      - [Faraday's law of induction](electromagnetism.md#faraday-s-law-of-induction)
        - [Electromagnetic induction](electromagnetism.md#electromagnetic-induction)
          - [Inductive sensor](electromagnetism.md#inductive-sensor)
      - [Lorentz force](electromagnetism.md#lorentz-force)
        - [Ampère's force law](electromagnetism.md#ampere-s-force-law)
      - [Explicit scalar form of the Maxwell's equations](electromagnetism.md#explicit-scalar-form-of-the-maxwell-s-equations)
        - [Overdetermination of Maxwell's equations](electromagnetism.md#overdetermination-of-maxwell-s-equations)
      - [Coulomb's law](electromagnetism.md#coulomb-s-law)
      - [Solutions of Maxwell's equations](electromagnetism.md#solutions-of-maxwell-s-equations)
        - [Maxwell's equations with pointlike particles](electromagnetism.md#maxwell-s-equations-with-pointlike-particles)
      - [Maxwell's equations in 2D](electromagnetism.md#maxwell-s-equations-in-2d)
      - [Existence and uniqueness of solutions to Maxwell's equations](electromagnetism.md#existence-and-uniqueness-of-solutions-to-maxwell-s-equations)
      - [Electric field](electromagnetism.md#electric-field)
        - [Electric charge](electromagnetism.md#electric-charge)
          - [Electric charge measure unit](electromagnetism.md#electric-charge-measure-unit)
            - [Coulomb](electromagnetism.md#coulomb)
          - [Charge conservation](electromagnetism.md#charge-conservation)
          - [Electric current](electromagnetism.md#electric-current)
        - [Electric potential](electromagnetism.md#electric-potential)
          - [Volt](electromagnetism.md#volt)
            - [Voltmeter](electromagnetism.md#voltmeter)
              - [Electrometer](electromagnetism.md#electrometer)
              - [Nanovoltmeter](electromagnetism.md#nanovoltmeter)
            - [Voltage](electromagnetism.md#voltage)
            - [Electronvolt](electromagnetism.md#electronvolt)
      - [Hall effect](electromagnetism.md#hall-effect)
        - [Hall resistance](electromagnetism.md#hall-resistance)
        - [Charge carrier density](electromagnetism.md#charge-carrier-density)
        - [Hall effect sensor](electromagnetism.md#hall-effect-sensor)
      - [Electromagnetic four-potential](electromagnetism.md#electromagnetic-four-potential)
        - [Electromagnetic tensor](electromagnetism.md#electromagnetic-tensor)
        - [Four-current](electromagnetism.md#four-current)
        - [Lorentz gauge condition](electromagnetism.md#lorentz-gauge-condition)
          - [Coulomb gauge](electromagnetism.md#coulomb-gauge)
    - [Magnetism](electromagnetism.md#magnetism)
      - [Magnetic field](electromagnetism.md#magnetic-field)
        - [Magnetic B and H field](electromagnetism.md#magnetic-b-and-h-field)
        - [Tesla (unit)](electromagnetism.md#tesla-unit)
      - [Magnetic moment](electromagnetism.md#magnetic-moment)
      - [Magnetometer](electromagnetism.md#magnetometer)
      - [Magnetic flux](electromagnetism.md#magnetic-flux)
      - [Magnetic vector potential](electromagnetism.md#magnetic-vector-potential)
  - [Relativity](relativity.md)
    - [Special relativity](relativity.md#special-relativity)
      - [Invariance of the speed of light](relativity.md#invariance-of-the-speed-of-light)
      - [History of special relativity](relativity.md#history-of-special-relativity)
        - [Luminiferous aether](relativity.md#luminiferous-aether)
          - [Aether theory](relativity.md#aether-theory)
        - [Aether drag hypothesis](relativity.md#aether-drag-hypothesis)
          - [Lorentz ether theory](relativity.md#lorentz-ether-theory)
      - [Special relativity experiment](relativity.md#special-relativity-experiment)
        - [Aberration (astronomy)](relativity.md#aberration-astronomy)
        - [Fizeau experiment](relativity.md#fizeau-experiment)
        - [Michelson-Morley experiment](relativity.md#michelson-morley-experiment)
          - [On the Relative Motion of the Earth and the Luminiferous Ether](relativity.md#on-the-relative-motion-of-the-earth-and-the-luminiferous-ether)
        - [Hafele-Keating experiment](relativity.md#hafele-keating-experiment)
      - [Einstein synchronization](relativity.md#einstein-synchronization)
        - [Frame of reference](relativity.md#frame-of-reference)
          - [Inertial frame of reference](relativity.md#inertial-frame-of-reference)
      - [Lorentz transformation](relativity.md#lorentz-transformation)
        - [Lorentz covariance](relativity.md#lorentz-covariance)
          - [Lorentz invariant](relativity.md#lorentz-invariant)
        - [Lorentz transform consequence: everyone sees the same speed of light](relativity.md#lorentz-transform-consequence-everyone-sees-the-same-speed-of-light)
        - [Length contraction](relativity.md#length-contraction)
          - [Terrell rotation](relativity.md#terrell-rotation)
        - [Time dilation](relativity.md#time-dilation)
          - [Transversal time dilation](relativity.md#transversal-time-dilation)
          - [Transverse Doppler effect](relativity.md#transverse-doppler-effect)
        - [Twin paradox](relativity.md#twin-paradox)
      - [Maxwell's equations require special relativity](relativity.md#maxwell-s-equations-require-special-relativity)
        - [Deriving magnetism from electricity and relativity](relativity.md#deriving-magnetism-from-electricity-and-relativity)
        - [Moving magnet and conductor problem](relativity.md#moving-magnet-and-conductor-problem)
        - [Covariant formulation of classical electromagnetism](relativity.md#covariant-formulation-of-classical-electromagnetism)
          - [Maxwell's equations are Lorentz invariant](relativity.md#maxwell-s-equations-are-lorentz-invariant)
          - [Maxwell's equations imply that the speed of light is the same for all inertial reference frames](relativity.md#maxwell-s-equations-imply-that-the-speed-of-light-is-the-same-for-all-inertial-reference-frames)
          - [Maxwell Lagrangian](relativity.md#maxwell-lagrangian)
      - [Spacetime](relativity.md#spacetime)
        - [Four-vector](relativity.md#four-vector)
        - [Four-gradient](relativity.md#four-gradient)
        - [Minkowski space](relativity.md#minkowski-space)
          - [Minkowski inner product](relativity.md#minkowski-inner-product)
            - [Minkowski inner product matrix](relativity.md#minkowski-inner-product-matrix)
        - [Spacetime diagram](relativity.md#spacetime-diagram)
          - [Light cone](relativity.md#light-cone)
            - [Timelike-separated event](relativity.md#timelike-separated-event)
            - [Spacelike-separated event](relativity.md#spacelike-separated-event)
      - [Relativistic mechanics](relativity.md#relativistic-mechanics)
        - [Four-momentum](relativity.md#four-momentum)
          - [Relativistic energy](relativity.md#relativistic-energy)
            - [Energy-momentum relation](relativity.md#energy-momentum-relation)
            - [Mass-energy equivalence](relativity.md#mass-energy-equivalence)
          - [Spacetime interval](relativity.md#spacetime-interval)
            - [Proper time](relativity.md#proper-time)
    - [General relativity](relativity.md#general-relativity)
      - [Tests of general relativity](relativity.md#tests-of-general-relativity)
        - [Perihelion precession of Mercury](relativity.md#perihelion-precession-of-mercury)
        - [Gravitational wave](relativity.md#gravitational-wave)
          - [Gravitational wave detection](relativity.md#gravitational-wave-detection)
            - [Hulse-Taylor pulsar](relativity.md#hulse-taylor-pulsar)
            - [LIGO](relativity.md#ligo)
      - [Why gravity is not a force?](relativity.md#why-gravity-is-not-a-force)
      - [Maxwell's equations in curved spacetime](relativity.md#maxwell-s-equations-in-curved-spacetime)
      - [Gravity](relativity.md#gravity)
        - [Gravimetry](relativity.md#gravimetry)
          - [Gravimeter](relativity.md#gravimeter)
        - [Gravitational constant](relativity.md#gravitational-constant)
          - [Experiments that measure the gravitational constant](relativity.md#experiments-that-measure-the-gravitational-constant)
            - [Cavendish experiment](relativity.md#cavendish-experiment)
        - [Graviton](relativity.md#graviton)
  - [Standard Model](standard-model.md)
    - [Theory of everything](standard-model.md#theory-of-everything)
      - [Grand Unified Theory](standard-model.md#grand-unified-theory)
      - [The standard model and general relativity are incompatible](standard-model.md#the-standard-model-and-general-relativity-are-incompatible)
      - [Fundamental interaction](standard-model.md#fundamental-interaction)
      - [Quantum gravity](standard-model.md#quantum-gravity)
        - [String theory](standard-model.md#string-theory)
    - [Subatomic particle](standard-model.md#subatomic-particle)
      - [Elementary particle](standard-model.md#elementary-particle)
        - [Are there more than 3 generations of particles in the Standard Model?](standard-model.md#are-there-more-than-3-generations-of-particles-in-the-standard-model)
        - [Defining properties of elementary particles](standard-model.md#defining-properties-of-elementary-particles)
        - [Photon](photon.md)
          - [Light](photon.md#light)
            - [Wave-particle duality](photon.md#wave-particle-duality)
              - [Corpuscular theory of light](photon.md#corpuscular-theory-of-light)
                - [Newton supported the corpuscular theory of light](photon.md#newton-supported-the-corpuscular-theory-of-light)
              - [Wave theory of light](photon.md#wave-theory-of-light)
                - [Diffraction of light](photon.md#diffraction-of-light)
                  - [Young's interference experiment](photon.md#young-s-interference-experiment)
                  - [Arago spot](photon.md#arago-spot)
              - [Electromagnetic radiation](photon.md#electromagnetic-radiation)
                - [History of the electromagnetic theory of light](photon.md#history-of-the-electromagnetic-theory-of-light)
                  - [Faraday effect](photon.md#faraday-effect)
            - [Light source](photon.md#light-source)
              - [Light source characteristic](photon.md#light-source-characteristic)
                - [Spectral coherence](photon.md#spectral-coherence)
                - [Spacial coherence](photon.md#spacial-coherence)
              - [Lamp](photon.md#lamp)
                - [Incandescent light bulb](photon.md#incandescent-light-bulb)
                - [Gas-discharge lamp](photon.md#gas-discharge-lamp)
                  - [Fluorescent lamp](photon.md#fluorescent-lamp)
                  - [Neon lamp](photon.md#neon-lamp)
            - [Optical fiber](photon.md#optical-fiber)
              - [Fiber optic equipment](photon.md#fiber-optic-equipment)
                - [Fiber optic cable](photon.md#fiber-optic-cable)
                - [Optical amplifier](photon.md#optical-amplifier)
                  - [Fiber optical amplifier](photon.md#fiber-optical-amplifier)
                    - [Erbium-doped fiber amplifier](photon.md#erbium-doped-fiber-amplifier)
              - [Fiber-optic communication](photon.md#fiber-optic-communication)
                - [Small Form-factor Pluggable](photon.md#small-form-factor-pluggable)
                - [Fiber optics cables often come in pairs because it is needed for duplex](photon.md#fiber-optics-cables-often-come-in-pairs-because-it-is-needed-for-duplex)
                - [Single-mode and multi-mode optical fiber](photon.md#single-mode-and-multi-mode-optical-fiber)
                  - [Single-mode optical fiber](photon.md#single-mode-optical-fiber)
                  - [Multi-mode optical fiber](photon.md#multi-mode-optical-fiber)
              - [History of fiber optics](photon.md#history-of-fiber-optics)
                - [Optical fiber engineer](photon.md#optical-fiber-engineer)
                  - [Charles K. Kao](photon.md#charles-k-kao)
              - [Optical fiber bibliography](photon.md#optical-fiber-bibliography)
                - [City of Light: The Story of Fiber Optics](photon.md#city-of-light-the-story-of-fiber-optics)
              - [Optical fiber equipment](photon.md#optical-fiber-equipment)
                - [Fiberscope](photon.md#fiberscope)
                - [Fiber optic coupling](photon.md#fiber-optic-coupling)
            - [Photometer](photon.md#photometer)
              - [Spectophotometry](photon.md#spectophotometry)
            - [Spectroscopy](photon.md#spectroscopy)
            - [Speed of light](photon.md#speed-of-light)
              - [Speed of light experiment](photon.md#speed-of-light-experiment)
                - [Fizeau's determination of the speed of light with a rotating cogwheel](photon.md#fizeau-s-determination-of-the-speed-of-light-with-a-rotating-cogwheel)
              - [Emission theory (vision)](photon.md#emission-theory-vision)
              - [Faster-than-light](photon.md#faster-than-light)
                - [Faster-than-light implies time travel](photon.md#faster-than-light-implies-time-travel)
                - [Tachyon](photon.md#tachyon)
                - [Tachyonic antitelephone](photon.md#tachyonic-antitelephone)
            - [Electromagnetic spectrum](photon.md#electromagnetic-spectrum)
              - [Ionizing and non-ionizing radiation](photon.md#ionizing-and-non-ionizing-radiation)
                - [Ionizing radiation](photon.md#ionizing-radiation)
                  - [Ionization of air by radiation ](photon.md#ionization-of-air-by-radiation)
                - [Non-ionizing radiation](photon.md#non-ionizing-radiation)
              - [Very low frequency](photon.md#very-low-frequency)
              - [Radio wave](photon.md#radio-wave)
                - [Microwave](photon.md#microwave)
                  - [Ultra High Frequency](photon.md#ultra-high-frequency)
                  - [Microwave source](photon.md#microwave-source)
                    - [Klystron](photon.md#klystron)
                    - [Cavity magnetron](photon.md#cavity-magnetron)
                  - [Microwave transmission](photon.md#microwave-transmission)
                    - [Microwave transmission for trading](photon.md#microwave-transmission-for-trading)
                    - [Microwave vs radio wave transmission](photon.md#microwave-vs-radio-wave-transmission)
                  - [Microwave oven](photon.md#microwave-oven)
              - [Infrared](photon.md#infrared)
              - [Visible spectrum](photon.md#visible-spectrum)
              - [Ultraviolet](photon.md#ultraviolet)
              - [X-ray](photon.md#x-ray)
                - [X-ray source](photon.md#x-ray-source)
                  - [X-ray tube](photon.md#x-ray-tube)
          - [Photon spin](photon.md#photon-spin)
          - [Radiation pressure](photon.md#radiation-pressure)
            - [Nichols radiometer](photon.md#nichols-radiometer)
            - [Solar sail](photon.md#solar-sail)
          - [Single photon production and detection](photon.md#single-photon-production-and-detection)
            - [Single photon production](photon.md#single-photon-production)
              - [Spontaneous parametric down-conversion](photon.md#spontaneous-parametric-down-conversion)
            - [Single photon detection](photon.md#single-photon-detection)
              - [Photomultiplier](photon.md#photomultiplier)
                - [Photomultiplier tube](photon.md#photomultiplier-tube)
                - [Silicon photomultiplier](photon.md#silicon-photomultiplier)
            - [Two photon interference experiment](photon.md#two-photon-interference-experiment)
          - [Squeezed state of light](photon.md#squeezed-state-of-light)
          - [Optics](photon.md#optics)
            - [Quantum optics](photon.md#quantum-optics)
            - [Optoelectronics](photon.md#optoelectronics)
            - [Optical component](photon.md#optical-component)
              - [Beam splitter](photon.md#beam-splitter)
              - [Half-silvered mirror](photon.md#half-silvered-mirror)
              - [Collimator](photon.md#collimator)
                - [Collimated beam](photon.md#collimated-beam)
                  - [Parallel light](photon.md#parallel-light)
              - [Diffraction grating](photon.md#diffraction-grating)
              - [Diaphragm (optics)](photon.md#diaphragm-optics)
              - [Lens](photon.md#lens)
                - [Biconvex spherical lens](photon.md#biconvex-spherical-lens)
                  - [Focal length](photon.md#focal-length)
              - [Photodetector](photon.md#photodetector)
            - [Camera obscura](photon.md#camera-obscura)
            - [Optical cavity](photon.md#optical-cavity)
            - [Optics vendor](photon.md#optics-vendor)
              - [Carl Zeiss AG](photon.md#carl-zeiss-ag)
                - [Carl Zeiss SMT](photon.md#carl-zeiss-smt)
            - [Point light source](photon.md#point-light-source)
            - [Photonics](photon.md#photonics)
              - [Silicon photonics](photon.md#silicon-photonics)
                - [Optical computing](photon.md#optical-computing)
                  - [Optical computing bibliography](photon.md#optical-computing-bibliography)
                    - [Deep learning with coherent nanophotonic circuits](photon.md#deep-learning-with-coherent-nanophotonic-circuits)
                  - [Optical interconnect](photon.md#optical-interconnect)
                  - [Optical switch](photon.md#optical-switch)
                    - [Optical switch company](photon.md#optical-switch-company)
                      - [Salience Labs](photon.md#salience-labs)
                  - [Optical computing company](photon.md#optical-computing-company)
                    - [Arago Inc](photon.md#arago-inc)
                    - [Celestial AI](photon.md#celestial-ai)
                    - [Flux Computing](photon.md#flux-computing)
                    - [Lightmatter](photon.md#lightmatter)
                    - [Lumai](photon.md#lumai)
                    - [Luminous Computing, Inc.](photon.md#luminous-computing-inc)
                    - [NcodiN](photon.md#ncodin)
              - [Photon polarization](photon.md#photon-polarization)
                - [Polarization of light](photon.md#polarization-of-light)
                - [Polarizer](photon.md#polarizer)
                  - [Fresnel equations](photon.md#fresnel-equations)
                    - [Brewster's angle](photon.md#brewster-s-angle)
                  - [History of polarization](photon.md#history-of-polarization)
                  - [Malus' Law](photon.md#malus-law)
                    - [Étienne-Louis Malus](photon.md#etienne-louis-malus)
                  - [Three polarizers 45 degrees apart](photon.md#three-polarizers-45-degrees-apart)
              - [Poincaré sphere](photon.md#poincare-sphere)
              - [Photonics equipment](photon.md#photonics-equipment)
                - [Acousto-optic modulator](photon.md#acousto-optic-modulator)
                - [Interferometer](photon.md#interferometer)
                  - [Fabry-Pérot interferometer](photon.md#fabry-perot-interferometer)
                  - [Mach-Zehnder interferometer](photon.md#mach-zehnder-interferometer)
                - [Optical fibre](photon.md#optical-fibre)
                - [Optical table](photon.md#optical-table)
                - [Optical ring resonator](photon.md#optical-ring-resonator)
        - [Higgs boson](standard-model.md#higgs-boson)
          - [Goldstone's theorem](standard-model.md#goldstone-s-theorem)
          - [Higgs mechanism](standard-model.md#higgs-mechanism)
        - [Lepton](standard-model.md#lepton)
          - [Electron](standard-model.md#electron)
            - [Elementary charge](standard-model.md#elementary-charge)
              - [Why do the electron and the proton have the same charge except for the opposite signs?](standard-model.md#why-do-the-electron-and-the-proton-have-the-same-charge-except-for-the-opposite-signs)
              - [Oil drop experiment](standard-model.md#oil-drop-experiment)
            - [Electron rest mass](standard-model.md#electron-rest-mass)
            - [Positron](standard-model.md#positron)
          - [Muon](standard-model.md#muon)
          - [Neutrino](standard-model.md#neutrino)
            - [Neutrino emission on Earth](standard-model.md#neutrino-emission-on-earth)
            - [Cowan-Reines neutrino experiment](standard-model.md#cowan-reines-neutrino-experiment)
      - [Composite particle](standard-model.md#composite-particle)
        - [Hadron](standard-model.md#hadron)
          - [Baryon](standard-model.md#baryon)
            - [Baryon vs meson vs lepton](standard-model.md#baryon-vs-meson-vs-lepton)
          - [Neutron](standard-model.md#neutron)
          - [Proton](standard-model.md#proton)
            - [Proton-to-electron mass ratio](standard-model.md#proton-to-electron-mass-ratio)
          - [Meson](standard-model.md#meson)
            - [Pion](standard-model.md#pion)
            - [Kaon](standard-model.md#kaon)
      - [Eightfold way (physics)](standard-model.md#eightfold-way-physics)
    - [Parameters of the Standard Model](standard-model.md#parameters-of-the-standard-model)
    - [Standard Model Lagrangian](standard-model.md#standard-model-lagrangian)
    - [Why do symmetries such as SU(3), SU(2) and U(1) matter in particle physics?](standard-model.md#why-do-symmetries-such-as-su-3-su-2-and-u-1-matter-in-particle-physics)
  - [Applications of particle physics](particle-physics.md#applications-of-particle-physics)
  - [Quantum mechanics](quantum-mechanics.md)
    - [Quantum mechanics experiment](quantum-mechanics.md#quantum-mechanics-experiment)
      - [Emission spectrum](quantum-mechanics.md#emission-spectrum)
        - [Spectral line](quantum-mechanics.md#spectral-line)
          - [NIST Atomic Spectra Database](quantum-mechanics.md#nist-atomic-spectra-database)
          - [Forbidden mechanism](quantum-mechanics.md#forbidden-mechanism)
            - [Selection rule](quantum-mechanics.md#selection-rule)
              - [Metastable electron](quantum-mechanics.md#metastable-electron)
                - [Triplet state](quantum-mechanics.md#triplet-state)
          - [Rydberg atom](quantum-mechanics.md#rydberg-atom)
          - [Hydrogen emission spectrum](quantum-mechanics.md#hydrogen-emission-spectrum)
            - [Gross hydrogen emission spectrum](quantum-mechanics.md#gross-hydrogen-emission-spectrum)
              - [Hydrogen 1-2 spectral line](quantum-mechanics.md#hydrogen-1-2-spectral-line)
            - [Rydberg formula](quantum-mechanics.md#rydberg-formula)
              - [Balmer series](quantum-mechanics.md#balmer-series)
            - [Hydrogen spectral series](quantum-mechanics.md#hydrogen-spectral-series)
              - [Pickering series](quantum-mechanics.md#pickering-series)
          - [Fine structure](quantum-mechanics.md#fine-structure)
            - [Fine structure constant](quantum-mechanics.md#fine-structure-constant)
            - [Hyperfine structure](quantum-mechanics.md#hyperfine-structure)
              - [Hydrogen line](quantum-mechanics.md#hydrogen-line)
          - [Zeeman effect](quantum-mechanics.md#zeeman-effect)
            - [Anomalous Zeeman effect](quantum-mechanics.md#anomalous-zeeman-effect)
      - [Double-slit experiment](quantum-mechanics.md#double-slit-experiment)
        - [Single particle double slit experiment](quantum-mechanics.md#single-particle-double-slit-experiment)
          - [Single electron double slit experiment](quantum-mechanics.md#single-electron-double-slit-experiment)
        - [Are particles bounced by the first wall in the double slit experiment?](quantum-mechanics.md#are-particles-bounced-by-the-first-wall-in-the-double-slit-experiment)
      - [Franck-Hertz experiment](quantum-mechanics.md#franck-hertz-experiment)
      - [Quantum Hall effect](quantum-mechanics.md#quantum-hall-effect)
        - [Integer quantum Hall effect](quantum-mechanics.md#integer-quantum-hall-effect)
        - [Fractional quantum Hall effect](quantum-mechanics.md#fractional-quantum-hall-effect)
          - [Fractional quantum Hall effect for $\nu = 1/m$](quantum-mechanics.md#fractional-quantum-hall-effect-for-nu-1-m)
          - [Fractional quantum Hall effect for $\nu \ne 1/m$](quantum-mechanics.md#fractional-quantum-hall-effect-for-nu-ne-1-m)
            - [Fractional quantum Hall effect 5/2](quantum-mechanics.md#fractional-quantum-hall-effect-5-2)
        - [Spin Hall effect](quantum-mechanics.md#spin-hall-effect)
      - [Macroscopic quantum phenomena](quantum-mechanics.md#macroscopic-quantum-phenomena)
    - [History of quantum mechanics](quantum-mechanics.md#history-of-quantum-mechanics)
      - [Timeline of quantum mechanics](quantum-mechanics.md#timeline-of-quantum-mechanics)
      - [Old quantum theory](quantum-mechanics.md#old-quantum-theory)
    - [History of quantum mechanics bibliography](quantum-mechanics.md#history-of-quantum-mechanics-bibliography)
      - [The Quantum Story by Jim Baggott (2011)](quantum-mechanics.md#the-quantum-story-by-jim-baggott-2011)
      - [The Old Quantum Theory by Dirk ter Haar (1967)](quantum-mechanics.md#the-old-quantum-theory-by-dirk-ter-haar-1967)
    - [Quantum mechanics bibliography](quantum-mechanics.md#quantum-mechanics-bibliography)
      - [Introductory Quantum Mechanics by Richard Fitzpatrick (2020)](quantum-mechanics.md#introductory-quantum-mechanics-by-richard-fitzpatrick-2020)
      - [The Principles of Quantum Mechanics by Paul Dirac (1930)](quantum-mechanics.md#the-principles-of-quantum-mechanics-by-paul-dirac-1930)
        - [The Principles of Quantum Mechanics by Paul Dirac revised fourth edition (1967)](quantum-mechanics.md#the-principles-of-quantum-mechanics-by-paul-dirac-revised-fourth-edition-1967)
      - [MIT 8.06 Quantum Physics III, Spring 2018 by Barton Zwiebach](quantum-mechanics.md#mit-8-06-quantum-physics-iii-spring-2018-by-barton-zwiebach)
      - [Applications of Quantum Mechanics by David Tong (2017)](quantum-mechanics.md#applications-of-quantum-mechanics-by-david-tong-2017)
      - [Quantum Mechanics for Engineers by Leon van Dommelen (2011)](quantum-mechanics.md#quantum-mechanics-for-engineers-by-leon-van-dommelen-2011)
      - [Quantum physics by Jim Branson (2003)](quantum-mechanics.md#quantum-physics-by-jim-branson-2003)
    - [Mathematical formulation of quantum mechanics](quantum-mechanics.md#mathematical-formulation-of-quantum-mechanics)
      - [Schrödinger picture](quantum-mechanics.md#schrodinger-picture)
        - [Schrödinger picture example: quantum harmonic oscillator](quantum-mechanics.md#schrodinger-picture-example-quantum-harmonic-oscillator)
        - [Wave function collapse](quantum-mechanics.md#wave-function-collapse)
          - [Interpretations of quantum mechanics](quantum-mechanics.md#interpretations-of-quantum-mechanics)
            - [Categorical quantum mechanics](quantum-mechanics.md#categorical-quantum-mechanics)
            - [EPR paradox](quantum-mechanics.md#epr-paradox)
            - [Many-worlds interpretation](quantum-mechanics.md#many-worlds-interpretation)
              - [Universal wavefunction](quantum-mechanics.md#universal-wavefunction)
      - [Born rule](quantum-mechanics.md#born-rule)
      - [Bra-ket notation](quantum-mechanics.md#bra-ket-notation)
      - [Dirac-von Neumann axioms](quantum-mechanics.md#dirac-von-neumann-axioms)
      - [Linearity of quantum mechanics](quantum-mechanics.md#linearity-of-quantum-mechanics)
      - [Observable](quantum-mechanics.md#observable)
      - [Phase-space formulation](quantum-mechanics.md#phase-space-formulation)
    - [Non-relativistic quantum mechanics](quantum-mechanics.md#non-relativistic-quantum-mechanics)
      - [Schrödinger equation](quantum-mechanics.md#schrodinger-equation)
        - [Time-independent Schrödinger equation](quantum-mechanics.md#time-independent-schrodinger-equation)
          - [Solving the Schrodinger equation with the time-independent Schrödinger equation](quantum-mechanics.md#solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation)
        - [Derivation of the Schrodinger equation](quantum-mechanics.md#derivation-of-the-schrodinger-equation)
          - [Why are complex numbers used in the Schrodinger equation?](quantum-mechanics.md#why-are-complex-numbers-used-in-the-schrodinger-equation)
        - [Schrodinger equation Hamiltonian](quantum-mechanics.md#schrodinger-equation-hamiltonian)
        - [The Schrodinger equation Hamiltonian has to be Hermitian](quantum-mechanics.md#the-schrodinger-equation-hamiltonian-has-to-be-hermitian)
        - [Solutions of the Schrodinger equation](quantum-mechanics.md#solutions-of-the-schrodinger-equation)
          - [Computational quantum mechanics](quantum-mechanics.md#computational-quantum-mechanics)
            - [Why it is hard to simulate quantum systems?](quantum-mechanics.md#why-it-is-hard-to-simulate-quantum-systems)
            - [Computational quantum mechanics software](quantum-mechanics.md#computational-quantum-mechanics-software)
              - [Quantum ESPRESSO](quantum-mechanics.md#quantum-espresso)
              - [QuTiP](quantum-mechanics.md#qutip)
          - [Schrödinger equation for a one dimensional particle](quantum-mechanics.md#schrodinger-equation-for-a-one-dimensional-particle)
          - [Schrödinger equation for a free one dimensional particle](quantum-mechanics.md#schrodinger-equation-for-a-free-one-dimensional-particle)
            - [Plane wave function](quantum-mechanics.md#plane-wave-function)
            - [Time-independent Schrödinger equation for a free one dimensional particle](quantum-mechanics.md#time-independent-schrodinger-equation-for-a-free-one-dimensional-particle)
          - [Particle in a box](quantum-mechanics.md#particle-in-a-box)
            - [Quantum well](quantum-mechanics.md#quantum-well)
          - [Quantum harmonic oscillator](quantum-mechanics.md#quantum-harmonic-oscillator)
            - [Quantum LC circuit](quantum-mechanics.md#quantum-lc-circuit)
            - [Hermite polynomials](quantum-mechanics.md#hermite-polynomials)
              - [Hermite functions](quantum-mechanics.md#hermite-functions)
            - [Ladder operator](quantum-mechanics.md#ladder-operator)
          - [Quantum tunnelling](quantum-mechanics.md#quantum-tunnelling)
          - [Schrödinger equation solution for the hydrogen atom](quantum-mechanics.md#schrodinger-equation-solution-for-the-hydrogen-atom)
            - [Atomic orbital](quantum-mechanics.md#atomic-orbital)
            - [Quantum number](quantum-mechanics.md#quantum-number)
              - [Principal quantum number](quantum-mechanics.md#principal-quantum-number)
              - [Azimuthal quantum number](quantum-mechanics.md#azimuthal-quantum-number)
                - [s-orbital](quantum-mechanics.md#s-orbital)
                - [p-orbital](quantum-mechanics.md#p-orbital)
                - [d-orbital](quantum-mechanics.md#d-orbital)
                - [f-orbital](quantum-mechanics.md#f-orbital)
              - [Magnetic quantum number](quantum-mechanics.md#magnetic-quantum-number)
              - [Spin quantum number](quantum-mechanics.md#spin-quantum-number)
                - [Spectroscopic notation](quantum-mechanics.md#spectroscopic-notation)
          - [Solutions for the Schrodinger equation with multiple particles](quantum-mechanics.md#solutions-for-the-schrodinger-equation-with-multiple-particles)
            - [Separable state](quantum-mechanics.md#separable-state)
            - [Solutions of the Schrodinger equation for two electrons](quantum-mechanics.md#solutions-of-the-schrodinger-equation-for-two-electrons)
            - [Orbital approximation](quantum-mechanics.md#orbital-approximation)
            - [Schrödinger equation solution for the helium atom](quantum-mechanics.md#schrodinger-equation-solution-for-the-helium-atom)
            - [Hartree-Fock method](quantum-mechanics.md#hartree-fock-method)
              - [Hartree-Fock method for the helium atom](quantum-mechanics.md#hartree-fock-method-for-the-helium-atom)
              - [Why do multiple electrons occupy the same orbital if electrons repel each other?](quantum-mechanics.md#why-do-multiple-electrons-occupy-the-same-orbital-if-electrons-repel-each-other)
              - [Aufbau principle](quantum-mechanics.md#aufbau-principle)
                - [Electron configuration](quantum-mechanics.md#electron-configuration)
                - [Electron configuration notation](quantum-mechanics.md#electron-configuration-notation)
                - [Why does 2s have less energy than 1s if they have the same principal quantum number?](quantum-mechanics.md#why-does-2s-have-less-energy-than-1s-if-they-have-the-same-principal-quantum-number)
                - [Madelung energy ordering rule](quantum-mechanics.md#madelung-energy-ordering-rule)
                  - [Exception to the Madelung energy ordering rule](quantum-mechanics.md#exception-to-the-madelung-energy-ordering-rule)
                - [Term symbol](quantum-mechanics.md#term-symbol)
                  - [Hund's rules](quantum-mechanics.md#hund-s-rules)
                    - [Hund's first rule](quantum-mechanics.md#hund-s-first-rule)
                    - [Hund's second rule](quantum-mechanics.md#hund-s-second-rule)
            - [Term symbols for carbon ground state](quantum-mechanics.md#term-symbols-for-carbon-ground-state)
            - [Schrödinger equation solution for molecule](quantum-mechanics.md#schrodinger-equation-solution-for-molecule)
              - [Schrödinger equation solution for the hydrogen molecule](quantum-mechanics.md#schrodinger-equation-solution-for-the-hydrogen-molecule)
              - [Chemical bond](quantum-mechanics.md#chemical-bond)
                - [Molecule](quantum-mechanics.md#molecule)
                  - [Molecule representation](quantum-mechanics.md#molecule-representation)
                    - [Ball-and-stick model](quantum-mechanics.md#ball-and-stick-model)
                  - [Isomer](quantum-mechanics.md#isomer)
                    - [Cis-trans isomerism](quantum-mechanics.md#cis-trans-isomerism)
                    - [Enantiomer](quantum-mechanics.md#enantiomer)
                    - [Polymorphism (materials science)](quantum-mechanics.md#polymorphism-materials-science)
                    - [Stereochemistry](quantum-mechanics.md#stereochemistry)
                - [Covalent bond](quantum-mechanics.md#covalent-bond)
                  - [Sigma bond](quantum-mechanics.md#sigma-bond)
                  - [Pi bond](quantum-mechanics.md#pi-bond)
                    - [Double bond](quantum-mechanics.md#double-bond)
                    - [Triple bond](quantum-mechanics.md#triple-bond)
                - [Ionic bond](quantum-mechanics.md#ionic-bond)
                - [Octet rule](quantum-mechanics.md#octet-rule)
          - [Two-state quantum system](quantum-mechanics.md#two-state-quantum-system)
            - [Bloch sphere](quantum-mechanics.md#bloch-sphere)
            - [Pauli matrix](quantum-mechanics.md#pauli-matrix)
        - [Born-Oppenheimer approximation](quantum-mechanics.md#born-oppenheimer-approximation)
        - [Uncertainty principle](quantum-mechanics.md#uncertainty-principle)
          - [Position and momentum space](quantum-mechanics.md#position-and-momentum-space)
            - [Position representation](quantum-mechanics.md#position-representation)
            - [Position operator](quantum-mechanics.md#position-operator)
            - [Momentum operator](quantum-mechanics.md#momentum-operator)
            - [Squeezed coherent state](quantum-mechanics.md#squeezed-coherent-state)
          - [Energy operator](quantum-mechanics.md#energy-operator)
            - [Time-energy uncertainty principle](quantum-mechanics.md#time-energy-uncertainty-principle)
          - [Angular momentum operator](quantum-mechanics.md#angular-momentum-operator)
            - [Total angular momentum operator](quantum-mechanics.md#total-angular-momentum-operator)
          - [Complementarity (physics)](quantum-mechanics.md#complementarity-physics)
        - [Conservation laws in Schrodinger equations](quantum-mechanics.md#conservation-laws-in-schrodinger-equations)
          - [Conservation of the square amplitude in the Schrodinger equation](quantum-mechanics.md#conservation-of-the-square-amplitude-in-the-schrodinger-equation)
            - [Probability current](quantum-mechanics.md#probability-current)
        - [Wave function](quantum-mechanics.md#wave-function)
          - [Matter wave](quantum-mechanics.md#matter-wave)
            - [Electron diffraction experiment](quantum-mechanics.md#electron-diffraction-experiment)
              - [Diffraction of Cathode Rays by a Thin Film by Thomson and Reid (1927)](quantum-mechanics.md#diffraction-of-cathode-rays-by-a-thin-film-by-thomson-and-reid-1927)
              - [Davisson-Germer experiment](quantum-mechanics.md#davisson-germer-experiment)
            - [de Broglie relations](quantum-mechanics.md#de-broglie-relations)
      - [Equivalent alternatives to the Schrodinger equation](quantum-mechanics.md#equivalent-alternatives-to-the-schrodinger-equation)
        - [Matrix mechanics](quantum-mechanics.md#matrix-mechanics)
          - [Quantum mechanical re-interpretation of kinematic and mechanical relations by Heisenberg (1925)](quantum-mechanics.md#quantum-mechanical-re-interpretation-of-kinematic-and-mechanical-relations-by-heisenberg-1925)
          - [Heisenberg picture](quantum-mechanics.md#heisenberg-picture)
        - [De Broglie-Bohm theory](quantum-mechanics.md#de-broglie-bohm-theory)
    - [Planck-Einstein relation](quantum-mechanics.md#planck-einstein-relation)
      - [Planck constant](quantum-mechanics.md#planck-constant)
        - [Reduced Planck constant](quantum-mechanics.md#reduced-planck-constant)
    - [Relativistic quantum mechanics](relativistic-quantum-mechanics.md)
      - [The Schrödinger equation is not relativistic](relativistic-quantum-mechanics.md#the-schrodinger-equation-is-not-relativistic)
      - [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation)
        - [Absorption, spontaneous and stimulated emission](relativistic-quantum-mechanics.md#absorption-spontaneous-and-stimulated-emission)
          - [Spontaneous emission](relativistic-quantum-mechanics.md#spontaneous-emission)
            - [Spontaneous emission defies causality](relativistic-quantum-mechanics.md#spontaneous-emission-defies-causality)
          - [Photon absorption](relativistic-quantum-mechanics.md#photon-absorption)
          - [Stimulated emission](relativistic-quantum-mechanics.md#stimulated-emission)
            - [History of stimulated emission](relativistic-quantum-mechanics.md#history-of-stimulated-emission)
              - [On the Quantum Theory of Radiation](relativistic-quantum-mechanics.md#on-the-quantum-theory-of-radiation)
          - [Einstein coefficients](relativistic-quantum-mechanics.md#einstein-coefficients)
        - [The Dirac equation predicts spin](relativistic-quantum-mechanics.md#the-dirac-equation-predicts-spin)
        - [Antimatter](relativistic-quantum-mechanics.md#antimatter)
        - [Particle creation and annihilation](relativistic-quantum-mechanics.md#particle-creation-and-annihilation)
          - [Particle decay](relativistic-quantum-mechanics.md#particle-decay)
            - [Pair production](relativistic-quantum-mechanics.md#pair-production)
          - [Relativistic particle in a box thought experiment](relativistic-quantum-mechanics.md#relativistic-particle-in-a-box-thought-experiment)
        - [The Dirac equation is consistent with special relativity](relativistic-quantum-mechanics.md#the-dirac-equation-is-consistent-with-special-relativity)
        - [Derivation of the Dirac equation](relativistic-quantum-mechanics.md#derivation-of-the-dirac-equation)
        - [Pauli equation](relativistic-quantum-mechanics.md#pauli-equation)
        - [Klein-Gordon equation](relativistic-quantum-mechanics.md#klein-gordon-equation)
          - [Derivation of the Klein-Gordon equation](relativistic-quantum-mechanics.md#derivation-of-the-klein-gordon-equation)
        - [Solutions of the Dirac equation](relativistic-quantum-mechanics.md#solutions-of-the-dirac-equation)
          - [Dirac equation solution for the hydrogen atom](relativistic-quantum-mechanics.md#dirac-equation-solution-for-the-hydrogen-atom)
        - [Spin (physics)](relativistic-quantum-mechanics.md#spin-physics)
          - [Spin experiments](relativistic-quantum-mechanics.md#spin-experiments)
            - [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment)
              - [The Stern-Gerlach experiment needs an inhomogenous magnetic field](relativistic-quantum-mechanics.md#the-stern-gerlach-experiment-needs-an-inhomogenous-magnetic-field)
              - [Stern-Gerlach experiment paper](relativistic-quantum-mechanics.md#stern-gerlach-experiment-paper)
                - [The experimental proof of directional quantization in the magnetic field](relativistic-quantum-mechanics.md#the-experimental-proof-of-directional-quantization-in-the-magnetic-field)
            - [Spintronics](relativistic-quantum-mechanics.md#spintronics)
              - [Spin valve](relativistic-quantum-mechanics.md#spin-valve)
              - [Tunnel magnetoresistance](relativistic-quantum-mechanics.md#tunnel-magnetoresistance)
              - [Giant magnetoresistance](relativistic-quantum-mechanics.md#giant-magnetoresistance)
              - [Spin-transfer torque](relativistic-quantum-mechanics.md#spin-transfer-torque)
          - [Spin number of a field](relativistic-quantum-mechanics.md#spin-number-of-a-field)
            - [Spin 0](relativistic-quantum-mechanics.md#spin-0)
            - [Spin half](relativistic-quantum-mechanics.md#spin-half)
            - [Spin 1](relativistic-quantum-mechanics.md#spin-1)
              - [Proca equation](relativistic-quantum-mechanics.md#proca-equation)
            - [Spin 2](relativistic-quantum-mechanics.md#spin-2)
            - [Why is the spin of the electron half?](relativistic-quantum-mechanics.md#why-is-the-spin-of-the-electron-half)
          - [Pauli exclusion principle](relativistic-quantum-mechanics.md#pauli-exclusion-principle)
            - [Slater determinant](relativistic-quantum-mechanics.md#slater-determinant)
            - [Fermions, bosons and anyons](relativistic-quantum-mechanics.md#fermions-bosons-and-anyons)
              - [Fermion](relativistic-quantum-mechanics.md#fermion)
              - [Boson](relativistic-quantum-mechanics.md#boson)
              - [Anyon](relativistic-quantum-mechanics.md#anyon)
                - [Abelian an non abelian anyons](relativistic-quantum-mechanics.md#abelian-an-non-abelian-anyons)
                  - [Abelian anyon](relativistic-quantum-mechanics.md#abelian-anyon)
                  - [Non Abelian anyon](relativistic-quantum-mechanics.md#non-abelian-anyon)
            - [Spin-statistics theorem](relativistic-quantum-mechanics.md#spin-statistics-theorem)
            - [Electron degeneracy pressure](relativistic-quantum-mechanics.md#electron-degeneracy-pressure)
        - [Dirac Lagrangian](relativistic-quantum-mechanics.md#dirac-lagrangian)
          - [Dirac adjoint](relativistic-quantum-mechanics.md#dirac-adjoint)
          - [Gamma matrices](relativistic-quantum-mechanics.md#gamma-matrices)
          - [Feynman slash notation](relativistic-quantum-mechanics.md#feynman-slash-notation)
      - [Quantum field theory](quantum-field-theory.md)
        - [Quantum field](quantum-field-theory.md#quantum-field)
        - [Mathematical formulation of quantum field theory](quantum-field-theory.md#mathematical-formulation-of-quantum-field-theory)
          - [Gauge theory](quantum-field-theory.md#gauge-theory)
            - [Lattice gauge theory](quantum-field-theory.md#lattice-gauge-theory)
            - [Gauge field](quantum-field-theory.md#gauge-field)
            - [Gauge symmetry](quantum-field-theory.md#gauge-symmetry)
          - [Fock space](quantum-field-theory.md#fock-space)
          - [Second quantization](quantum-field-theory.md#second-quantization)
            - [Canonical quantization](quantum-field-theory.md#canonical-quantization)
          - [Path integral formulation](quantum-field-theory.md#path-integral-formulation)
            - [Quantum particles take all possible paths](quantum-field-theory.md#quantum-particles-take-all-possible-paths)
            - [Propagator](quantum-field-theory.md#propagator)
            - [Infinitely many slits thought experiment](quantum-field-theory.md#infinitely-many-slits-thought-experiment)
          - [Renormalization](quantum-field-theory.md#renormalization)
            - [Mass renormalization](quantum-field-theory.md#mass-renormalization)
            - [Renormalization group](quantum-field-theory.md#renormalization-group)
            - [Cutoff energy](quantum-field-theory.md#cutoff-energy)
            - [Effective field theory](quantum-field-theory.md#effective-field-theory)
            - [Yang-Mills theory](quantum-field-theory.md#yang-mills-theory)
              - [Yang-Mills existence and mass gap](quantum-field-theory.md#yang-mills-existence-and-mass-gap)
                - [Wightman axioms](quantum-field-theory.md#wightman-axioms)
        - [Quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics)
          - [Quantum electrodynamics experiment](quantum-field-theory.md#quantum-electrodynamics-experiment)
            - [Lamb shift](quantum-field-theory.md#lamb-shift)
              - [Lamb-Retherford experiment](quantum-field-theory.md#lamb-retherford-experiment)
            - [Electron magnetic moment](quantum-field-theory.md#electron-magnetic-moment)
              - [Anomalous magnetic dipole moment](quantum-field-theory.md#anomalous-magnetic-dipole-moment)
                - [Anomalous magnetic dipole moment of the electron](quantum-field-theory.md#anomalous-magnetic-dipole-moment-of-the-electron)
                  - [The Magnetic Moment of the Electron by Kusch and Foley (1948)](quantum-field-theory.md#the-magnetic-moment-of-the-electron-by-kusch-and-foley-1948)
            - [Dirac equation vs quantum electrodynamics](quantum-field-theory.md#dirac-equation-vs-quantum-electrodynamics)
              - [The Dirac equation does not work for more than one electron](quantum-field-theory.md#the-dirac-equation-does-not-work-for-more-than-one-electron)
          - [Applications of quantum electrodynamics](quantum-field-theory.md#applications-of-quantum-electrodynamics)
          - [Quantum electrodynamics Lagrangian](quantum-field-theory.md#quantum-electrodynamics-lagrangian)
            - [Derivation of the quantum electrodynamics Lagrangian](quantum-field-theory.md#derivation-of-the-quantum-electrodynamics-lagrangian)
          - [What does it mean that photons are force carriers for electromagnetism?](quantum-field-theory.md#what-does-it-mean-that-photons-are-force-carriers-for-electromagnetism)
          - [Photon field](quantum-field-theory.md#photon-field)
          - [Schwinger effect](quantum-field-theory.md#schwinger-effect)
          - [Feynman diagram](quantum-field-theory.md#feynman-diagram)
            - [Feynman diagram solver](quantum-field-theory.md#feynman-diagram-solver)
            - [Does the exact position of vertices matter in Feynman diagrams?](quantum-field-theory.md#does-the-exact-position-of-vertices-matter-in-feynman-diagrams)
          - [Wheeler-Feynman absorber theory](quantum-field-theory.md#wheeler-feynman-absorber-theory)
          - [Cavity quantum electrodynamics](quantum-field-theory.md#cavity-quantum-electrodynamics)
            - [Circuit quantum electrodynamics](quantum-field-theory.md#circuit-quantum-electrodynamics)
          - [Positrons are electrons travelling back in time](quantum-field-theory.md#positrons-are-electrons-travelling-back-in-time)
          - [Quantum electrodynamics bibliography](quantum-field-theory.md#quantum-electrodynamics-bibliography)
            - [Quantum Theory of Radiation by Fermi (1932)](quantum-field-theory.md#quantum-theory-of-radiation-by-fermi-1932)
            - [Advanced quantum mechanics by Freeman Dyson (1951)](quantum-field-theory.md#advanced-quantum-mechanics-by-freeman-dyson-1951)
            - [Selected Papers on Quantum Electrodynamics by Julian Schwinger (1958)](quantum-field-theory.md#selected-papers-on-quantum-electrodynamics-by-julian-schwinger-1958)
            - [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](quantum-field-theory.md#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979)
              - [Quantum Mechanical View of Reality by Richard Feynman (1983)](quantum-field-theory.md#quantum-mechanical-view-of-reality-by-richard-feynman-1983)
            - [Quantum electrodynamics by Lifshitz et al. 2nd edition (1982)](quantum-field-theory.md#quantum-electrodynamics-by-lifshitz-et-al-2nd-edition-1982)
            - [Physics 253a by Sidney Coleman (1986)](quantum-field-theory.md#physics-253a-by-sidney-coleman-1986)
            - [QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)](quantum-field-theory.md#qed-and-the-men-who-made-it-dyson-feynman-schwinger-and-tomonaga-by-silvan-schweber-1994)
            - [Advanced quantum mechanics II by Douglas Gingrich (2004)](quantum-field-theory.md#advanced-quantum-mechanics-ii-by-douglas-gingrich-2004)
        - [Weak interaction](quantum-field-theory.md#weak-interaction)
          - [Electroweak interaction](quantum-field-theory.md#electroweak-interaction)
          - [Parity violation](quantum-field-theory.md#parity-violation)
            - [Wu experiment](quantum-field-theory.md#wu-experiment)
            - [CP Violation](quantum-field-theory.md#cp-violation)
              - [CPT symmetry](quantum-field-theory.md#cpt-symmetry)
              - [Strong CP problem](quantum-field-theory.md#strong-cp-problem)
          - [Weak charge](quantum-field-theory.md#weak-charge)
          - [W boson](quantum-field-theory.md#w-boson)
          - [Z boson](quantum-field-theory.md#z-boson)
        - [Quantum chromodynamics](quantum-field-theory.md#quantum-chromodynamics)
          - [Quark](quantum-field-theory.md#quark)
            - [Down quark](quantum-field-theory.md#down-quark)
            - [Up quark](quantum-field-theory.md#up-quark)
              - [Why do the up ad down quarks have different masses?](quantum-field-theory.md#why-do-the-up-ad-down-quarks-have-different-masses)
          - [Strange quark](quantum-field-theory.md#strange-quark)
          - [Gluon](quantum-field-theory.md#gluon)
            - [Glueball](quantum-field-theory.md#glueball)
          - [Proton decay](quantum-field-theory.md#proton-decay)
          - [Strong interaction](quantum-field-theory.md#strong-interaction)
          - [Color charge](quantum-field-theory.md#color-charge)
          - [Color confinement](quantum-field-theory.md#color-confinement)
        - [Quantum field theory simulations](quantum-field-theory.md#quantum-field-theory-simulations)
          - [Nielsen-Ninomiya theorem](quantum-field-theory.md#nielsen-ninomiya-theorem)
        - [Infinities in quantum field theory](quantum-field-theory.md#infinities-in-quantum-field-theory)
          - [Mathematical consistency of quantum field theory](quantum-field-theory.md#mathematical-consistency-of-quantum-field-theory)
        - [Internal and spacetime symmetries](quantum-field-theory.md#internal-and-spacetime-symmetries)
          - [Internal symmetry](quantum-field-theory.md#internal-symmetry)
          - [Spacetime symmetry](quantum-field-theory.md#spacetime-symmetry)
        - [Quantum field theory bibliography](quantum-field-theory.md#quantum-field-theory-bibliography)
          - [Quantum field theory lecture notes](quantum-field-theory.md#quantum-field-theory-lecture-notes)
            - [An Introduction to QED and QCD by Jeff Forshaw (1997)](quantum-field-theory.md#an-introduction-to-qed-and-qcd-by-jeff-forshaw-1997)
            - [Quantum Field Theory lecture notes by David Tong (2007)](quantum-field-theory.md#quantum-field-theory-lecture-notes-by-david-tong-2007)
            - [Quantum Field Theory book by Mark Srednicki (2006)](quantum-field-theory.md#quantum-field-theory-book-by-mark-srednicki-2006)
          - [Quantum field theory lectures](quantum-field-theory.md#quantum-field-theory-lectures)
            - [Relativistic Quantum Mechanics by Apoorva D Patel (2014)](quantum-field-theory.md#relativistic-quantum-mechanics-by-apoorva-d-patel-2014)
            - [New Revolutions in Particle Physics by Leonard Susskind (2009)](quantum-field-theory.md#new-revolutions-in-particle-physics-by-leonard-susskind-2009)
            - [David Tong's 2009 Quantum Field Theory lectures at the Perimeter Institute](quantum-field-theory.md#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute)
              - [Lecture 1](quantum-field-theory.md#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/lecture-1)
            - [Quantum field theory courses by Tobias Osborne](quantum-field-theory.md#quantum-field-theory-courses-by-tobias-osborne)
              - [Quantum field theory lecture by Tobias Osborne (2017)](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017)
                - [Lecture 1](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1)
                - [Lecture 2](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2)
                - [Lecture 3](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-3)
                - [Lecture 4](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-4)
                - [Lecture 5](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-5)
                - [Lecture 8](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-8)
                - [Lecture 9](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-9)
                - [Lecture 14](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-14)
                - [Lecture 15](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-15)
              - [Advanced quantum field theory lecture by Tobias Osborne (2017)](quantum-field-theory.md#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017)
                - [Lecture 2](quantum-field-theory.md#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2)
          - [Quantum field theory book](quantum-field-theory.md#quantum-field-theory-book)
            - [No-Nonsense Quantum Field Theory by Jakob Schwichtenberg (2020)](quantum-field-theory.md#no-nonsense-quantum-field-theory-by-jakob-schwichtenberg-2020)
            - [Quantum Field Theory for The Gifted Amateur by Tom Lancaster (2015)](quantum-field-theory.md#quantum-field-theory-for-the-gifted-amateur-by-tom-lancaster-2015)
            - [Student Friendly Quantum Field Theory by Robert D Klauber (2013)](quantum-field-theory.md#student-friendly-quantum-field-theory-by-robert-d-klauber-2013)
            - [Quantum field theory in a nutshell by Anthony Zee (2010)](quantum-field-theory.md#quantum-field-theory-in-a-nutshell-by-anthony-zee-2010)
            - [Problem Book in Quantum Field Theory by Voja Radovanovic (2008)](quantum-field-theory.md#problem-book-in-quantum-field-theory-by-voja-radovanovic-2008)
            - [Quantum Field Theory Demystified by David McMahon (2008)](quantum-field-theory.md#quantum-field-theory-demystified-by-david-mcmahon-2008)
            - [An Introduction To Quantum Field Theory by Peskin and Schroeder (1995)](quantum-field-theory.md#an-introduction-to-quantum-field-theory-by-peskin-and-schroeder-1995)
    - [Quantization (physics)](quantum-mechanics.md#quantization-physics)
      - [Quantization of a real scalar field](quantum-mechanics.md#quantization-of-a-real-scalar-field)
    - [Quantum superposition](quantum-mechanics.md#quantum-superposition)
    - [Quantum entanglement](quantum-mechanics.md#quantum-entanglement)
      - [Bell's theorem](quantum-mechanics.md#bell-s-theorem)
        - [Bell test experiment](quantum-mechanics.md#bell-test-experiment)
          - [Loopholes in Bell test experiments](quantum-mechanics.md#loopholes-in-bell-test-experiments)
        - [Local hidden-variable theory](quantum-mechanics.md#local-hidden-variable-theory)
    - [No-go theorem](quantum-mechanics.md#no-go-theorem)
  - [Experimental particle physics](particle-physics.md#experimental-particle-physics)
    - [Cross section (physics)](particle-physics.md#cross-section-physics)
      - [Barn (unit)](particle-physics.md#barn-unit)
    - [Particle detector](particle-physics.md#particle-detector)
      - [Cloud chamber](particle-physics.md#cloud-chamber)
      - [Bubble chamber](particle-physics.md#bubble-chamber)
    - [Particle accelerator](particle-physics.md#particle-accelerator)
      - [Particle accelerator facility](particle-physics.md#particle-accelerator-facility)
        - [CERN](particle-physics.md#cern)
          - [CERN experiment](particle-physics.md#cern-experiment)
            - [Large Hadron Collider](particle-physics.md#large-hadron-collider)
        - [Superconducting Super Collider](particle-physics.md#superconducting-super-collider)
      - [Synchrotron](particle-physics.md#synchrotron)
        - [Cyclotron](particle-physics.md#cyclotron)
          - [Landau quantization](particle-physics.md#landau-quantization)
            - [Landau level](particle-physics.md#landau-level)
  - [Nuclear physics](particle-physics.md#nuclear-physics)
    - [History of nuclear physics](particle-physics.md#history-of-nuclear-physics)
    - [Nuclear binding energy](particle-physics.md#nuclear-binding-energy)
      - [Semi-empirical mass formula](particle-physics.md#semi-empirical-mass-formula)
    - [Atomic nucleus](particle-physics.md#atomic-nucleus)
      - [Nucleon](particle-physics.md#nucleon)
      - [Nuclear force](particle-physics.md#nuclear-force)
    - [Nuclear reaction](particle-physics.md#nuclear-reaction)
      - [Nuclear fission](particle-physics.md#nuclear-fission)
        - [Neutron temperature](particle-physics.md#neutron-temperature)
          - [Fast neutron](particle-physics.md#fast-neutron)
          - [Thermal neutron](particle-physics.md#thermal-neutron)
            - [Neutron moderation](particle-physics.md#neutron-moderation)
          - [Slow neutron](particle-physics.md#slow-neutron)
        - [Fissile material](particle-physics.md#fissile-material)
        - [Nuclear chain reaction](particle-physics.md#nuclear-chain-reaction)
          - [Nuclear reactor](particle-physics.md#nuclear-reactor)
            - [Breeder reactor](particle-physics.md#breeder-reactor)
      - [Neutron capture](particle-physics.md#neutron-capture)
        - [Neutron cross section](particle-physics.md#neutron-cross-section)
      - [Radioactive decay](particle-physics.md#radioactive-decay)
        - [Type of radioactive decay](particle-physics.md#type-of-radioactive-decay)
          - [Alpha decay](particle-physics.md#alpha-decay)
            - [Cluster decay](particle-physics.md#cluster-decay)
            - [Spontaneous fission](particle-physics.md#spontaneous-fission)
            - [Alpha particle](particle-physics.md#alpha-particle)
              - [Alpha particles have low penetration depth](particle-physics.md#alpha-particles-have-low-penetration-depth)
              - [Geiger-Nuttall law](particle-physics.md#geiger-nuttall-law)
          - [Beta decay](particle-physics.md#beta-decay)
          - [Gamma ray](particle-physics.md#gamma-ray)
            - [Nuclear isomer](particle-physics.md#nuclear-isomer)
            - [Gamma spectroscopy](particle-physics.md#gamma-spectroscopy)
              - [Do all gamma rays have the same energy during a given nuclear reaction?](particle-physics.md#do-all-gamma-rays-have-the-same-energy-during-a-given-nuclear-reaction)
        - [Decay chain](particle-physics.md#decay-chain)
        - [Decay scheme](particle-physics.md#decay-scheme)
        - [Half-life](particle-physics.md#half-life)
    - [Isotope](particle-physics.md#isotope)
      - [Isotope separation](particle-physics.md#isotope-separation)
        - [Gaseous diffusion](particle-physics.md#gaseous-diffusion)
        - [Gas centrifuge](particle-physics.md#gas-centrifuge)
    - [Nuclear magnetic moment](particle-physics.md#nuclear-magnetic-moment)
      - [Nuclear magnetic resonance](particle-physics.md#nuclear-magnetic-resonance)
        - [History of NMR](particle-physics.md#history-of-nmr)
          - [Rabi's NMR experiment](particle-physics.md#rabi-s-nmr-experiment)
            - [Rabi resonance method](particle-physics.md#rabi-resonance-method)
        - [Larmor precession](particle-physics.md#larmor-precession)
          - [Larmor frequency](particle-physics.md#larmor-frequency)
        - [Nuclear magnetic resonance spectroscopy](particle-physics.md#nuclear-magnetic-resonance-spectroscopy)
        - [Magnetic resonance imaging](particle-physics.md#magnetic-resonance-imaging)
        - [NMR vendor](particle-physics.md#nmr-vendor)
          - [Bruker Corporation](particle-physics.md#bruker-corporation)
    - [Nuclear weapon](nuclear-weapon.md)
      - [Fission weapon](nuclear-weapon.md#fission-weapon)
        - [Fission weapon by geometry](nuclear-weapon.md#fission-weapon-by-geometry)
          - [Gun-type fission weapon](nuclear-weapon.md#gun-type-fission-weapon)
            - [Gun-type fission weapons don't work with plutonium](nuclear-weapon.md#gun-type-fission-weapons-don-t-work-with-plutonium)
          - [Implosion-type fission weapon](nuclear-weapon.md#implosion-type-fission-weapon)
            - [RaLa Experiment](nuclear-weapon.md#rala-experiment)
        - [Boosted fission weapon](nuclear-weapon.md#boosted-fission-weapon)
        - [Pit (nuclear weapon)](nuclear-weapon.md#pit-nuclear-weapon)
      - [Thermonuclear weapon](nuclear-weapon.md#thermonuclear-weapon)
        - [Mark 17 nuclear bomb](nuclear-weapon.md#mark-17-nuclear-bomb)
      - [Low-background steel](nuclear-weapon.md#low-background-steel)
      - [Nuclear weapon design](nuclear-weapon.md#nuclear-weapon-design)
        - [Physics package (nuclear weapon)](nuclear-weapon.md#physics-package-nuclear-weapon)
      - [Fizzle (nuclear explosion)](nuclear-weapon.md#fizzle-nuclear-explosion)
      - [Weapons-grade nuclear material](nuclear-weapon.md#weapons-grade-nuclear-material)
      - [Nuclear site](nuclear-weapon.md#nuclear-site)
      - [Nuclear weapons testing](nuclear-weapon.md#nuclear-weapons-testing)
        - [Nuclear weapon test](nuclear-weapon.md#nuclear-weapon-test)
        - [Nuclear weapon detonation](nuclear-weapon.md#nuclear-weapon-detonation)
          - [Atomic bombings of Hiroshima and Nagasaki](nuclear-weapon.md#atomic-bombings-of-hiroshima-and-nagasaki)
      - [Nuclear weapons program](nuclear-weapon.md#nuclear-weapons-program)
        - [American nuclear weapons program](nuclear-weapon.md#american-nuclear-weapons-program)
          - [American plutonium production](nuclear-weapon.md#american-plutonium-production)
          - [American nuclear weapon facility](nuclear-weapon.md#american-nuclear-weapon-facility)
            - [Hanford site](nuclear-weapon.md#hanford-site)
              - [B Reactor](nuclear-weapon.md#b-reactor)
            - [Savannah River site](nuclear-weapon.md#savannah-river-site)
            - [Pantex](nuclear-weapon.md#pantex)
          - [Nuclear football](nuclear-weapon.md#nuclear-football)
          - [Manhattan Project](nuclear-weapon.md#manhattan-project)
            - [Einstein-Szilard letter](nuclear-weapon.md#einstein-szilard-letter)
            - [Chicago Pile-1](nuclear-weapon.md#chicago-pile-1)
              - [Metallurgical Laboratory](nuclear-weapon.md#metallurgical-laboratory)
            - [Trinity (nuclear test)](nuclear-weapon.md#trinity-nuclear-test)
        - [British nuclear weapons program](nuclear-weapon.md#british-nuclear-weapons-program)
          - [Atomic Weapons Establishment](nuclear-weapon.md#atomic-weapons-establishment)
            - [AWE Aldermaston](nuclear-weapon.md#awe-aldermaston)
        - [French nuclear weapons program](nuclear-weapon.md#french-nuclear-weapons-program)
        - [German nuclear weapons program](nuclear-weapon.md#german-nuclear-weapons-program)
      - [Nuclear weapon delivery](nuclear-weapon.md#nuclear-weapon-delivery)
        - [Nuclear triad](nuclear-weapon.md#nuclear-triad)
        - [Intercontinental ballistic missile](nuclear-weapon.md#intercontinental-ballistic-missile)
          - [American Intercontinental ballistic missile](nuclear-weapon.md#american-intercontinental-ballistic-missile)
            - [LGM-30 Minuteman](nuclear-weapon.md#lgm-30-minuteman)
              - [Hardened Intersite Cable System](nuclear-weapon.md#hardened-intersite-cable-system)
        - [Multiple independently targetable reentry vehicle](nuclear-weapon.md#multiple-independently-targetable-reentry-vehicle)
      - [Salted bomb](nuclear-weapon.md#salted-bomb)
        - [Cobalt bomb](nuclear-weapon.md#cobalt-bomb)
      - [Tactical and strategic nuclear weapons](nuclear-weapon.md#tactical-and-strategic-nuclear-weapons)
        - [Strategic nuclear weapon](nuclear-weapon.md#strategic-nuclear-weapon)
        - [Tactical nuclear weapon](nuclear-weapon.md#tactical-nuclear-weapon)
      - [Variable yield](nuclear-weapon.md#variable-yield)
      - [List of nuclear weapons](nuclear-weapon.md#list-of-nuclear-weapons)
        - [Fat Man](nuclear-weapon.md#fat-man)
        - [Little Boy](nuclear-weapon.md#little-boy)
        - [Nuclear strategy](nuclear-weapon.md#nuclear-strategy)
  - [History of particle physics](particle-physics.md#history-of-particle-physics)
    - [The Harvest of a Century by Siegmund Brandt (2008)](particle-physics.md#the-harvest-of-a-century-by-siegmund-brandt-2008)
    - [Inward Bound by Abraham Pais (1988)](particle-physics.md#inward-bound-by-abraham-pais-1988)
  - [Radiation](particle-physics.md#radiation)
    - [Penetration of radiation](particle-physics.md#penetration-of-radiation)
  - [Particle physics bibliography](particle-physics.md#particle-physics-bibliography)
    - [PBS Space Time](particle-physics.md#pbs-space-time)
    - [2011 PHYS 485 lecture videos by Roger Moore from the University of Alberta](particle-physics.md#2011-phys-485-lecture-videos-by-roger-moore-from-the-university-of-alberta)
    - [Particle physics YouTube channel](particle-physics.md#particle-physics-youtube-channel)
      - [Andrew Dotson YouTube channel](particle-physics.md#andrew-dotson-youtube-channel)
        - [Andrew Dotson](particle-physics.md#andrew-dotson)
      - [Dietterich Labs](particle-physics.md#dietterich-labs)
      - [Pretty Much Physics](particle-physics.md#pretty-much-physics)
      - [ViaScience](particle-physics.md#viascience)
      - [Physics Videos by Eugene Khutoryansky](particle-physics.md#physics-videos-by-eugene-khutoryansky)
        - [Eugene Khutoryansky](particle-physics.md#eugene-khutoryansky)
      - [Don Lincoln](particle-physics.md#don-lincoln)
- [Energy](#energy)
  - [Unit of measurement for energy](#unit-of-measurement-for-energy)
    - [Joule](#joule)
    - [Watt](#watt)
  - [Conservation of energy](#conservation-of-energy)
  - [Potential energy](#potential-energy)
    - [Potential barrier](#potential-barrier)
  - [Kinetic energy](#kinetic-energy)
    - [Why kinetic energy is $mv^2/2$?](#why-kinetic-energy-is-mv-2-2)
  - [Work (physics)](#work-physics)
    - [Why work is force times distance?](#why-work-is-force-times-distance)
- [Experimental physics](#experimental-physics)
  - [Theoretical physics](#theoretical-physics)
- [Field (physics)](#field-physics)
  - [Principle of locality](#principle-of-locality)
    - [Causality](#causality)
      - [Causality in quantum mechanics](#causality-in-quantum-mechanics)
        - [Causality and quantum jumps are incompatible](#causality-and-quantum-jumps-are-incompatible)
- [Law of physics](#law-of-physics)
- [History of physics](#history-of-physics)
  - [Abraham Pais Prize for History of Physics](#abraham-pais-prize-for-history-of-physics)
- [Condensed matter physics](condensed-matter-physics.md)
  - [Atomic, Molecular and Optical Physics](condensed-matter-physics.md#atomic-molecular-and-optical-physics)
    - [Molecular beam](condensed-matter-physics.md#molecular-beam)
  - [Solid-state physics](condensed-matter-physics.md#solid-state-physics)
    - [Crystallography](condensed-matter-physics.md#crystallography)
      - [Crystal system](condensed-matter-physics.md#crystal-system)
      - [Point group](condensed-matter-physics.md#point-group)
        - [Point groups in two dimensions](condensed-matter-physics.md#point-groups-in-two-dimensions)
        - [Point groups in three dimensions](condensed-matter-physics.md#point-groups-in-three-dimensions)
        - [Crystallographic restriction theorem](condensed-matter-physics.md#crystallographic-restriction-theorem)
      - [Bravais lattice](condensed-matter-physics.md#bravais-lattice)
      - [Crystal](condensed-matter-physics.md#crystal)
    - [Topological insulator](condensed-matter-physics.md#topological-insulator)
      - [Topology in condensed matter](condensed-matter-physics.md#topology-in-condensed-matter)
  - [Electronic band theory](condensed-matter-physics.md#electronic-band-theory)
    - [Direct and indirect band gaps](condensed-matter-physics.md#direct-and-indirect-band-gaps)
  - [Electrical resistivity and conductivity](condensed-matter-physics.md#electrical-resistivity-and-conductivity)
    - [Electrical reactance](condensed-matter-physics.md#electrical-reactance)
      - [Electrical impedance](condensed-matter-physics.md#electrical-impedance)
    - [Four-terminal sensing](condensed-matter-physics.md#four-terminal-sensing)
    - [Dependence of electrical resistivity on tempreature](condensed-matter-physics.md#dependence-of-electrical-resistivity-on-tempreature)
      - [Kondo effect](condensed-matter-physics.md#kondo-effect)
    - [Semiconductor](condensed-matter-physics.md#semiconductor)
      - [Doping (semiconductor)](condensed-matter-physics.md#doping-semiconductor)
      - [Type of semiconductor](condensed-matter-physics.md#type-of-semiconductor)
        - [III-V semiconductor](condensed-matter-physics.md#iii-v-semiconductor)
    - [Superconductivity](condensed-matter-physics.md#superconductivity)
      - [Superconductor resistivity experiment video](condensed-matter-physics.md#superconductor-resistivity-experiment-video)
      - [Superconductor coil experiment video](condensed-matter-physics.md#superconductor-coil-experiment-video)
      - [Superconductivity is a a form of superfluidity](condensed-matter-physics.md#superconductivity-is-a-a-form-of-superfluidity)
      - [Cooper pair](condensed-matter-physics.md#cooper-pair)
      - [Superconducting temperature](condensed-matter-physics.md#superconducting-temperature)
      - [Superconducting phase diagram](condensed-matter-physics.md#superconducting-phase-diagram)
      - [Type of superconductor](condensed-matter-physics.md#type-of-superconductor)
        - [Type-I superconductor](condensed-matter-physics.md#type-i-superconductor)
        - [Type-II superconductor](condensed-matter-physics.md#type-ii-superconductor)
        - [High-temperature superconductivity](condensed-matter-physics.md#high-temperature-superconductivity)
          - [Room temperature superconductor](condensed-matter-physics.md#room-temperature-superconductor)
            - [Resonating valence bond theory](condensed-matter-physics.md#resonating-valence-bond-theory)
            - [Room temperature and pressure superconductor](condensed-matter-physics.md#room-temperature-and-pressure-superconductor)
              - [LK-99](condensed-matter-physics.md#lk-99)
          - [List of High-temperature superconductors](condensed-matter-physics.md#list-of-high-temperature-superconductors)
            - [Yttrium barium copper oxide](condensed-matter-physics.md#yttrium-barium-copper-oxide)
            - [Bismuth strontium calcium copper oxide](condensed-matter-physics.md#bismuth-strontium-calcium-copper-oxide)
      - [Superconducting material](condensed-matter-physics.md#superconducting-material)
      - [Applications of superconductivity](condensed-matter-physics.md#applications-of-superconductivity)
        - [Most important superconductor material](condensed-matter-physics.md#most-important-superconductor-material)
      - [Superconductor I-V curve](condensed-matter-physics.md#superconductor-i-v-curve)
        - [Do superconductors carry infinite current?](condensed-matter-physics.md#do-superconductors-carry-infinite-current)
      - [BCS Theory](condensed-matter-physics.md#bcs-theory)
      - [Josephson effect](condensed-matter-physics.md#josephson-effect)
        - [History of the Josephson effect](condensed-matter-physics.md#history-of-the-josephson-effect)
          - [Possible new effects in superconductive tunnelling](condensed-matter-physics.md#possible-new-effects-in-superconductive-tunnelling)
          - [Probable observation of the Josephson superconducting tunneling effect](condensed-matter-physics.md#probable-observation-of-the-josephson-superconducting-tunneling-effect)
        - [Josephson effect regime](condensed-matter-physics.md#josephson-effect-regime)
          - [DC Josephson effect](condensed-matter-physics.md#dc-josephson-effect)
          - [AC Josephson effect](condensed-matter-physics.md#ac-josephson-effect)
          - [Inverse AC Josephson effect](condensed-matter-physics.md#inverse-ac-josephson-effect)
            - [Shapiro steps](condensed-matter-physics.md#shapiro-steps)
        - [Josephson equations](condensed-matter-physics.md#josephson-equations)
          - [Josephson current](condensed-matter-physics.md#josephson-current)
          - [Josephson phase](condensed-matter-physics.md#josephson-phase)
        - [Josephson junction](condensed-matter-physics.md#josephson-junction)
          - [Pi Josephson junction](condensed-matter-physics.md#pi-josephson-junction)
        - [Magnetic flux quantum](condensed-matter-physics.md#magnetic-flux-quantum)
          - [Experimental Evidence for Quantized Flux in Superconducting Cylinders](condensed-matter-physics.md#experimental-evidence-for-quantized-flux-in-superconducting-cylinders)
          - [Josephson constant](condensed-matter-physics.md#josephson-constant)
        - [Symmetry breaking in superconductors](condensed-matter-physics.md#symmetry-breaking-in-superconductors)
        - [Applications of Josephson Junctions](condensed-matter-physics.md#applications-of-josephson-junctions)
          - [Josephson voltage standard](condensed-matter-physics.md#josephson-voltage-standard)
          - [SQUID device](condensed-matter-physics.md#squid-device)
            - [DC SQUID](condensed-matter-physics.md#dc-squid)
  - [Superconducting tunnel junction](condensed-matter-physics.md#superconducting-tunnel-junction)
  - [Superfluidity](condensed-matter-physics.md#superfluidity)
  - [State of matter](condensed-matter-physics.md#state-of-matter)
    - [High pressure](condensed-matter-physics.md#high-pressure)
  - [List of states of matter](condensed-matter-physics.md#list-of-states-of-matter)
    - [Solid](condensed-matter-physics.md#solid)
    - [Liquid](condensed-matter-physics.md#liquid)
    - [Gas](condensed-matter-physics.md#gas)
      - [Fermi gas](condensed-matter-physics.md#fermi-gas)
        - [Electron gas](condensed-matter-physics.md#electron-gas)
          - [Two-dimensional electron gas](condensed-matter-physics.md#two-dimensional-electron-gas)
            - [Laughlin wavefunction](condensed-matter-physics.md#laughlin-wavefunction)
        - [1D Fermi gas](condensed-matter-physics.md#1d-fermi-gas)
          - [Impenetrable Bose Gas](condensed-matter-physics.md#impenetrable-bose-gas)
    - [Bose-Einstein condensate](condensed-matter-physics.md#bose-einstein-condensate)
  - [Materials science](condensed-matter-physics.md#materials-science)
    - [Type of material](condensed-matter-physics.md#type-of-material)
      - [Glass](condensed-matter-physics.md#glass)
      - [Quantum dot](condensed-matter-physics.md#quantum-dot)
        - [Quantum dot single photon source](condensed-matter-physics.md#quantum-dot-single-photon-source)
      - [Metal](condensed-matter-physics.md#metal)
        - [Field electron emission](condensed-matter-physics.md#field-electron-emission)
        - [Alloy](condensed-matter-physics.md#alloy)
          - [Binary alloy](condensed-matter-physics.md#binary-alloy)
        - [Metallurgy](condensed-matter-physics.md#metallurgy)
          - [Ingot](condensed-matter-physics.md#ingot)
      - [Polymer](condensed-matter-physics.md#polymer)
        - [Plastic](condensed-matter-physics.md#plastic)
    - [Material property](condensed-matter-physics.md#material-property)
      - [Material property database](condensed-matter-physics.md#material-property-database)
        - [Open material property database](condensed-matter-physics.md#open-material-property-database)
          - [The Materials Project](condensed-matter-physics.md#the-materials-project)
      - [Density](condensed-matter-physics.md#density)
      - [Magnet](condensed-matter-physics.md#magnet)
        - [Permanent magnet](condensed-matter-physics.md#permanent-magnet)
          - [Curie temperature](condensed-matter-physics.md#curie-temperature)
          - [Ferromagnetism](condensed-matter-physics.md#ferromagnetism)
            - [Magnetic hysteresis](condensed-matter-physics.md#magnetic-hysteresis)
              - [Saturation magnetisation](condensed-matter-physics.md#saturation-magnetisation)
        - [Electromagnet](condensed-matter-physics.md#electromagnet)
          - [Electromagnetic coil](condensed-matter-physics.md#electromagnetic-coil)
          - [Solenoid](condensed-matter-physics.md#solenoid)
          - [Lifting electromagnet](condensed-matter-physics.md#lifting-electromagnet)
            - [Breaking Bad magnet scene](condensed-matter-physics.md#breaking-bad-magnet-scene)
        - [Ising model](condensed-matter-physics.md#ising-model)
          - [Solution of the Ising model](condensed-matter-physics.md#solution-of-the-ising-model)
          - [1D Ising model](condensed-matter-physics.md#1d-ising-model)
          - [2D Ising model](condensed-matter-physics.md#2d-ising-model)
          - [3D Ising model](condensed-matter-physics.md#3d-ising-model)
        - [Magnetic dipole](condensed-matter-physics.md#magnetic-dipole)
          - [Magnetic dipole moment](condensed-matter-physics.md#magnetic-dipole-moment)
          - [Interaction between a magnetic dipole and a magnetic field](condensed-matter-physics.md#interaction-between-a-magnetic-dipole-and-a-magnetic-field)
            - [Interaction between a magnetic dipole and a homogenous magnetic field](condensed-matter-physics.md#interaction-between-a-magnetic-dipole-and-a-homogenous-magnetic-field)
            - [Magnetic dipole in an inhomogenous magnetic field](condensed-matter-physics.md#magnetic-dipole-in-an-inhomogenous-magnetic-field)
        - [Compass](condensed-matter-physics.md#compass)
          - [Water compass](condensed-matter-physics.md#water-compass)
        - [Superconducting magnet](condensed-matter-physics.md#superconducting-magnet)
          - [Superconducting magnet vendor](condensed-matter-physics.md#superconducting-magnet-vendor)
            - [Oxford Instruments](condensed-matter-physics.md#oxford-instruments)
          - [High temperature superconductor superconducting magnet](condensed-matter-physics.md#high-temperature-superconductor-superconducting-magnet)
      - [Optical material property](condensed-matter-physics.md#optical-material-property)
        - [Black-body radiation](condensed-matter-physics.md#black-body-radiation)
          - [Planck's law](condensed-matter-physics.md#planck-s-law)
            - [Wien approximation](condensed-matter-physics.md#wien-approximation)
            - [Rayleigh-Jeans law](condensed-matter-physics.md#rayleigh-jeans-law)
          - [Black-body radiation experiment](condensed-matter-physics.md#black-body-radiation-experiment)
          - [Ultraviolet catastrophe](condensed-matter-physics.md#ultraviolet-catastrophe)
        - [Transparency (electromagnetic radiation)](condensed-matter-physics.md#transparency-electromagnetic-radiation)
          - [Absorption (electromagnetic radiation)](condensed-matter-physics.md#absorption-electromagnetic-radiation)
      - [Piezoelectricity](condensed-matter-physics.md#piezoelectricity)
        - [Piezoelectric actuator](condensed-matter-physics.md#piezoelectric-actuator)
          - [Piezoelectric motor](condensed-matter-physics.md#piezoelectric-motor)
        - [Piezo ignition](condensed-matter-physics.md#piezo-ignition)
      - [Photoluminescence](condensed-matter-physics.md#photoluminescence)
        - [Fluorescence](condensed-matter-physics.md#fluorescence)
          - [Fluorometer](condensed-matter-physics.md#fluorometer)
          - [Phosphorescence](condensed-matter-physics.md#phosphorescence)
      - [Specific heat capacity](condensed-matter-physics.md#specific-heat-capacity)
        - [Einstein solid](condensed-matter-physics.md#einstein-solid)
          - [Dulong-Petit law](condensed-matter-physics.md#dulong-petit-law)
        - [Debye model](condensed-matter-physics.md#debye-model)
      - [Viscosity](condensed-matter-physics.md#viscosity)
        - [Pitch drop experiment](condensed-matter-physics.md#pitch-drop-experiment)
  - [Laser](condensed-matter-physics.md#laser)
    - [History of the laser](condensed-matter-physics.md#history-of-the-laser)
      - [The History of the Laser by Mario Bertolotti](condensed-matter-physics.md#the-history-of-the-laser-by-mario-bertolotti)
    - [Laser spectrum](condensed-matter-physics.md#laser-spectrum)
      - [Laser linewidth](condensed-matter-physics.md#laser-linewidth)
      - [Laser gain curve](condensed-matter-physics.md#laser-gain-curve)
    - [Lasers vs other light sources](condensed-matter-physics.md#lasers-vs-other-light-sources)
      - [Lasers emit a narrow spectrum](condensed-matter-physics.md#lasers-emit-a-narrow-spectrum)
        - [Laser spectrum vs LED spectrum](condensed-matter-physics.md#laser-spectrum-vs-led-spectrum)
      - [Why can't you collimate incoherent light as well as a laser?](condensed-matter-physics.md#why-can-t-you-collimate-incoherent-light-as-well-as-a-laser)
    - [Type of laser](condensed-matter-physics.md#type-of-laser)
      - [Maser](condensed-matter-physics.md#maser)
      - [Fiber laser](condensed-matter-physics.md#fiber-laser)
      - [Gas laser](condensed-matter-physics.md#gas-laser)
      - [Laser diode](condensed-matter-physics.md#laser-diode)
        - [Laser pointer](condensed-matter-physics.md#laser-pointer)
      - [Three-level laser](condensed-matter-physics.md#three-level-laser)
      - [Four-level laser](condensed-matter-physics.md#four-level-laser)
    - [Are lasers polarized](condensed-matter-physics.md#are-lasers-polarized)
    - [Optical tweezers](condensed-matter-physics.md#optical-tweezers)
      - [Laser cooling](condensed-matter-physics.md#laser-cooling)
    - [Population inversion](condensed-matter-physics.md#population-inversion)
    - [Pulsed laser](condensed-matter-physics.md#pulsed-laser)
    - [Laser vendor](condensed-matter-physics.md#laser-vendor)
      - [Coherent, Inc.](condensed-matter-physics.md#coherent-inc)
  - [Quasiparticle](condensed-matter-physics.md#quasiparticle)
    - [Quasiparticles vs elementary particles](condensed-matter-physics.md#quasiparticles-vs-elementary-particles)
  - [History of condensed matter physics](condensed-matter-physics.md#history-of-condensed-matter-physics)
  - [Condensed matter Physics bibliography](condensed-matter-physics.md#condensed-matter-physics-bibliography)
    - [Condensed matter university course](condensed-matter-physics.md#condensed-matter-university-course)
      - [Theories of Quantum Matter by Austen Lamacraft](theories-of-quantum-matter-by-austen-lamacraft.md)
        - [Many Body Wavefunctions](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions)
          - [Bosons and Fermions](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/bosons-and-fermions)
            - [Two Particles](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/two-particles)
            - [Product States](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/product-states)
          - [The 1D Fermi Gas](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/the-1d-fermi-gas)
            - [Ground State](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/1d-fermi-gas-ground-state)
            - [Density; Density Matrix; Pair Distribution](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/1d-fermi-gas-density)
            - [Impenetrable Bose Gas](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/impenetrable-bose-gas)
        - [Quantum Hall Effect](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect)
          - [Fractional Quantum Hall Effect](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/fractional-quantum-hall-effect)
            - [Landau Levels](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/landau-levels)
              - [Lowest Landau level](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/lowest-landau-level)
                - [Filled LLL of Fermions](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/filled-lll-of-fermions)
            - [The Laughlin Wavefunction](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/the-laughlin-wavefunction)
            - [The Plasma Analogy](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/the-plasma-analogy)
            - [Fractional Charge](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/fractional-charge)
            - [Fractional Statistics](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/fractional-statistics)
          - [Appendix](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/quantum-hall-effect-appendix)
            - [Sampling from a complex wavefunction](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/sampling-from-a-complex-wavefunction)
        - [The Elastic Chain](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain)
          - [The Classical System](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/the-classical-system)
            - [Equations of Motion](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/equations-of-motion)
            - [Hamiltonian Formulation](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/hamiltonian-formulation)
            - [Complex Coordinates](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/complex-coordinates)
          - [Quantum Oscillators](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/quantum-oscillators)
            - [The Quantum Chain](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/the-quantum-chain)
            - [Oscillator Quanta are Bosons!](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/oscillator-quanta-are-bosons)
            - [Thermodynamic ($N \to \infty$) limit](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/thermodynamic-n-to-infty-limit)
            - [Finite Temperature](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/finite-temperature)
            - [Position Fluctuations](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/position-fluctuations)
            - [Density Fluctuations](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/density-fluctuations)
          - [Appendix](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/appendix)
            - [Fourier review](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/fourier-review)
            - [Discrete Fourier Transform](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/discrete-fourier-transform)
            - [Properties of the Fourier Transform](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/properties-of-the-fourier-transform)
            - [Higher dimensions](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/higher-dimensions)
            - [Evaluating (56)](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/evaluating-56)
      - [Course: Quantum Many-Body Physics in Condensed Matter by Luis Gregorio Dias (2020)](condensed-matter-physics.md#course-quantum-many-body-physics-in-condensed-matter-by-luis-gregorio-dias-2020)
- [Statistical physics](statistical-physics.md)
  - [Statistical mechanics](statistical-physics.md#statistical-mechanics)
    - [Kinetic theory of gases](statistical-physics.md#kinetic-theory-of-gases)
    - [Statistical mechanics model](statistical-physics.md#statistical-mechanics-model)
      - [Percolation](statistical-physics.md#percolation)
        - [Percolation theory](statistical-physics.md#percolation-theory)
  - [Sedimentation](statistical-physics.md#sedimentation)
  - [Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics](statistical-physics.md#maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics)
    - [Maxwell-Boltzmann distribution](statistical-physics.md#maxwell-boltzmann-distribution)
      - [Maxwell-Boltzmann statistics](statistical-physics.md#maxwell-boltzmann-statistics)
      - [Experimental verification of the Maxwell-Boltzmann distribution](statistical-physics.md#experimental-verification-of-the-maxwell-boltzmann-distribution)
        - [Zartman Ko experiment](statistical-physics.md#zartman-ko-experiment)
          - [Stern-Zartman experiment](statistical-physics.md#stern-zartman-experiment)
        - [Application of the Maxwell-Boltzmann distribution](statistical-physics.md#application-of-the-maxwell-boltzmann-distribution)
    - [Quantum statistics](statistical-physics.md#quantum-statistics)
      - [Bose-Einstein statistics](statistical-physics.md#bose-einstein-statistics)
      - [Fermi-Dirac statistics](statistical-physics.md#fermi-dirac-statistics)
        - [Quantum statistical mechanics](statistical-physics.md#quantum-statistical-mechanics)
  - [Thermodynamics](statistical-physics.md#thermodynamics)
    - [Boltzmann constant](statistical-physics.md#boltzmann-constant)
    - [Equipartition theorem](statistical-physics.md#equipartition-theorem)
    - [Thermodynamic potential](statistical-physics.md#thermodynamic-potential)
      - [Enthalpy](statistical-physics.md#enthalpy)
      - [Gibbs free energy](statistical-physics.md#gibbs-free-energy)
        - [Chemical equilibrium](statistical-physics.md#chemical-equilibrium)
        - [Reversible reaction](statistical-physics.md#reversible-reaction)
    - [Equation of state](statistical-physics.md#equation-of-state)
      - [Ideal gas law](statistical-physics.md#ideal-gas-law)
        - [Monatomic gas](statistical-physics.md#monatomic-gas)
    - [Entropy](statistical-physics.md#entropy)
      - [Clausius entropy](statistical-physics.md#clausius-entropy)
        - [Carnot cycle](statistical-physics.md#carnot-cycle)
      - [Second law of thermodynamics](statistical-physics.md#second-law-of-thermodynamics)
        - [Time reversibility](statistical-physics.md#time-reversibility)
          - [Arrow of time](statistical-physics.md#arrow-of-time)
          - [Time reversibility of classical mechanics](statistical-physics.md#time-reversibility-of-classical-mechanics)
          - [Time reversibility of gravity](statistical-physics.md#time-reversibility-of-gravity)
    - [Phase (matter)](statistical-physics.md#phase-matter)
      - [List of phase transitions](statistical-physics.md#list-of-phase-transitions)
        - [Evaporation](statistical-physics.md#evaporation)
        - [Sublimation](statistical-physics.md#sublimation)
      - [Phase transition](statistical-physics.md#phase-transition)
        - [Phase diagram](statistical-physics.md#phase-diagram)
          - [Type of phase diagram](statistical-physics.md#type-of-phase-diagram)
            - [Temperature-pressure phase diagram](statistical-physics.md#temperature-pressure-phase-diagram)
            - [Composition phase diagram](statistical-physics.md#composition-phase-diagram)
              - [Temperature-composition phase diagram](statistical-physics.md#temperature-composition-phase-diagram)
          - [Triple point](statistical-physics.md#triple-point)
          - [Critical point (thermodynamics)](statistical-physics.md#critical-point-thermodynamics)
        - [Second-order phase transition](statistical-physics.md#second-order-phase-transition)
    - [Refrigerator](statistical-physics.md#refrigerator)
      - [Dilution refrigerator](statistical-physics.md#dilution-refrigerator)
        - [Cryogen-free dilution refrigerator](statistical-physics.md#cryogen-free-dilution-refrigerator)
        - [Dilution refrigerator manufacturer](statistical-physics.md#dilution-refrigerator-manufacturer)
          - [Bluefors](statistical-physics.md#bluefors)
    - [Temperature](statistical-physics.md#temperature)
      - [Standard temperature and pressure](statistical-physics.md#standard-temperature-and-pressure)
      - [Scale of temperature](statistical-physics.md#scale-of-temperature)
        - [Kelvin](statistical-physics.md#kelvin)
      - [Thermometer](statistical-physics.md#thermometer)
        - [Mercury-in-glass thermometer](statistical-physics.md#mercury-in-glass-thermometer)
    - [Vacuum](statistical-physics.md#vacuum)
      - [Vacuum engineering](statistical-physics.md#vacuum-engineering)
        - [Vacuum vendor](statistical-physics.md#vacuum-vendor)
          - [Edwards Vacuum](statistical-physics.md#edwards-vacuum)
        - [Ultra-high vacuum](statistical-physics.md#ultra-high-vacuum)
- [Mechanics](mechanics.md)
  - [Angular momentum](mechanics.md#angular-momentum)
    - [Precession](mechanics.md#precession)
  - [Axle](mechanics.md#axle)
  - [Classical mechanics](mechanics.md#classical-mechanics)
    - [Classical physics](mechanics.md#classical-physics)
      - [Classical limit](mechanics.md#classical-limit)
        - [Correspondence principle](mechanics.md#correspondence-principle)
  - [Continuum mechanics](mechanics.md#continuum-mechanics)
    - [Continuity equation](mechanics.md#continuity-equation)
    - [Diffusion](mechanics.md#diffusion)
      - [Fick's laws of diffusion](mechanics.md#fick-s-laws-of-diffusion)
    - [Fluid mechanics](mechanics.md#fluid-mechanics)
      - [Fluid dynamics](mechanics.md#fluid-dynamics)
      - [Gravity wave](mechanics.md#gravity-wave)
      - [Navier-Stokes equations](mechanics.md#navier-stokes-equations)
        - [Navier-Stokes existence and smoothness](mechanics.md#navier-stokes-existence-and-smoothness)
  - [Lagrangian mechanics](mechanics.md#lagrangian-mechanics)
    - [Lagrangian mechanics lectures by Michel van Biezen (2017)](mechanics.md#lagrangian-mechanics-lectures-by-michel-van-biezen-2017)
    - [Action (physics)](mechanics.md#action-physics)
      - [Stationary action principle](mechanics.md#stationary-action-principle)
        - [Calculus of variations](mechanics.md#calculus-of-variations)
          - [Functional](mechanics.md#functional)
          - [Euler-Lagrange equation](mechanics.md#euler-lagrange-equation)
            - [Equations of motion](mechanics.md#equations-of-motion)
    - [Lagrangian](mechanics.md#lagrangian)
      - [Lagrangian (field theory)](mechanics.md#lagrangian-field-theory)
        - [Lagrangian density](mechanics.md#lagrangian-density)
      - [Generalized coordinate](mechanics.md#generalized-coordinate)
    - [Noether's theorem](mechanics.md#noether-s-theorem)
      - [Time invariance implies energy conservation](mechanics.md#time-invariance-implies-energy-conservation)
    - [Spontaneous symmetry breaking](mechanics.md#spontaneous-symmetry-breaking)
    - [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics)
      - [Lagrangian vs Hamiltonian](mechanics.md#lagrangian-vs-hamiltonian)
      - [Phase space coordinate](mechanics.md#phase-space-coordinate)
      - [Hamilton's equations](mechanics.md#hamilton-s-equations)
      - [Poisson bracket](mechanics.md#poisson-bracket)
    - [Equivalence between Lagrangian and Hamiltonian formalisms](mechanics.md#equivalence-between-lagrangian-and-hamiltonian-formalisms)
      - [Legendre transformation](mechanics.md#legendre-transformation)
  - [Mechanics problem](mechanics.md#mechanics-problem)
    - [Atwood machine](mechanics.md#atwood-machine)
      - [Compound Atwood machine](mechanics.md#compound-atwood-machine)
    - [Elastic collision](mechanics.md#elastic-collision)
    - [Harmonic oscillator](mechanics.md#harmonic-oscillator)
      - [Spring-mass system](mechanics.md#spring-mass-system)
      - [Coupled oscillators](mechanics.md#coupled-oscillators)
    - [Pendulum](mechanics.md#pendulum)
      - [Double pendulum](mechanics.md#double-pendulum)
      - [Spherical pendulum](mechanics.md#spherical-pendulum)
    - [Two-body problem](mechanics.md#two-body-problem)
    - [Continuous mechanics problem](mechanics.md#continuous-mechanics-problem)
      - [Mechanical resonance](mechanics.md#mechanical-resonance)
        - [Tuning fork](mechanics.md#tuning-fork)
  - [Mechanics vendor](mechanics.md#mechanics-vendor)
    - [Rolls-Royce](mechanics.md#rolls-royce)
  - [Newton's laws of motion](mechanics.md#newton-s-laws-of-motion)
    - [Force](mechanics.md#force)
      - [Torque](mechanics.md#torque)
    - [Mass](mechanics.md#mass)
  - [Point particle](mechanics.md#point-particle)
    - [Rigid body](mechanics.md#rigid-body)
      - [Rigid body dynamics](mechanics.md#rigid-body-dynamics)
        - [Rigid body dynamics simulator](mechanics.md#rigid-body-dynamics-simulator)
          - [Rigid body dynamics acceleration](mechanics.md#rigid-body-dynamics-acceleration)
        - [2D rigid body dynamics simulator](mechanics.md#2d-rigid-body-dynamics-simulator)
          - [Box2D](mechanics.md#box2d)
        - [3D rigid body dynamics](mechanics.md#3d-rigid-body-dynamics)
          - [3D rigid body dynamics simulator](mechanics.md#3d-rigid-body-dynamics-simulator)
            - [Bullet Physics](mechanics.md#bullet-physics)
              - [Bullet Physics parallel execution](mechanics.md#bullet-physics-parallel-execution)
              - [pyBullet](mechanics.md#pybullet)
              - [Erwin Coumans](mechanics.md#erwin-coumans)
            - [MuJoCo](mechanics.md#mujoco)
              - [MuJoCo getting started](mechanics.md#mujoco-getting-started)
              - [MJCF](mechanics.md#mjcf)
            - [PhysX](mechanics.md#physx)
          - [3D rigid body dynamics benchmark](mechanics.md#3d-rigid-body-dynamics-benchmark)
            - [SimBenchmark](mechanics.md#simbenchmark)
      - [Soft-body dynamics](mechanics.md#soft-body-dynamics)
- [Computational physics](#computational-physics)
  - [Computational chemistry](#computational-chemistry)
    - [Quantum chemistry](#quantum-chemistry)
      - [Relativistic quantum chemistry](#relativistic-quantum-chemistry)
      - [Quantum chemistry software](#quantum-chemistry-software)
        - [PySCF](#pyscf)
        - [Psi4](#psi4)
    - [Quantum computing computational chemistry algorithms](#quantum-computing-computational-chemistry-algorithms)
      - [IBM 2017 beryllium hydride ground state calculation on a quantum computer](#ibm-2017-beryllium-hydride-ground-state-calculation-on-a-quantum-computer)
- [Physics conference](#physics-conference)
  - [Solvay Conference](#solvay-conference)
    - [First Solvay Conference (1911)](#first-solvay-conference-1911)
    - [Fifth Solvay Conference (1927)](#fifth-solvay-conference-1927)
  - [Shelter Island Conference](#shelter-island-conference)
    - [Pocono conference](#pocono-conference)
- [Physicist](physicist.md)
  - [Abraham Pais](physicist.md#abraham-pais)
    - [Book by Abraham Pais](physicist.md#book-by-abraham-pais)
  - [Alain Aspect](physicist.md#alain-aspect)
  - [Albert Einstein](physicist.md#albert-einstein)
    - [Annus Mirabilis papers](physicist.md#annus-mirabilis-papers)
      - [Investigations on the theory of the Brownian movement by Einstein (1905)](physicist.md#investigations-on-the-theory-of-the-brownian-movement-by-einstein-1905)
      - [On a Heuristic Viewpoint Concerning the Production and Transformation of Light by Einstein (1905)](physicist.md#on-a-heuristic-viewpoint-concerning-the-production-and-transformation-of-light-by-einstein-1905)
    - [Work about Einstein](physicist.md#work-about-einstein)
      - [Subtle is the Lord by Abraham Pais (1982)](physicist.md#subtle-is-the-lord-by-abraham-pais-1982)
  - [André-Marie Ampère](physicist.md#andre-marie-ampere)
    - [Education of André-Marie Ampère](physicist.md#education-of-andre-marie-ampere)
  - [Augustin-Jean Fresnel](physicist.md#augustin-jean-fresnel)
  - [Barton Zwiebach](physicist.md#barton-zwiebach)
  - [Brian Josephson](physicist.md#brian-josephson)
    - [Paper by Brian Josephson](physicist.md#paper-by-brian-josephson)
  - [Carl David Anderson](physicist.md#carl-david-anderson)
  - [Carl Sagan](physicist.md#carl-sagan)
    - [Work by Carl Sagan](physicist.md#work-by-carl-sagan)
    - [We Are Made of Star-Stuff](physicist.md#we-are-made-of-star-stuff)
  - [David Tong](physicist.md#david-tong)
  - [Edward Witten](physicist.md#edward-witten)
  - [Edward Teller](physicist.md#edward-teller)
  - [Enrico Fermi](physicist.md#enrico-fermi)
    - [Alberto Fermi](physicist.md#alberto-fermi)
    - [Adolfo Amidei](physicist.md#adolfo-amidei)
    - [Work about Enrico Fermi](physicist.md#work-about-enrico-fermi)
      - [Enrico Fermi: physicist by Emilio Segrè (1970)](physicist.md#enrico-fermi-physicist-by-emilio-segre-1970)
      - [The World Of Enrico Fermi by Harvard Project Physics (1970)](physicist.md#the-world-of-enrico-fermi-by-harvard-project-physics-1970)
  - [Ernest Lawrence](physicist.md#ernest-lawrence)
  - [Ernest Rutherford](physicist.md#ernest-rutherford)
  - [Erwin Schrödinger](physicist.md#erwin-schrodinger)
    - [Work by Erwin Schrödinger](physicist.md#work-by-erwin-schrodinger)
      - [What is life?](physicist.md#what-is-life)
      - [Paper by Erwin Schrödinger](physicist.md#paper-by-erwin-schrodinger)
        - [Quantization as an Eigenvalue Problem](physicist.md#quantization-as-an-eigenvalue-problem)
          - [Collected Papers On Wave Mechanics by Deans (1928)](physicist.md#collected-papers-on-wave-mechanics-by-deans-1928)
  - [Ettore Majorana](physicist.md#ettore-majorana)
    - [Majorana fermion](physicist.md#majorana-fermion)
  - [Freeman Dyson](physicist.md#freeman-dyson)
    - [Work by Freeman Dyson](physicist.md#work-by-freeman-dyson)
    - [Freeman Dyson Web of Stories interview (1998)](physicist.md#freeman-dyson-web-of-stories-interview-1998)
  - [Galileo Galilei](physicist.md#galileo-galilei)
  - [Hans Bethe](physicist.md#hans-bethe)
  - [Heinrich Hertz](physicist.md#heinrich-hertz)
  - [Henri Becquerel](physicist.md#henri-becquerel)
    - [Becquerel's rays](physicist.md#becquerel-s-rays)
  - [Hermann Weyl](physicist.md#hermann-weyl)
    - [Publication by Hermann Weyl](physicist.md#publication-by-hermann-weyl)
      - [Gravity and electricity by Hermann Weyl (1918)](physicist.md#gravity-and-electricity-by-hermann-weyl-1918)
  - [Isaac Newton](physicist.md#isaac-newton)
    - [Philosophiæ Naturalis Principia Mathematica](physicist.md#philosophiae-naturalis-principia-mathematica)
  - [Leo Szilard](physicist.md#leo-szilard)
  - [Isidor Isaac Rabi](physicist.md#isidor-isaac-rabi)
    - [Work by Isidor Rabi](physicist.md#work-by-isidor-rabi)
      - [A New Method of Measuring Nuclear Magnetic Moment](physicist.md#a-new-method-of-measuring-nuclear-magnetic-moment)
      - [The Molecular Beam Resonance Method for Measuring Nuclear Magnetic Moments](physicist.md#the-molecular-beam-resonance-method-for-measuring-nuclear-magnetic-moments)
  - [Jakob Schwichtenberg](physicist.md#jakob-schwichtenberg)
    - [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015)
    - [Physics Travel Guide](physicist.md#physics-travel-guide)
  - [James Clerk Maxwell](physicist.md#james-clerk-maxwell)
  - [Jean Baptiste Perrin](physicist.md#jean-baptiste-perrin)
    - [Work by Jean Perrin](physicist.md#work-by-jean-perrin)
  - [J. J. Thomson](physicist.md#j-j-thomson)
  - [John Archibald Wheeler](physicist.md#john-archibald-wheeler)
  - [John Bardeen](physicist.md#john-bardeen)
    - [True Genius: The Life and Science of John Bardeen](physicist.md#true-genius-the-life-and-science-of-john-bardeen)
  - [John C. Baez](physicist.md#john-c-baez)
  - [John von Neumann](physicist.md#john-von-neumann)
  - [John Rowell](physicist.md#john-rowell)
  - [Julian Schwinger](physicist.md#julian-schwinger)
  - [Karl Guthe Jansky](physicist.md#karl-guthe-jansky)
  - [Leonard Susskind](physicist.md#leonard-susskind)
    - [Lecture by Leonard Susskind](physicist.md#lecture-by-leonard-susskind)
  - [Louis de Broglie](physicist.md#louis-de-broglie)
  - [Lord Kelvin](physicist.md#lord-kelvin)
    - [Nineteen Century Clouds by Lord Kelvin (1901)](physicist.md#nineteen-century-clouds-by-lord-kelvin-1901)
  - [Luboš Motl](physicist.md#lubos-motl)
    - [Feud between Sabine Hossenfelder and Luboš Motl](physicist.md#feud-between-sabine-hossenfelder-and-lubos-motl)
  - [Ludwig Boltzmann](physicist.md#ludwig-boltzmann)
  - [Marie Curie](physicist.md#marie-curie)
    - [Find the most interesting research topic that no one is researching](physicist.md#find-the-most-interesting-research-topic-that-no-one-is-researching)
    - [Pierre Curie](physicist.md#pierre-curie)
    - [Publication by Marie Curie](physicist.md#publication-by-marie-curie)
      - [On a new radioactive substance contained in pitchblende](physicist.md#on-a-new-radioactive-substance-contained-in-pitchblende)
      - [On a new, strongly radioactive substance contained in pitchblende](physicist.md#on-a-new-strongly-radioactive-substance-contained-in-pitchblende)
  - [Michio Kaku](physicist.md#michio-kaku)
  - [Murray Gell-Mann](physicist.md#murray-gell-mann)
  - [Max Planck](physicist.md#max-planck)
    - [Work by Max Planck](physicist.md#work-by-max-planck)
      - [Scientific autobiography by Max Planck (1948)](physicist.md#scientific-autobiography-by-max-planck-1948)
        - [Scientific Autobiography and Other Papers by Max Planck translated by Frank Gaynor (1949)](physicist.md#scientific-autobiography-and-other-papers-by-max-planck-translated-by-frank-gaynor-1949)
          - [Scientific Autobiography by Max Planck translated by Frank Gaynor (1949)](physicist.md#scientific-autobiography-by-max-planck-translated-by-frank-gaynor-1949)
      - [Paper by Max Planck](physicist.md#paper-by-max-planck)
        - [On the Law of Distribution of Energy in the Normal Spectrum](physicist.md#on-the-law-of-distribution-of-energy-in-the-normal-spectrum)
  - [Max von Laue](physicist.md#max-von-laue)
  - [Michael Faraday](physicist.md#michael-faraday)
  - [Niels Bohr](physicist.md#niels-bohr)
  - [Pascual Jordan](physicist.md#pascual-jordan)
  - [Paul Dirac](physicist.md#paul-dirac)
  - [Philip W. Anderson](physicist.md#philip-w-anderson)
  - [Pieter Zeeman](physicist.md#pieter-zeeman)
  - [Polykarp Kusch](physicist.md#polykarp-kusch)
  - [Richard Feynman](richard-feynman.md)
    - [Personal life of Richard Feynman](richard-feynman.md#personal-life-of-richard-feynman)
      - [Arline Greenbaum](arline-greenbaum.md)
      - [Infinity (1996 film)](infinity-1996-film.md)
      - [Feynman was a huge womanizer during a certain period of his life](feynman-was-a-huge-womanizer-during-a-certain-period-of-his-life.md)
      - [Joan Feynman](joan-feynman.md)
      - [Richard Feynman's drug use](richard-feynman-s-drug-use.md)
    - [Richard Feynman's first seminar in 1941](richard-feynman-s-first-seminar-in-1941.md)
    - [Quote by Richard Feynman](quote-by-richard-feynman.md)
      - [What I cannot create, I do not understand](what-i-cannot-create-i-do-not-understand.md)
    - [Work by Richard Feynman](work-by-richard-feynman.md)
      - [Space-Time Approach to Quantum Electrodynamic by Richard Feynman (1949)](space-time-approach-to-quantum-electrodynamic-by-richard-feynman-1949.md)
    - [Works about Richard Feynman](works-about-richard-feynman.md)
      - [Genius: Richard Feynman and Modern Physics by James Gleick (1994)](genius-richard-feynman-and-modern-physics-by-james-gleick-1994.md)
      - [Los Alamos From Below by Richard Feynman (1975)](los-alamos-from-below-by-richard-feynman-1975.md)
      - [Surely You're Joking, Mr. Feynman](surely-you-re-joking-mr-feynman.md)
        - [Surely You're Joking, Mr. Feynman chapter O Americano, Outra Vez!](surely-you-re-joking-mr-feynman-chapter-o-americano-outra-vez.md)
        - [Surely You're Joking, Mr. Feynman chapter Alfred Nobel's Other Mistake](surely-you-re-joking-mr-feynman-chapter-alfred-nobel-s-other-mistake.md)
          - [Rich people who create charitable prizes are often crooked](rich-people-who-create-charitable-prizes-are-often-crooked.md)
  - [Sean M. Carroll](physicist.md#sean-m-carroll)
    - [The Purpose of Harvard is Not to Educate People by Sean Carroll (2008)](physicist.md#the-purpose-of-harvard-is-not-to-educate-people-by-sean-carroll-2008)
    - [How To Get Tenure at a Major Research University by Sean Carroll (2011)](physicist.md#how-to-get-tenure-at-a-major-research-university-by-sean-carroll-2011)
  - [Stephen Hawking](physicist.md#stephen-hawking)
  - [Steven H. Simon](physicist.md#steven-h-simon)
  - [Sylvain Poirier](physicist.md#sylvain-poirier)
    - [settheory.net](physicist.md#settheory-net)
  - [Tobias J. Osborne](physicist.md#tobias-j-osborne)
  - [Victor Francis Hess](physicist.md#victor-francis-hess)
  - [Walter Houser Brattain](physicist.md#walter-houser-brattain)
  - [Werner Heisenberg](physicist.md#werner-heisenberg)
    - [Paper by Werner Heisenberg](physicist.md#paper-by-werner-heisenberg)
  - [William Shockley](physicist.md#william-shockley)
  - [Willis Lamb](physicist.md#willis-lamb)
  - [Wolfgang Pauli](physicist.md#wolfgang-pauli)
- [Physics gossip](#physics-gossip)
- [Unsolved physics problem](#unsolved-physics-problem)
- [Physics bibliography](#physics-bibliography)
  - [Theoretical Physics Reference by Ondrej Certík](#theoretical-physics-reference-by-ondrej-certik)
  - [Physics YouTube channel](#physics-youtube-channel)
    - [Faculty of Khan](#faculty-of-khan)
    - [Looking Glass Universe](#looking-glass-universe)
    - [Ludic Science](#ludic-science)
    - [minutephysics](#minutephysics)
    - [Physics Explained](#physics-explained)
    - [ScienceClic](#scienceclic)
    - [Steve Mould](#steve-mould)
    - [The Science Asylum](#the-science-asylum)
      - [Nick Lucid](#nick-lucid)
    - [UCSB Physics Lecture Demonstrations](#ucsb-physics-lecture-demonstrations)
    - [UNSW Physics YouTube channel](#unsw-physics-youtube-channel)
    - [Veritasium](#veritasium)
  - [Physics journal](#physics-journal)
    - [Physics Letters](#physics-letters)
      - [Physics Letters A](#physics-letters-a)
      - [Physics Letters B](#physics-letters-b)
    - [Journal by the American Physical Society](#journal-by-the-american-physical-society)
      - [Physical Review](#physical-review)
        - [Paper published on Physical Review ](#paper-published-on-physical-review)
      - [Physical Review Letters](#physical-review-letters)
        - [Physical Review Letters article](#physical-review-letters-article)

## How to teach and learn physics

↑ **Parent:** [Physics](physics.md)  
🏷️ **Tags:** [Essays by Ciro Santilli](ciro-santilli.md#essays-by-ciro-santilli)

The approach many courses take to physics, specially "modern Physics" is really bad, this is how it should be taught:
- start by describing experiments that the previous best theory did not explain, see also: [Section "Physics education needs more focus on understanding experiments and their history"](#physics-education-needs-more-focus-on-understanding-experiments-and-their-history)
- then, give the final formula for the next best theory
- then, give all the important final implications of that formula, and how it amazingly describes the experiments. In particular this means: [doing physics means calculating a number](#doing-physics-means-calculating-a-number)
- then, give some mathematical intuition on the formulas, and how the main equation could have been derived
- finally, then and only then, start deriving the outcomes of the main formula in detail

This is likely because at some point, experiments get more and more complicated, and so people are tempted to say "this is the truth" instead of "this is why we think this is the truth", which is much harder.

But we can't be lazy, there is no replacement to the why.

Related:
- [http://settheory.net/learnphysics](http://settheory.net/learnphysics) and [https://www.youtube.com/watch?v=5MKjPYuD60I&list=PLJcTRymdlUQPwx8qU4ln83huPx-6Y3XxH](https://www.youtube.com/watch?v=5MKjPYuD60I&list=PLJcTRymdlUQPwx8qU4ln83huPx-6Y3XxH) from [settheory.net](physicist.md#settheory-net)
- [https://math.ucr.edu/home/baez/books.html](https://math.ucr.edu/home/baez/books.html) by [John Baez](physicist.md#john-c-baez). Mentions:> This webpage doesn't have lots of links to websites. Websites just don't have the sort of in-depth material you need to learn technical subjects like advanced math and physics — at least, not yet. To learn this stuff, you need to read lots of books

  [Ciro Santilli](ciro-santilli.md) is trying to change that: [OurBigBook.com](ourbigbook-com.md).
- [https://web.archive.org/web/20210324182549/http://jakobschwichtenberg.com/one-thing/](https://web.archive.org/web/20210324182549/http://jakobschwichtenberg.com/one-thing/) by [Jakob Schwichtenberg](physicist.md#jakob-schwichtenberg)

### Physics education needs more focus on understanding experiments and their history

↑ **Parent:** [How to teach and learn physics](#how-to-teach-and-learn-physics)  
🏷️ **Tags:** [Cirism](cirism.md)

This is the only way to truly understand and appreciate the subject.

Understanding the experiments gets intimately entangled with basically learning the [history of physics](#history-of-physics), which is extremely beneficial as also highlighted by [Ron Maimon](stack-overflow.md#ron-maimon), related: [there is value in tutorials written by early pioneers of the field](#there-is-value-in-tutorials-written-by-early-pioneers-of-the-field).

"How we know" is a basically more fundamental point than "what we know" in the natural sciences.

In the [Surely You're Joking, Mr. Feynman chapter O Americano, Outra Vez!](surely-you-re-joking-mr-feynman-chapter-o-americano-outra-vez.md) [Richard Feynman](richard-feynman.md) describes his experience teaching in [Brazil](brazil.md) in the early 1950s, and how everything was memorized, without any explanation of the experiments or that the theory has some relationship to the real world!

Although things have improved considerably since in Brazil, Ciro still feels that some areas of physics are still taught without enough experiments described upfront. Notably, ironically, [quantum field theory](quantum-field-theory.md), which is where Feynman himself worked.

Feynman gave huge importance to understanding and explaining experiments, as can also be seen on [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](quantum-field-theory.md#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979).

<a id="video-making-the-best-way-of-learning-science-and-technology-by-manish-jain-2018"></a>
**[Video 1](#video-making-the-best-way-of-learning-science-and-technology-by-manish-jain-2018). 'Making' - the best way of learning science and technology by Manish Jain (2018)** [Source](https://www.youtube.com/watch?v=EpTFQcD7bME).

#### There is value in tutorials written by early pioneers of the field

↑ **Parent:** [Physics education needs more focus on understanding experiments and their history](#physics-education-needs-more-focus-on-understanding-experiments-and-their-history)  
🏷️ **Tags:** [Cirism](cirism.md)

Everyone is beginner when the field is new, and [there is value in tutorials written by beginners](cirism.md#there-is-value-in-tutorials-written-by-beginners).

For example, [Ciro Santilli](ciro-santilli.md) felt it shocking how direct and satisfying [Richard Feynman](richard-feynman.md)'s [scientific vulgarization](science.md#popular-science) of [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics) were, e.g. at: [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](quantum-field-theory.md#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979), and that if he had just assumed minimal knowledge of [mathematics](mathematics.md), he was about to give a full satisfactory picture in just a few hours.

Other supporters of this:
- [Ron Maimon](stack-overflow.md#ron-maimon): the same also applies to early original papers of the field, not just tutorials
- [Dean Kamen](technology.md#dean-kamen): quick mention at: [https://fi.edu/en/awards/laureates/dean-kamen](https://fi.edu/en/awards/laureates/dean-kamen), but a better longer mention on Dreamer (2020), nearby section from trailer: [https://youtu.be/Cj2VKVJKf1I?t=16](https://youtu.be/Cj2VKVJKf1I?t=16)

### Doing physics means calculating a number

↑ **Parent:** [How to teach and learn physics](#how-to-teach-and-learn-physics)  
🏷️ **Tags:** [Cirism](cirism.md)

In Physics, in order to test a theory, you must be able to extract a number from it.

It does not matter how, if it is exact, or numerical, or a message from [God](religion.md#god): a number has to come out of the formulas in the end, and you have to compare it with the experimental data.

Many theoretical physicists seem to forget this in their lectures, see also: [Section "How to teach and learn physics"](#how-to-teach-and-learn-physics).

#### Physics is a way to predict the future

↑ **Parent:** [Doing physics means calculating a number](#doing-physics-means-calculating-a-number)

It is quite beautiful to look at it like that.

That which previous generations would treat as magical, and divine.

We are doing better and better right now.

Of course, in a way, humans are trying and often successfully predicting certain daily aspects of the future all the time. Will this car stop if I cross the road? Will this glass break if I drop it?

But there's a beauty to the level of precision that can be achieved with [physics](physics.md) and other [natural sciences](science.md#natural-science).

### It is OK to treat things as black boxes

↑ **Parent:** [How to teach and learn physics](#how-to-teach-and-learn-physics)

Nature [is a black box, right](technology.md#science-is-the-reverse-engineering-of-nature)?

You don't need to understand the [from first principles](science.md#from-first-principles) derivation of every single phenomena.

And most important of all: you should not start learning phenomena by reading the from first principles derivation.

Instead, you should see what happens in experiments, and how matches some known formula (which hopefully has been derived from first principles).

Only open the boxes (understand from first principles derivation) if the need is felt!

E.g.:
- you don't need to understand everything about why [SQUID devices](condensed-matter-physics.md#squid-device) have their specific [I-V curve](electronics.md#current-voltage-characteristic) curve. You have to first of all learn what the I-V curve would be in an experiment!
- you don't need to understand the fine details of how [cavity magnetrons](photon.md#cavity-magnetron) work. What you need to understand first is what kind of [microwave](photon.md#microwave) you get from what kind of input ([DC current](electronics.md#direct-current)), and how that compares to other sources of [microwaves](photon.md#microwave)
- [lasers](condensed-matter-physics.md#laser): same

Physics is [all about predicting the future](#doing-physics-means-calculating-a-number). If you can predict the future with an end result, that's already predicting the future, and valid.

## The most important physics experiments

↑ **Parent:** [Physics](physics.md)

Videos should be found/made for all of those: [videos of all key physics experiments](todo.md#videos-of-all-key-physics-experiments)

- [speed of light experiment](photon.md#speed-of-light-experiment)
- basically all experiments listed under [Section "Quantum mechanics experiment"](quantum-mechanics.md#quantum-mechanics-experiment) such as:
  - [black-body radiation experiment](condensed-matter-physics.md#black-body-radiation-experiment)
- [Davisson-Germer experiment](quantum-mechanics.md#davisson-germer-experiment)

### Physics experiment without a decent modern video

↑ **Parent:** [The most important physics experiments](#the-most-important-physics-experiments)

### Aharonov-Bohm effect

↑ **Parent:** [The most important physics experiments](#the-most-important-physics-experiments)

This shows that viewing [electromagnetism](electromagnetism.md) as [gauge theory](quantum-field-theory.md#gauge-theory) does have experimentally observable consequences. TODO understand what that means.

In more understandable terms, it shows that the [magnetic vector potential](electromagnetism.md#magnetic-vector-potential) matters where the magnetic field is 0.

<a id="video-the-quantum-experiment-that-almost-broke-locality-by-the-science-asylum-2019"></a>
**[Video 2](#video-the-quantum-experiment-that-almost-broke-locality-by-the-science-asylum-2019). The Quantum Experiment that ALMOST broke Locality by The Science Asylum (2019)** [Source](https://www.youtube.com/watch?v=a70Bmkza7XA).

### Compton scattering

↑ **Parent:** [The most important physics experiments](#the-most-important-physics-experiments)  
🏷️ **Tags:** [1927 Nobel Prize in Physics](nobel-prize.md#1927-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Compton_scattering)

Classic theory predicts that the output frequency must be the same as the input one since the electromagnetic wave makes the electron vibrate with same frequency as itself, which then irradiates further waves.

But the output waves are longer because [photons are discrete and energy is proportional to frequency](quantum-mechanics.md#planck-einstein-relation):

The formula is exactly that of two [relativistic](relativity.md) billiard balls colliding.

Therefore this is evidence that [photons](photon.md) exist and have momentum.

<a id="video-compton-scattering-by-compton-scattering-2017"></a>
**[Video 3](#video-compton-scattering-by-compton-scattering-2017). Compton Scattering by Compton Scattering (2017)** [Source](http://youtube.com/watch?v=uICnnfYHYJ4). Experiment with a [caesium-137](chemistry.md#caesium-137) source.

<a id="video-l3-3-compton-scattering-by-barton-zwiebach-2017"></a>
**[Video 4](#video-l3-3-compton-scattering-by-barton-zwiebach-2017). L3.3 Compton Scattering by Barton Zwiebach (2017)** [Source](http://youtube.com/watch?v=WR88_Vzfcx4).

### Photoelectric effect

↑ **Parent:** [The most important physics experiments](#the-most-important-physics-experiments)  
🏷️ **Tags:** [1921 Nobel Prize in Physics](nobel-prize.md#1921-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Photoelectric_effect)

No matter how hight the wave intensity, if it the frequency is small, no photons are removed from the material.

This is different from classic waves where energy is proportional to intensity, and coherent with the [existence of photons](photon.md) and the [Planck-Einstein relation](quantum-mechanics.md#planck-einstein-relation).

<a id="video-photoelectric-effect-by-ucsb-physics-lecture-demonstrations-2021"></a>
**[Video 5](#video-photoelectric-effect-by-ucsb-physics-lecture-demonstrations-2021). Photoelectric effect by UCSB Physics Lecture Demonstrations (2021)** [Source](https://www.youtube.com/watch?v=22RSoYpazao&amp;list=PLGImELmE_zlPqmRbbvZ1MjWnbFovcwBBO&amp;index=96).

## System of units

↑ **Parent:** [Physics](physics.md)

[This section is present in another page, follow this link to view it.](system-of-units.md)

## Particle physics

↑ **Parent:** [Physics](physics.md)

[This section is present in another page, follow this link to view it.](particle-physics.md)

## Energy

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Energy)

### Unit of measurement for energy

↑ **Parent:** [Energy](#energy)  
🏷️ **Tags:** [Unit of measurement](system-of-units.md#unit-of-measurement)

#### Joule

↑ **Parent:** [Unit of measurement for energy](#unit-of-measurement-for-energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Joule)

#### Watt

↑ **Parent:** [Unit of measurement for energy](#unit-of-measurement-for-energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Watt)

### Conservation of energy

↑ **Parent:** [Energy](#energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Conservation_of_energy)

### Potential energy

↑ **Parent:** [Energy](#energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Potential_energy)

#### Potential barrier

↑ **Parent:** [Potential energy](#potential-energy)

### Kinetic energy

↑ **Parent:** [Energy](#energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kinetic_energy)

<h4 id="why-kinetic-energy-is-mv-2-2">Why kinetic energy is <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1.0641em;vertical-align:-0.25em;"></span><span class="mord mathnormal">m</span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03588em;">v</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span><span class="mord">/2</span></span></span></span>?</h4>

↑ **Parent:** [Kinetic energy](#kinetic-energy)

- why the square: [https://physics.stackexchange.com/questions/535/why-does-kinetic-energy-increase-quadratically-not-linearly-with-speed](https://physics.stackexchange.com/questions/535/why-does-kinetic-energy-increase-quadratically-not-linearly-with-speed) on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange). [Ron Maimon](stack-overflow.md#ron-maimon)'s answer is great, as it relies only on the following staring points:
  - [energy is conserved](#conservation-of-energy)
  - [Galilean invariance](geometry.md#galilean-invariance)

  He also offers a [symmetry](group.md#symmetry) argument considering the case of [potential energy](#potential-energy).
- why the half: [https://physics.stackexchange.com/questions/27847/why-is-there-a-frac-1-2-in-frac-1-2-mv2](https://physics.stackexchange.com/questions/27847/why-is-there-a-frac-1-2-in-frac-1-2-mv2) on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange)

Others:
- [https://physics.stackexchange.com/questions/156696/why-is-kinetic-energy-defined-as-1-2m-v2](https://physics.stackexchange.com/questions/156696/why-is-kinetic-energy-defined-as-1-2m-v2)

### Work (physics)

↑ **Parent:** [Energy](#energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Work_(physics))

#### Why work is force times distance?

↑ **Parent:** [Work (physics)](#work-physics)

- [https://physics.stackexchange.com/questions/26797/why-does-work-equal-force-times-distance](https://physics.stackexchange.com/questions/26797/why-does-work-equal-force-times-distance)
- [https://www.quora.com/Why-do-we-define-work-as-force-times-distance](https://www.quora.com/Why-do-we-define-work-as-force-times-distance)
- [https://physics.stackexchange.com/questions/428525/why-does-work-depend-on-distance](https://physics.stackexchange.com/questions/428525/why-does-work-depend-on-distance)
- [https://physics.stackexchange.com/questions/79523/why-does-the-amount-of-energy-transferred-depend-on-distance-rather-than-time](https://physics.stackexchange.com/questions/79523/why-does-the-amount-of-energy-transferred-depend-on-distance-rather-than-time)

## Experimental physics

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Experimental_physics)

Experiment and theory are like the [yin and yang](religion.md#yin-and-yang): opposites, but one cannot exist without the other.

### Theoretical physics

↑ **Parent:** [Experimental physics](#experimental-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Theoretical_physics)

## Field (physics)

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Field_(physics))

[Quantum Field Theory lecture notes by David Tong (2007)](quantum-field-theory.md#quantum-field-theory-lecture-notes-by-david-tong-2007) puts it well:

> In classical physics, the primary reason for introducing the concept of the [field](#field-physics) is to construct laws of Nature that are local. The old laws of Coulomb and Newton involve "action at a distance". This means that the force felt by an electron (or planet) changes immediately if a distant [proton](standard-model.md#proton) (or star) moves. This situation is philosophically unsatisfactory. More importantly, it is also experimentally wrong. The field theories of Maxwell and Einstein remedy the situation, with all interactions mediated in a local fashion by the field.

This is also mentioned e.g. at [Video 2. "The Quantum Experiment that ALMOST broke Locality by The Science Asylum (2019)"](#video-the-quantum-experiment-that-almost-broke-locality-by-the-science-asylum-2019).

### Principle of locality

↑ **Parent:** [Field (physics)](#field-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Principle_of_locality)

#### Causality

↑ **Parent:** [Principle of locality](#principle-of-locality)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Causality)

- [https://en.wikipedia.org/wiki/Causality](https://en.wikipedia.org/wiki/Causality)
- [https://en.wikipedia.org/wiki/Causality_(physics)](https://en.wikipedia.org/wiki/Causality_(physics))

##### Causality in quantum mechanics

↑ **Parent:** [Causality](#causality)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Causality_in_quantum_mechanics)

In simple terms, if you believe in the [Schrödinger equation](quantum-mechanics.md#schrodinger-equation) and its modern probabilistic interpretation as described in the [Schrödinger picture](quantum-mechanics.md#schrodinger-picture), then at first it seem that there is no strict causality to the outcome of experiments.

People have then tried to recover that by assuming that there is some inner sate beyond the [Schrödinger equation](quantum-mechanics.md#schrodinger-equation), but these ideas are refuted by [Bell test experiments](quantum-mechanics.md#bell-test-experiment), unless we give up the [principle of locality](#principle-of-locality), which feels more important, especially in [special relativity](relativity.md#special-relativity), where [faster-than-light implies time travel](photon.md#faster-than-light-implies-time-travel), which breaks causality even more dramatically.

The [de Broglie-Bohm theory](quantum-mechanics.md#de-broglie-bohm-theory) is a deterministic but [non-local](#principle-of-locality) formulation of quantum mechanics.

###### Causality and quantum jumps are incompatible

↑ **Parent:** [Causality in quantum mechanics](#causality-in-quantum-mechanics)

If something does a [quantum jump](chemistry.md#quantum-jump), what causes it to decide doing so at a particular time and not another? It is expected that a continuous cause would have continuous effects.

This concern was raised immediately by [Rutherford](physicist.md#ernest-rutherford) while reviewing the [Bohr model](chemistry.md#bohr-model) in 1913 as mentioned in [The Quantum Story by Jim Baggott (2011)](quantum-mechanics.md#the-quantum-story-by-jim-baggott-2011) page 32.

## Law of physics

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scientific_law#Laws_of_physics)

## History of physics

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/History_of_physics)

Good reading list: [Abraham Pais Prize for History of Physics](#abraham-pais-prize-for-history-of-physics).

### Abraham Pais Prize for History of Physics

↑ **Parent:** [History of physics](#history-of-physics)  
🏷️ **Tags:** [Prize](social-technology.md#prize)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Abraham_Pais_Prize_for_History_of_Physics)

## Condensed matter physics

↑ **Parent:** [Physics](physics.md)

[This section is present in another page, follow this link to view it.](condensed-matter-physics.md)

## Statistical physics

↑ **Parent:** [Physics](physics.md)

[This section is present in another page, follow this link to view it.](statistical-physics.md)

## Mechanics

↑ **Parent:** [Physics](physics.md)

[This section is present in another page, follow this link to view it.](mechanics.md)

## Computational physics

↑ **Parent:** [Physics](physics.md)  
🏷️ **Tags:** [Computer simulation](software.md#computer-simulation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computational_physics)

The intersection of two beautiful [arts](art.md): [coding](computer.md) and [physics](physics.md)!

Computational physics is a good way to get valuable intuition about the key equations of physics, and train your [numerical analysis](mathematics.md#numerical-analysis) skills:
- classical mechanics
  - "Real-time [heat equation](calculus.md#heat-equation) OpenGL visualization with interactive mouse cursor using relaxation method" under [the best articles by Ciro Articles](articles.md)
- [https://phet.colorado.edu](https://phet.colorado.edu) PhET simulations from University of Colorado Boulder

Other child sections:
- [Schrödinger equation simulations](quantum-mechanics.md#computational-quantum-mechanics)
- [quantum field theory simulations](quantum-field-theory.md#quantum-field-theory-simulations)

### Computational chemistry

↑ **Parent:** [Computational physics](#computational-physics)  
🏷️ **Tags:** [Computer simulation](software.md#computer-simulation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computational_chemistry)

#### Quantum chemistry

↑ **Parent:** [Computational chemistry](#computational-chemistry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_chemistry)

Ah, the jewel of [computational physics](#computational-physics).

Also known as an [ab initio](https://en.wikipedia.org/wiki/Ab_initio_quantum_chemistry_methods) method: no experimental measurement is taken as input, [QED is all you need](quantum-field-theory.md#quantum-electrodynamics).

But since QED is thought to fully describe all relevant aspects [molecules](quantum-mechanics.md#molecule), it could be called "the" ab initio method.

For one, if we were able to predict protein molecule interactions, our understanding of [molecular biology technologies](ciro-santilli.md#molecular-biology-technologies) would be solved.

No more ultra expensive and complicated [X-ray crystallography](microscopy.md#x-ray-crystallography) or [cryogenic electron microscopy](microscopy.md#cryogenic-electron-microscopy).

And the fact that [quantum computers](quantum-computing.md) are one of the most promising advances to this field, is also very very exciting: [Section "Quantum algorithm"](quantum-computing.md#quantum-algorithm).

##### Relativistic quantum chemistry

↑ **Parent:** [Quantum chemistry](#quantum-chemistry)  
🏷️ **Tags:** [Applications of quantum electrodynamics](quantum-field-theory.md#applications-of-quantum-electrodynamics)

- [https://www.youtube.com/watch?v=NtnsHtYYKf0](https://www.youtube.com/watch?v=NtnsHtYYKf0) "Mercury and Relativity - Periodic Table of Videos" by a

##### Quantum chemistry software

↑ **Parent:** [Quantum chemistry](#quantum-chemistry)

###### PySCF

↑ **Parent:** [Quantum chemistry software](#quantum-chemistry-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PySCF)

[https://github.com/pyscf/pyscf](https://github.com/pyscf/pyscf)

###### Psi4

↑ **Parent:** [Quantum chemistry software](#quantum-chemistry-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PSI_(computational_chemistry))

[https://github.com/psi4/psi4](https://github.com/psi4/psi4)

#### Quantum computing computational chemistry algorithms

↑ **Parent:** [Computational chemistry](#computational-chemistry)

##### IBM 2017 beryllium hydride ground state calculation on a quantum computer

↑ **Parent:** [Quantum computing computational chemistry algorithms](#quantum-computing-computational-chemistry-algorithms)

TODO what's the largest molecule done on a [classical computer](quantum-computing.md#classical-computer)?

- [https://www.ibm.com/blogs/research/2017/09/quantum-molecule/](https://www.ibm.com/blogs/research/2017/09/quantum-molecule/)
- [https://www.nature.com/articles/nature23879](https://www.nature.com/articles/nature23879) "Hardware-efficient variational quantum eigensolver for small molecules and quantum magnets"
- [https://www.sciencemag.org/news/2017/09/quantum-computer-simulates-largest-molecule-yet-sparking-hope-future-drug-discoveries](https://www.sciencemag.org/news/2017/09/quantum-computer-simulates-largest-molecule-yet-sparking-hope-future-drug-discoveries)

## Physics conference

↑ **Parent:** [Physics](physics.md)

### Solvay Conference

↑ **Parent:** [Physics conference](#physics-conference)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solvay_Conference)

#### First Solvay Conference (1911)

↑ **Parent:** [Solvay Conference](#solvay-conference)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/First_Solvay_Conference_(1911))

#### Fifth Solvay Conference (1927)

↑ **Parent:** [Solvay Conference](#solvay-conference)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fifth_Solvay_Conference_(1927))

### Shelter Island Conference

↑ **Parent:** [Physics conference](#physics-conference)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Shelter_Island_Conference)

Sponsored by [National Academy of Sciences](education.md#national-academy-of-sciences), located in [Long Island](united-states.md#long-island).

Some photos at: [http://www.nasonline.org/about-nas/history/archives/milestones-in-NAS-history/shelter-island-conference-photos.html](http://www.nasonline.org/about-nas/history/archives/milestones-in-NAS-history/shelter-island-conference-photos.html) on the website of [National Academy of Sciences](education.md#national-academy-of-sciences), therefore canon. 

This is where [Isidor Rabi](physicist.md#isidor-isaac-rabi) exposed experiments carried out on the [anomalous magnetic dipole moment](quantum-field-theory.md#anomalous-magnetic-dipole-moment) and [Willis Lamb](physicist.md#willis-lamb) presented his work on the [Lamb shift](quantum-field-theory.md#lamb-shift).

It was a very private and intimate conference, that gathered the best physicists of the area, one is reminded of the style of the [Solvay Conference](#solvay-conference).

[QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)](quantum-field-theory.md#qed-and-the-men-who-made-it-dyson-feynman-schwinger-and-tomonaga-by-silvan-schweber-1994) chapter 4.1 this conference was soon compared to the [First Solvay Conference (1911)](#first-solvay-conference-1911), which set in motion the development of [non-relativistic quantum mechanics](quantum-mechanics.md#non-relativistic-quantum-mechanics).

#### Pocono conference

↑ **Parent:** [Shelter Island Conference](#shelter-island-conference)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pocono_conference)

Followup to the [Shelter Island Conference](#shelter-island-conference), this is where [Julian Schwinger](physicist.md#julian-schwinger) and [Richard Feynman](richard-feynman.md) exposed their theories to explain the experiments of the previous conference.

Julian made a formal presentation that took until the afternoon and bored everyone to death, though the mathematics avoided much questioning.

Feynman then presented his revolutionary approach, which he was unable to prove basic properties of, but which gave correct results, and people were not very happy.

## Physicist

↑ **Parent:** [Physics](physics.md)

[This section is present in another page, follow this link to view it.](physicist.md)

## Physics gossip

↑ **Parent:** [Physics](physics.md)

## Unsolved physics problem

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_unsolved_problems_in_physics)

The most important ones are:
- [theory of everything](standard-model.md#theory-of-everything). We are certain that our base equations are wrong, but we don't know how to fix them :-)
  - [Grand Unified Theory](standard-model.md#grand-unified-theory)
  - [strong CP problem](quantum-field-theory.md#strong-cp-problem)
- full explanation of [high-temperature superconductivity](condensed-matter-physics.md#high-temperature-superconductivity). [Superconductivity](condensed-matter-physics.md#superconductivity) already has a gazillion applications, and doing it in higher temperatures would add a gazillion more, and maybe this theoretical explanation would help us find new high temperature superconducting materials more effectively
- [fractional quantum Hall effect 5/2](quantum-mechanics.md#fractional-quantum-hall-effect-5-2)

Other super important ones:
- [neutrino](standard-model.md#neutrino) mass measurement and explanation

## Physics bibliography

↑ **Parent:** [Physics](physics.md)

<h3 id="theoretical-physics-reference-by-ondrej-certik">Theoretical Physics Reference by Ondrej Certík</h3>

↑ **Parent:** [Physics bibliography](#physics-bibliography)

- [https://github.com/certik/theoretical-physics](https://github.com/certik/theoretical-physics)
- [https://www.theoretical-physics.com/dev/index.html](https://www.theoretical-physics.com/dev/index.html)

The only one on [GitHub](software.md#github). In RST and renders to HTML with image formulas.

Too "direct formula overload" at first look.

By the creator of SymPy, who works at [Los Alamos National Laboratory](research-institute.md#los-alamos-national-laboratory) and has a PhD in chemical physics: s[https://www.linkedin.com/in/ondřej-čertík-064b355b/](https://www.linkedin.com/in/ondřej-čertík-064b355b/) Man, big kudos to this dude.

### Physics YouTube channel

↑ **Parent:** [Physics bibliography](#physics-bibliography)

#### Faculty of Khan

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[https://www.youtube.com/channel/UCGDanWUzNMbIV11lcNi-yBg](https://www.youtube.com/channel/UCGDanWUzNMbIV11lcNi-yBg)

This is quite in-depth, pretty good.

Unrelated to the [Khan Academy](website.md#khan-academy).

#### Looking Glass Universe

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[https://www.youtube.com/user/LookingGlassUniverse](https://www.youtube.com/user/LookingGlassUniverse)

Cute simple paper-cut stop motion animations videos by Mithuna Yoganathan, a PhD in theoretical physics at the [University of Cambridge](university.md#university-of-cambridge): [http://www.damtp.cam.ac.uk/person/my332](http://www.damtp.cam.ac.uk/person/my332).

This has the seeds of direct good intuition, but often stops a bit too short. Worth a look though, there is value in them for beginners.

#### Ludic Science

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[https://www.youtube.com/channel/UCM014DFZ7peFVrSaxnh4-Mw](https://www.youtube.com/channel/UCM014DFZ7peFVrSaxnh4-Mw)

Maybe [Spanish](linguistics.md#spanish-language) accent, but might also be from some other [european](continent.md#europe) language.

Very practical, low-cost experiments.

#### minutephysics

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[https://www.youtube.com/channel/UCUHW94eEFW7hkUMVaZz4eDg](https://www.youtube.com/channel/UCUHW94eEFW7hkUMVaZz4eDg)

#### Physics Explained

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[https://www.youtube.com/c/PhysicsExplainedVideos](https://www.youtube.com/c/PhysicsExplainedVideos)

Falls a bit too much on the basic side of the [the missing link between basic and advanced](ciro-santilli.md#the-missing-link-between-basic-and-advanced).

#### ScienceClic

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

- [English](linguistics.md#english-language): [https://www.youtube.com/channel/UCWvq4kcdNI1r1jZKFw9TiUA](https://www.youtube.com/channel/UCWvq4kcdNI1r1jZKFw9TiUA)
- French: [https://www.youtube.com/user/ScienceClic](https://www.youtube.com/user/ScienceClic)

This is very promising.

#### Steve Mould

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Steve_Mould)

[https://www.youtube.com/channel/UCEIwxahdLz7bap-VDs9h35A](https://www.youtube.com/channel/UCEIwxahdLz7bap-VDs9h35A)

#### The Science Asylum

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[https://www.youtube.com/channel/UCXgNowiGxwwnLeQ7DXTwXPg](https://www.youtube.com/channel/UCXgNowiGxwwnLeQ7DXTwXPg)

##### Nick Lucid

↑ **Parent:** [The Science Asylum](#the-science-asylum)

[Ciro Santilli](ciro-santilli.md)'s answer to [How credible is Nick Lucid, of YouTube's "The Science Asylum"?](https://www.quora.com/How-credible-is-Nick-Lucid-of-YouTubes-%E2%80%9CThe-Science-Asylum%E2%80%9D/answer/Ciro-Santilli) on [Quora](website.md#quora).

#### UCSB Physics Lecture Demonstrations

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)  
🏷️ **Tags:** [UCSB](university.md#university-of-california-santa-barbara)

- [https://www.youtube.com/playlist?list=PLGImELmE_zlPqmRbbvZ1MjWnbFovcwBBO](https://www.youtube.com/playlist?list=PLGImELmE_zlPqmRbbvZ1MjWnbFovcwBBO)
- [https://web.physics.ucsb.edu/~lecturedemonstrations/](https://web.physics.ucsb.edu/~lecturedemonstrations/)
- [https://web.physics.ucsb.edu/~lecturedemonstrations/Demonstration%20Videos.html](https://web.physics.ucsb.edu/~lecturedemonstrations/Demonstration%20Videos.html)

TODO find teacher name, all seem to be made by the same cute dude from [UCSB](university.md#university-of-california-santa-barbara).

#### UNSW Physics YouTube channel

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)  
🏷️ **Tags:** [UNSW](university.md#university-of-new-south-wales)

#### Veritasium

↑ **Parent:** [Physics YouTube channel](#physics-youtube-channel)

[YouTube](website.md#youtube) channel: [https://www.youtube.com/channel/UCHnyfMqiRRG1u-2MsSQLbXA](https://www.youtube.com/channel/UCHnyfMqiRRG1u-2MsSQLbXA)

Does have some gems worth looking at. But generally always [too superficial](science.md#popular-science) as can be expected from any self-sufficient YouTubber.

<a id="video-my-life-story-by-veritasium-2018"></a>
**[Video 6](#video-my-life-story-by-veritasium-2018). My Life Story by Veritasium (2018)** [Source](https://www.youtube.com/watch?v=S1tFT4smd6E). Basically a [don't be a pussy](don-t-be-a-pussy.md) story where he describes how he has always been passionate by both [science](science.md) and [film making](film.md). Veritasium is a nice guy.

### Physics journal

↑ **Parent:** [Physics bibliography](#physics-bibliography)  
🏷️ **Tags:** [Academic journal](education.md#academic-journal)

The strongest are:
- early 20th century: [Annalen der Physik](education.md#annalen-der-physik): God [OG](linguistics.md#original-gangster) physics journal of the early 20th century, before the [Nazis](continent.md#nazism) fucked German science back to the [Middle Ages](science.md#middle-ages)
- 20s/30s: [Nature](education.md#nature-journal) started picking up strong
- 40s/50s: [American](united-states.md) journals started to come in strong after all the genius [Jews](religion.md#judaism) escaped from [Germany](continent.md#germany), notably [Physical Review Letters](#physical-review-letters)

#### Physics Letters

↑ **Parent:** [Physics journal](#physics-journal)  
🏷️ **Tags:** [Elsevier](education.md#elsevier)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Physics_Letters)

##### Physics Letters A

↑ **Parent:** [Physics Letters](#physics-letters)

[https://www.sciencedirect.com/journal/physics-letters-a](https://www.sciencedirect.com/journal/physics-letters-a)

##### Physics Letters B

↑ **Parent:** [Physics Letters](#physics-letters)

[https://www.sciencedirect.com/journal/physics-letters-b](https://www.sciencedirect.com/journal/physics-letters-b)

#### Journal by the American Physical Society

↑ **Parent:** [Physics journal](#physics-journal)  
🏷️ **Tags:** [American Physical Society](education.md#american-physical-society)

##### Physical Review

↑ **Parent:** [Journal by the American Physical Society](#journal-by-the-american-physical-society)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Physical_Review)

List of the sub-journals at: [https://journals.aps.org/browse](https://journals.aps.org/browse)

###### Paper published on Physical Review 

↑ **Parent:** [Physical Review](#physical-review)  
🏷️ **Tags:** [Paper](education.md#academic-paper)

##### Physical Review Letters

↑ **Parent:** [Journal by the American Physical Society](#journal-by-the-american-physical-society)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Physical_Review_Letters)

As indicated by its name, the journal contains mostly short letters sent to the editor, often 2 or 3 pages long, which allows for a faster publication cycle and dissemination of new results. This is notably useful for [experimental physics](#experimental-physics).

###### Physical Review Letters article

↑ **Parent:** [Physical Review Letters](#physical-review-letters)

## 🏷️ Tagged (1)

- [Physics research institute by country](research-institute.md#physics-research-institute-by-country)

## ↑ Ancestors (3)

1. [Natural science](science.md#natural-science)
2. [Science](science.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (40)

- [Ciro Santilli's Homepage](README.md)
- [100 Greatest Discoveries by the Discovery Channel (2004-2005)](science.md#100-greatest-discoveries-by-the-discovery-channel-2004-2005)
- [Abraham Pais](physicist.md#abraham-pais)
- [Adolfo Amidei](physicist.md#adolfo-amidei)
- [Animal rights](cirism.md#animal-rights)
- [Art](art.md)
- [The best articles by Ciro Santilli](articles.md)
- [Chemistry](chemistry.md)
- [Ciro Santilli's bad old event memory](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-bad-old-event-memory)
- [Closed access academic journals are evil](education.md#closed-access-academic-journals-are-evil)
- [Computational physics](#computational-physics)
- [Deep tech](technology.md#deep-tech)
- [Deletionism on Wikipedia](website.md#deletionism-on-wikipedia)
- [Don't be a pussy](don-t-be-a-pussy.md)
- [Existence and uniqueness of solutions of partial differential equations](calculus.md#existence-and-uniqueness-of-solutions-of-partial-differential-equations)
- [Formalization of mathematics](formalization-of-mathematics.md)
- [Formalization of physics](formalization-of-mathematics.md#formalization-of-physics)
- [Having more than one natural language is bad for the world](cirism.md#having-more-than-one-natural-language-is-bad-for-the-world)
- [High flying bird vs gophers](mathematics.md#high-flying-bird-vs-gophers)
- [Important partial differential equation](calculus.md#important-partial-differential-equation)
- [Minimal working example](software.md#minimal-working-example)
- [Molecular Sciences Course of the University of São Paulo](university.md#molecular-sciences-course-of-the-university-of-sao-paulo)
- [Murray Gell-Mann](physicist.md#murray-gell-mann)
- [Natural science](science.md#natural-science)
- [Open boundary condition](calculus.md#open-boundary-condition)
- [OurBigBook.com](the-most-important-projects-done-by-ciro-santilli.md#ourbigbook-com-top-project)
- [Motivation](ourbigbook-com.md#motivation)
- [Physics](physics.md)
- [Physics is a way to predict the future](#physics-is-a-way-to-predict-the-future)
- [Physics Travel Guide](physicist.md#physics-travel-guide)
- [Project to explain each Nobel Prize better](nobel-prize.md#project-to-explain-each-nobel-prize-better)
- [Ron Maimon](stack-overflow.md#ron-maimon)
- [Rooting for sport teams is stupid](cirism.md#rooting-for-sport-teams-is-stupid)
- [Settheory.net](physicist.md#settheory-net)
- [Single electron double slit experiment](quantum-mechanics.md#single-electron-double-slit-experiment)
- [Sponsor Ciro Santilli's work on OurBigBook.com](sponsor.md)
- [Telecommunication](telecommunication.md)
- [The beauty of mathematics](mathematics.md#the-beauty-of-mathematics)
- [Theory of everything](standard-model.md#theory-of-everything)
- [Videos of all key physics experiments](todo.md#videos-of-all-key-physics-experiments)
