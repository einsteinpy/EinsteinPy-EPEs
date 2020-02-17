EPEs: EinsteinPy Proposals for Enhancement
------------------------------------------

EPEs are documents to address non-trivial enhancements that require discussion
and thought beyond a single Pull Request. EPEs are also meant to put forward and document the 
governance model of The EinsteinPy Project. This is intended to mirror the
long-standing Python Enhancement Proposal, and Astropy Proposal of Enhancement process, but generally not quite as
formally. Normally a proposal goes through various phases of consideration.
Discussion is expected to take place using existing mechanisms (einsteinpy-dev,
github, hangouts, etc), and eventually a decision is made regarding whether the
proposal should be accepted, rejected, or modified.

Accepted EPEs
^^^^^^^^^^^^^

=== ================================================================ =========== ============
#     Title                                                          Date        DOI
=== ================================================================ =========== ============
.. 1   `EPEs and EinsteinPy Governance`_                             2020-Feb-02 |EPE 1 DOI|
=== ================================================================ =========== ============

.. _EPEs and EinsteinPy Governance: https://github.com/einsteinpy/EinsteinPy-EPEs/blob/master/EPE_00001.rst

.. |EPE 1 DOI| image:: https://zenodo.org/badge/DOI/10.5281/zenodo.1043886.svg
   :target: https://doi.org/10.5281/zenodo.1043886


Proposing a new EPE
^^^^^^^^^^^^^^^^^^^

New EPEs should be created using the ``EPEtemplate.rst`` file in this repository.
Fork the repository, copy ``EPEtemplate.rst`` to
``EPE_<some_working_name>.rst`` and issue a Pull Request with that file once
you've written it up (little explanation is required in the PR itself given that
the document has all the content - usually it's easiest to just paste in the
abstract). The EPE number will be assigned once the PR is merged.

Note that there is not much point to making proposals unless someone or some
group has signed up to implement it if the EPE is accepted
(typically this would involve the author or authors of the EPE).  Just issuing
an EPE in order to spur others to do work is not generally going to be received
well. Generally, an implementation is expected before an EPE can be considered
fully accepted. For proposals that require extensive work that few are willing
to perform without some assurance it will be accepted, provisional acceptance
is an option. For serious consideration it is usually good to show that detailed
technical aspects have been played with in real code rather (even if it isn't a
complete implementation) [This point only applies to non-governance EPEs] .

Finalizing EPEs
^^^^^^^^^^^^^^^

The final decision on accepting or rejecting EPEs lies with the EisnteinPy
Coordination Group.  Once the community discussion on the EPE has wound
down, the group discusses the EPE and makes a final decision on acceptance
or rejection.  One of the group members should then:

1. Fill in the "Decision rationale" section of the EPE with a description of why
   the EPE was accepted or rejected, including a summary of the community's
   discussion as relevant.
2. Update the "date-last-revised" to the day of merging and "status" to
   "Accepted" or "Rejected".
3. If necessary, rename the EPE file to be ``EPE##.rst``, where ## is the next
   free number on the list of EPEs.
#. Leave a brief comment in the PR indicating the result.
#. Merge the PR with the above changes.
#. If the EPE was accepted then continue with the remaining steps, otherwise stop now.
#. Upload the EPE to Zenodo to give it a DOI.  Go to https://zenodo.org/deposit/new, upload
   the .rst file, and set the fields to the following:

   ============================= ======================================================
   Zenodo field                  Set to
   ============================= ======================================================
   Communities                   The EinsteinPy Project
   Upload type                   Publication
   Publication type              Technical note
   Publication Date              The date-last-revised of the EPE (which should be the same as the accepted date for new APEs)
   Title                         EinsteinPy Proposal for Enhancement <number>: <title> (EPE <number>)
   Authors                       The EPE authors (directly from the APE text, but with ORCIDs if possible)
   Description                   The EPE abstract (copy/paste the rendered HTML from GitHub)
   License                       CC-Attribution (default)
   Related/alternate identifiers Github link to the APE file *at the specific merge commit* (e.g. https://github.com/astropy/astropy-APEs/blob/42951733ac42c0ea178d8df30705274a43c93091/APE1.rst) as "is supplemented by this upload". If this is a revised version, this should be the URL of the commit where the APE was revised.
   ============================= ======================================================

#. Get the source for the DOI badge from the newly-created Zenodo record page by
   clicking on the DOI badge on the right side of the page and copying the
   reStructuredText source.
#. On GitHub (or locally) edit ``README.rst`` and add an entry for the new APE to the
   "Accepted EPEs" table.  Use the DOI link from the previous step.  Add
   corresponding RST link refs for both the DOI link and the new EPE.  Preview
   the update and test the links to make sure they are all correct.  Then commit
   directly to master (or PR if you prefer).
#. Send an email to `einsteinpy-dev <https://groups.io/g/einsteinpy-dev>`_
   announcing the acceptance In general this should just point to the accepted
   EPE rather than providing additional decision rationale.

Updating EPEs
^^^^^^^^^^^^^

In the cases where an updated EPE requires updating (e.g. references to a  new
EPE that supercedes it, clarifying information that emerges after the EPE is
accepted, etc.), changes can be made directly via PR, but the
"date-last-revised" should be updated in the EPE. Additionally, the Zenodo entry
will need to be updated with a new version of the EPE (*not* a completely new
Zenodo entry), by using the "New version" button and then filling out the forms
as described above.
