# Concepts

1. Physics of MRI
2. File Formats
3. the BOLD signal
    - what contributes to it?
    - how can we interpret it?
4. Other sources that contribute to MRI signal
    - what are they?
    - How do they contribute to the MRI signal?
    - How do we account for them?
5. How do we model the data?
    - Introduction to linear models
    - How do we remove the confounds and model the changes?
6. Reporting the results

## Physics of MRI

Understanding how we see the soft tissue in the brain through magnets is a mind blowing concept and is not without it's pitfalls. 
Knowing the conceptual background behind how images are acquired will be useful when you are quality checking your data and trying to derive necessary bits of information for preprocessing your data. Slicetiming, echo time, repetition time,phase encoding direction, and many other words are jargon without the appropriate background, but can be essential parameters to know when working with your data.

Another mri lecture series
- [Shimoney](https://sites.wustl.edu/nillabs/mr-lecture-series/)

The best lecture series I would start with is Dr. Lipton's series on MRI
- [Dr. Lipton Lectures](https://www.youtube.com/playlist?list=PLH_k6d9j2lGUms4QZzokrkXGEoP6oxkYH)

For some interactive learning of how the hydrogen atoms behave in the scanner, use this simulator.

- [Sequence Simulator](http://www.drcmr.dk/BlochSimulator/)

Finally, if you want some more in-depth walkthroughs of what Dr. Lipton covered, the MRI questions website has been immensely helpful.

- [MRI questions](http://mriquestions.com/index.html)

An alternative to Dr. Lipton's Lectures is practical fMRI.

- [PractiCAL fMRI physics](https://practicalfmri.blogspot.com/2012/02/physics-for-understanding-fmri.html)

## File Formats

Since we have collected the data on the MRI scanner, it has to be saved somehow.
Instead of an image file like a jpeg or a png, the standard medical file format is dicoms.
Dicoms contain a large amount of meta-data that is necessary to understand how exactly the image was aquired (which will be essential when preprocessing the image).
However, we do not use dicoms when analyzing the data, instead we commonly use a leaner file format (NIfTI) that does not contain as much metadata and merges the individual 2D dicoms into a 3D (or 4D) shape.
This file format does get rid of some useful information that is present in the dicoms making it necessary to store the dicom information in some manner along side the NIfTI file.

For a comprehensive and high level review of dicoms check out Roni's series.

- [Roni's Dicom Tutorial](http://dicomiseasy.blogspot.com/2011/10/introduction-to-dicom-chapter-1.html)

Straight from the horse's mouth you can look at the dicom standard website itself

- [dicom standard website](https://www.dicomstandard.org/)

and crucially, you should know that each MR vendor has their own conformance statement to the DICOM standard, for example here is the [GE 750W Discoveries conformance statement](https://www3.gehealthcare.com/~/media/documents/us-global/products/interoperability/dicom/magnetic-resonance/gehc-dicom-conformance_dv25-1-disoverymr750w-750-450-optimamr450w_doc1708004_rev2.pdf)

For files NIfTI there is NIfTI-1 and NIfTI-2

- [NIfTI-1](https://nifti.nimh.nih.gov/nifti-1/)
- [NIfTI-2](https://nifti.nimh.nih.gov/nifti-2/)
- [NIFTI faq](https://nifti.nimh.nih.gov/nifti-1/documentation/faq)

And a high level introduction

- [brainder intro](https://brainder.org/2012/09/23/the-nifti-file-format/)

Finally, a popular tool that attempts to translate information from dicoms to NIfTIs is dcm2niix

- [dcm2niix wiki](https://www.nitrc.org/plugins/mwiki/index.php/dcm2nii:MainPage)

## The BOLD signal

- [mri question: bold contrast](http://mriquestions.com/bold-contrast.html)

## Other Sources

- [What's Neuronal and what's not](https://fmrif.nimh.nih.gov/course/2017/08_Dan_20170619)

## Model Data

- [regressionResources](https://github.com/jdkent/regressionResources)

### Other Online Courses for Learning about fMRI
- [FMRIF](https://fmrif.nimh.nih.gov/public/fmri-course/index_html)
- [OHBM](https://www.pathlms.com/ohbm)
- Principles of fMRI [1](https://www.coursera.org/learn/functional-mri) and [2](https://www.coursera.org/learn/functional-mri-2)
