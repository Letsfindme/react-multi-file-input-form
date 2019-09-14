# Welcome to react custom input!

Hi! i ceated this custom input for my personal project **LetsFind ME**.and i want to share it with you.
this custom input manages text, files, images, select and checkbox.


# How to use

- You need to install **Formik** 
then create your custom field like so:
```const  fields  =  [{ label:  "Title for your post", type:  "input", name:  "title", value:  "" }];```

- Install **YUP** schema validator and create validation schema:
	``` export  const  newPostValid  =  Yup.object().shape({
	title:  Yup.string()
	.max(35,  "35 characters max")
	.required("Please entre a title for this post"),
	});
	```

- Then create your custom input like so:
	```
	<Input
	cancel
	value={postForm.title}
	control="form"
	fields={fields}
	validation={newPostValid}
	onChange={postInputChangeHandler}
	formSubmit={value =>  acceptPostChangeHandler(value)}
	btnValue="Create my post"
	cancelPostChangeHandler={cancelPostChangeHandler}
	>
	```
