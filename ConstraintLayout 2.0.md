# ConstraintLayout 2.0 by Nicolas Roard and John Hoford, Google EN

## ConstraintLayout1.1
###  - BARRIERS
### - Placeholder
### - Optimizer
#### constraints- optimizer- mesures - solver

## ConstraintLayout 2.0
why we want to build constraintlayout 2.0
UI: rasing the bar
key: helpers

### what's a helper
- not necessarily part of your view hierarchy
- helps you specify and build your ui
- example: guideline, barrier 

### main categories of helpers
- layout manipulation 
- post layout manipulation
- rendering or decorating

### constraint helpers
- keep a reference to existing views
- flat hierarchy
- view can be referenced by multiple helpers
- essentially, it allows you to tag views ,setting specific behaviors

### Decorator
- manipulate graphically a collection of views
- supports transforms, etc,
- can be set as the bounding box of the refernced views

### Virtual Layouts
- layout the referenced views
- stil keep flat hierarchy
- linear
- flow

