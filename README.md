# Holiday Photos

This repo is being used for hosting photos on my 2023 Europe vacation, and as a very barebones CMS. There is also a website that will use the github REST API to pull the photos and display them in a nice way.

## Uploading Photos

Photos will be displayed in sections based on what folder they are in. The folders must be named in this pattern `*number*_*photo-name*`. The sections will be ordered based on the number in the folder name, with the lower numbers being displayed at the bottom.

To upload photos, simply copy/paste them into the folder you want them in, then make a commit and push. This repo has an automated workflow that will trigger a re-build of the frontend website so that it stays up to date with the photos.

## Adding a Section Description

We can have the frontend show some text under a section's title by creating a `README.md` file in the folder that corresponds with the section. The text in the `README.md` file will be displayed under the section title.

Any markdown formatting applied in the README file will not be rendered in the frontend, so it is best to keep it simple.

## Adding Photo Captions

To add a caption to a photo, create a `data.json` file in the same section as the photo, in that file create a structure like this:

```json
{
	"captions": {
		"photo-name.jpg": "This is a caption for the photo"
	}
}
```

Within the "captions" object, you can add a caption to an image by adding the image's file name as a key, and the caption as the value.
