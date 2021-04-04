[![SPASE Manual Validation](https://github.com/hpde/CCMC/actions/workflows/validate.yml/badge.svg)](https://github.com/hpde/CCMC/actions/workflows/validate.yml)
[![SPASE Push Validation](https://github.com/hpde/CCMC/actions/workflows/validate-push.yml/badge.svg)](https://github.com/hpde/CCMC/actions/workflows/validate-push.yml)

# CCMC
Community Coordinated Modeling Center (CCMC) - NASA

Visit the [website](https://ccmc.gsfc.nasa.gov/) [https://ccmc.gsfc.nasa.gov/]

# How to Use This Repository

If you are a consumer of the metadata simply clone the repostory with:

````
git clone -b master --single-branch --depth=1 https://github.com/hpde/CCMC
````

If you are a contributor, clone the repository and use the "draft" branch.
````
git clone git@github.com:hpde/CCMC.git
git checkout draft
````

After pushing updates send a "pull request". After a review, the changes
will be added to the master branch and shared with consumers.

# Validation Actions

GitHub actions are configured for this repository. When a "git push" occurs 
a validation and referential check is performed on the changes or additions 
to the repository since the last push. The status of the action is displayed in the
"SPASE Push Validation" badge at the top of the page. You can view the log of the
validation by viewing the [action workflows](../../actions), clicking on the appropriate workflow
run, then "validate-log" artifict.

The "SPASE Push Validation" is designed to incrementally validate the repository. It assumes
that the repository is valid before the "git push". To perform a whole repository validation
run the "SPASE Manual Validation" action.  To manually run an action go to the [actions](../../actions) page,
select the "SPASE Manual Validation" action, then click on "Run Workflow". For large repositories it 
can take many minutes for the workflow to complete - be patient. Once it is complete the "SPASE Manual Validation"
badge will update.

**Note on badge refresh**: The status portion of a badge is an image. Typically browsers cache images so an 
updated status may not appear immediately. One way to view the current badge is to clear cached images back to when you
last loaded the page, then refresh the page.

**Notes for repository administrator**: There is no garbage collection for workflows. So, its a good practice to
occassionally visit the [action workflows](../../actions) and remove old workflow runs. To remove a run click
the elipses (...) for a work flow and select "Delete workflow run". Typically you would only need the most recent run.