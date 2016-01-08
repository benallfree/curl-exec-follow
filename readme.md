# Overview

PHP's `curl` library doesn't work well on shared hosting environments.

When `open_basedir` is set, the `CURLOPT_FOLLOWLOCATION` will cause an error and fail. This code works around that issue, which is common on shared hosting.

# Usage

Wherever you'd use `curl_exec`, use `curl_exec_follow` instead.