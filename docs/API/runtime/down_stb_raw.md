# download_stb_raw(URL, file_path)

| Parameter | Class |
| --- | --- |
| URL | String |
| file_path | String |


`download_stb_raw` downloads a single file from a github repository to your project folder.  The first argument is a URL of a specific Github file while the second is a file path relative to your project folder.  

This function can help facilitate the integration of external code files. Open Source Software (OSS) contributors are encouraged to create libraries that all fit in one file (lowering the barrier to entry for adoption).

## Example

```ruby
def tick args
end

# source code will be downloaded from a direct/raw url and saved to a direct/raw local path.
$gtk.download_stb_rb_raw "https://raw.githubusercontent.com/xenobrain/ruby_vectormath/main/vectormath_2d.rb",
                         "lib/xenobrain/ruby_vectionmath/vectormath_2d.rb"
```

## Related Functions

[download_stb_rb](download_stb_rb.md)
