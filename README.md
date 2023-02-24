# snap-py-simple

Building a python app using snapcraft using github actions.

Need to add a setup.py

But https://packaging.python.org/en/latest/tutorials/packaging-projects/ uses pyproject.toml

More research needed.

## snapcraft build

Uses the official snapcraft Python example.
Results in a local snap

Though I had to change the yml slightly - see https://forum.snapcraft.io/t/python-apps/6741/30 

## github actions

Uses the snapcraft build action
https://github.com/snapcore/action-build

results in the same snap being built via github actions

## install the snap

	snap install --devmode --dangerous yt-dlp_2023.02.17-4-gcc0908363_multi.snap
	snap list
	yt-dlp --help

## To trigger the github action

	git tag list
	git tag -a pre-14
	git push --follow-tags

