## Install Postgres
brew doctor
brew update
brew install postgresql@13

# Note:
If you need to have postgresql@13 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/postgresql@13/bin:$PATH"' >> /Users/tuyen.nguyen5/.bash_profile

For compilers to find postgresql@13 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/postgresql@13/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/postgresql@13/include"

# Start postgres foreground
/opt/homebrew/opt/postgresql@13/bin/postgres -D /opt/homebrew/var/postgresql@13

# Start postgres in background
brew services start postgresql

# Stop postgres
brew services stop postgresql

# Start PostgreSQL terminal (root privileges)
psql postgres

