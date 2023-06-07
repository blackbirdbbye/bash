## All the bash commands that I've used in practical and commercial projects.
```bash
# Navigating Directories
pwd                                              # Print current directory path
ls                                               # List directories
cd mark                                          # Go to mark sub-directory
cd                                               # Go to home directory
cd ~                                             # Go to home directory
cd -                                             # Go to last directory

# Creating Directories
mkdir mark                                       # Create a directory
mkdir mark mark2                                 # Create multiple directories

# Moving Directories
cp -R mark mark2                                 # Copy directory
mv mark mark2                                    # Move directory

# Deleting Directories
rmdir mark                                       # Delete empty directory
rm -r foo                                        # Delete directory including contents
rm -rf mark                                      # Delete directory including contents, ignore nonexistent files and never prompt

# Creating Files
touch mark.txt                                   # Create file or update existing files modified timestamp
touch mark.txt mark2.txt                         # Create multiple files
touch {mark,mark2}.txt                           # Create multiple files
touch mark{1..3}                                 # Create mark1, mark2 and mark3 files     
touch mark{a..c}                                 # Create marka, markb and markc files

# Standard Input
echo "mark" > bar.txt                            # Overwrite file with content
echo "mark" >> bar.txt                           # Append to file with content

# Moving Files
cp mark.txt mark2.txt                            # Copy file
mv mark.txt mark2.txt                            # Move file

# Deleting Files
rm mark.txt                                      # Delete file
rm -f mark.txt                                   # Delete file, ignore nonexistent files and never prompt

# Reading Files
cat mark.txt                                     # Print all contents
less mark.txt                                    # Print some contents at a time 
head mark.txt                                    # Print top 10 lines of file
tail mark.txt                                    # Printсom 10 lines of file

# Finding Files
find /path -name mark.txt                        # Find a file
find /path -iname mark.txt                       # Find a file with case insensitive search
find /path -name "*.txt"                         # Find all text files
find /path -name mark.txt -delete                # Find a file and delete it

# Find in Files
grep 'hi' /mark.txt                              # Search for 'hi' in file 'mark.txt'
grep 'hi' /mark -R                               # Search for 'hi' in directory 'mark' and follow symbolic links
grep 'hi' /mark -c                               # Count the number lines that match

# Replace in Files
sed 's/gd/bb/' mark.txt -i                       # Replace fox with bear and overwrite mark.txt

# Processes
ps all                                           # List all processes
kill PID                                         # Shut down process by PID gracefully. Sends TERM signal.

# HTTP Requests
curl https://example.com                         # Return response body
curl -X POST -H "Content-Type: application/json" # POST JSON
-d @name.json https://example.com 

# Network Troubleshooting
ping example.com                                 # Send multiple ping requests using the ICMP protocol
ping -c 5 -i 3 example.com                       # Make 5 attempts, 3 seconds apart
```
