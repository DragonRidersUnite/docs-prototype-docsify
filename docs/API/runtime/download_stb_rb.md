# download_stb_rb(URL), download_stb_rb(github_user, repository, file)

| Parameter | Class | Parameter | Class |
| --- | --- | --- | --- |
| URL | String | github_user | String |
|  |  |  repository | String |
| | | file | String |


`download_stb_rb` downloads a single file from a github repository to your project folder.  This function can have two forms.  If the first argument is a URL of a specific Github file, the other parameters can be omitted.  
Otherwise, if all three parameters are provided, the first parameter must be a github user name, then a repository name and finally a file path.  

This function can help facilitate the integration of external code files. Open Source Software (OSS) contributors are encouraged to create libraries that all fit in one file (lowering the barrier to entry for adoption).

## Example

```ruby
def tick args
end

# option 1:
# source code will be downloaded from the specified GitHub url, and saved locally with a
# predefined folder convension.
$gtk.download_stb_rb "https://github.com/xenobrain/ruby_vectormath/blob/main/vectormath_2d.rb"

# option 2:
# source code will be downloaded from the specified GitHub username, repository, and file.
# code will be saved locally with a predefined folder convension.
$gtk.download_stb_rb "xenobrain", "ruby_vectormath", "vectormath_2d.rb"
```

## Related Functions

[download_stb_raw](download_stb_raw.md)
