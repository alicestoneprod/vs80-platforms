# VS80 Build Tools Support in Visual Studio 2010

## Problem

Visual Studio 2010 does not support the VS80 build tools (Visual Studio 2005) out of the box, even if Visual Studio 2005 is installed.  
As a result, attempting to compile an old project that relies on the `v80` toolset will fail due to missing platform toolset configurations.

## Solution

To work around this limitation, you can use the `v100` platform toolset (from VS2010), rename it to `v80`, and modify additional property sheets to mimic the original VS80 environment.

### Steps to Apply the Fix

I have already prepared the necessary files, so you can simply copy them into the following directory:
`C:\Program Files (x86)\MSBuild\Microsoft.Cpp\v4.0\Platforms`
This will allow Visual Studio 2010 to recognize `v80` as a valid platform toolset and enable compilation of projects originally designed for Visual Studio 2005.
