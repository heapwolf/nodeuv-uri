# SYNOPSIS
a little C++ library that parses URLs into bite-sized pieces.

# EXAMPLE
```cpp
#include <iostream>
#include <UriParser.h>

using namespace std;
using namespace uri;

int main() {

  string haystack = "http://user:password@www.google.com:80/path?search";

  auto parsed = ParseHttpUrl(haystack);
  
  cout << "Protocol: " << parsed.protocol << "\n"
       << "User:     " << parsed.user << "\n"
       << "Password: " << parsed.password << "\n"
       << "Host:     " << parsed.host << "\n"
       << "Port:     " << parsed.port << "\n"
       << "Path:     " << parsed.path << "\n"
       << "Search:   " << parsed.search << std::endl;
}
```

This is based on the url spec defined in 
[RFC 1738](http://www.ietf.org/rfc/rfc1738.txt).e

# License
This code is licensed under the [MIT License](http://opensource.org/licenses/MIT). See `LICENSE.txt`.

