# CAD for iterative design

## Context

_MAE2250 Intro to Mechanical Design_ at Cornell Mechanical & Aerospace
Engineering (MAE) is a sophomore (4th semester) class with an enrollment of
about 200 students, and it is the first required course for students to
affiliate to our department.

The course is structured around two lectures and one lab-section per week, with
lab-sections being limited to 20 students per section, and with access to power
tools and fabrication tools, namely laser-cutting, drill-press, bandsaw, and
sanding belt. Other fabrication methods, including mills, lathes, and 3D
printers are available to students _outside_ standard class hours.

The intended learning objectives include (excerpt from the syllabus):

> You will work through the various stages of the design process, namely (1)
> identify and define the problem, then (2) exploring the solution space, and
> finally (3) execute a given solution through **iterative prototyping and
> validation**.

We recognized that previous instruction did not sufficiently emphasize the
**iterative prototyping and validation** portion, and taught different design
tools (including CAD, e.g.~Autodesk Fusion360) in isolation, which led to
students applying the tools in a sequential manner. In other words, we want to
move instruction for CAD _away_ from understanding where buttons are, and
towards decision-making in design. For this to happen, assignments need to be
open-ended enough for decision-making to matter, and they need to involve both
design and implementation, so the consequences of those decisions are tangible.
A major challenge we saw is, for a class of 200, open-ended assignments lead to
designs that are not only difficult to grade, they are difficult _and_ expensive
to fabricate.

Our main strategy for managing scoping is to use constraints that naturally
funnels the design decisions to a set we can manage. For assignments with
fabrication, students will have time and budget constraints, and are limited to
either the McMaster catalog, or components we have pre-sourced and have in
stock. The pre-sourced components allow us to keep costs down, and we can price
them accordingly such that students can only afford a few components from
McMaster, but need to rely the cheaper pre-sourced components. This gives us a
good tuning knob of how much flexibility they have in their design space.

We also want to de-emphasize 3D printing as a fabrication method, as it allows
students to be lazy about thinking of how fabrication/assembly impact design. We
address this (in some assignments) by having very stringent fabrication-time
constraints (fabricate during lab section), which should drive people to using
the laser-cutter or similar.

### Current State

_September 2026_  
We've finished a first iteration of the redesign over summer, with the help of 3
UG students who just finished taking the class.  
The redesigned assignments are not yet fully tested, and will be in the spring
semester 2027.  
We have done _some_ testing over the summer with the students executing (some)
of the assignments.

### Assignment List

#### Coffee Mugs

**ILO**: basic CAD This is an existing assignment: CAD a coffee mug, using
different features (e.g. extrude, revolve, etc.)

#### Coffee Travel Thermos

**ILO**: Parameter-driven design This is an existing assignment: CAD a travel
thermos with lid, that is parameterized so you can change 1 parameter (cup
volume), and it automatically scales your entire design.

### SwissCard

This is a team-based assignment, with each student designing one tool for a
credit card-sized multi-tool.

**ILO:**

- Work on CAD in a team-setting
- Use top-down (aka master-modeling) design workflow

#### Mug Rack

Design and build a rack for your mugs, using only fabrication techniques
available to you in the Design Studio (hand-tools, laser-cutter, bandsaw,
drill-press).

**ILO**

- Design around fabrication technique, considering speed, ease of assembly,
- Connect to _ENGRD2020 Statics_, using free-body diagrams to assess
  load-bearing and stability requirements

We expect students to converge towards laser-cutting as it is the fastest
fabrication method they will have available to them. This will require them to
design a rack that can be assembled from flat parts (see examples), which will
also emphasize tolerancing and assembly. We will also make sure to provide
cardboard tubes, wood dowels, blocks, and similar, such that students do have
other pathways available.

### Coffee Grinder

This is the core of the redesign, and is a 4-assignment sequence. Students will
design a hand-powered coffee grinder, and build a validation prototype of the
assembly and test mechanism. We will pre-source many of the components incl.
gears and burrs for the grinder, and price them accordingly; student will have
to do component selection while staying under-budget (100 USD per student),
either from our stock or McMaster. This budget is how we're constraining designs
to using the components (and therefore design choices) we've made, while keeping
the actual assignment open-ended.

#### Step 1

Use sketches and simple prototype (cardboard, wooden dowels, etc.) to identify
rough sizing, load-bearing points and bearing types, etc. Sketch and CAD a rough
design of what you expect the final product to be. Decide on validation criteria
for the mechanism (what loads/throughput etc., and how will you test it).

#### Step 2: Design a testbed

Select components on McMaster or pre-sourced in the class while staying
under-budget, and design a testbed to validate the assembly. The testbed does
not have to stay in the constraints of the final grinder, but needs to be close
enough that it is an accurate validation (should test the appropriate loads).
Peer review: student will be assigned another student's design to review, with
an emphasis on ensuring all critical points are tested.

#### Step 3: Fabricate the testbed, validate the design

Assemble your testbed, documenting the assembly process (produce an assembly
manual). Execute your validation tests (from Step 1), note results.

#### Step 4:

Based on the validation outcome, adjust your design, and finalize the housing.
Peer review designs, and ensure designs are ready for fabrication.

Next year, we plan to further develop step 4.

## LaTeX handouts

All handouts use the shared
[`styles/mae2250-handout.sty`](styles/mae2250-handout.sty) for typography,
headers, title blocks, and lists. Compile with pdfLaTeX or XeLaTeX from the
source folder; the PDF and auxiliary files are written there. For example, in
`A3_MugRack/`:

```sh
pdflatex MugRack.tex
# or
xelatex MugRack.tex
```
