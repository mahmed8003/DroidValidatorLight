# DroidValidatorLight
[![](https://jitpack.io/v/mahmed8003/DroidValidatorLight.svg)](https://jitpack.io/#mahmed8003/DroidValidatorLight)

This library is heavily inspired by [AwesomeValidation](https://github.com/thyrlian/AwesomeValidation) but with no external dependencies. It makes it very light weight

### Setup
Step 1. Add the JitPack repository to your build file
Add it in your root build.gradle at the end of repositories:
```gradle
allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
```

Step 2. Add the dependency
```gradle
compile 'com.github.mahmed8003:DroidValidatorLight:${VERSION}'
```


### Usage Examples
```java
Form form = new Form(this);
form.enablePerFieldErrorMessageDisplay(); // If you want per field validation

// For simple scenarios
form.check(editText, RegexTemplate.NOT_EMPTY_PATTERN, "Must not be empty");
form.check(editText, RegexTemplate.EMAIL_PATTERN, "Must be an Email");
form.checkLength(editText, Range.equalOrLess(12), "Text length must be less or equal to 12");

form.checkValue(editText2, Range.equalOrMore(23), "Entered value must be greater equal than 23");

if(form.validate()) {
    Toast.makeText(this, "Success", Toast.LENGTH_LONG).show();
}

```

You can remove validate from form as well, You can make your own validators by extending Validator class.

Happy Validation, Thanks

License
-------

    Copyright (C) 2018 Muhammad Ahmed

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


