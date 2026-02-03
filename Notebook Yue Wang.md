# Jan 21

Tested feasibility of PokeApi, was able to retrieve data for single Pokémon using standard REST API request, had coding errors when trying to retrieve data for all Pokémon. Did not commit broken code.

# Jan 22
Saw feedback from a bunch of groups, our API was not being done by classmate but already had existing wrapper so we decided to focus more on analysis. Did some light research into free AI APIs to use, as we had integrated a local AI into our 533 project and wanted to do something similar.

# Jan 24
Google’s Gemini API is free, while most of the other popular ones like Grok or ChatGPT seemed to be paid only. Decided to try using Google’s Gemini API to save costs, and daily limits are reasonable and instead of overcharging users like AWS, the free key simply stops working if limit hit.

# Jan 25
Wrote some basic test code for Gemini AI API, to check that key worked and could get a simple response back. Initially tried gemini.R library to help, but that constantly caused 404 errors. After much testing discovered that the model in gemini.R is hardcoded, and outdated, causing errors. Decided to not use any library and simply use standard REST API request directly to Google. Confirmed key worked and could make REST API calls to Google Gemini 2.5. Code not committed yet.

# Jan 29
Proposal accepted, recommended we also add UI elements to the project to make it easier for users to use. Looked into UI libraries, standard seems to be Shiny. Made a quick POC of the UI with Shiny, also added the Gemini code that was tested before, in this commit https://github.com/yueywangse/PokemonAnalyzer/commit/c5986eb7b9f3bdc5401400331e05f36e7f57c2d8 and then fixed some errors I noticed later https://github.com/yueywangse/PokemonAnalyzer/commit/08a27cbf3eecf9192df419bd517a59a2324b1511. 

# Jan 30
Needed the code to link Pokémon names to id numbers from another member, so did some light research into CRAN submission, R package best practice, unit testing etc.

# Feb 1
Met up with team members to work out the R wrapper today. Functions I was waiting on were ready so spent some time rewriting some of the GUI code to integrate new functions, made a new helper function to grab Pokémon pictures off a URL using the ID number, added logic to like suggestions with UI here https://github.com/yueywangse/PokemonAnalyzer/commit/d47424042a7f2459f22c7aa0afec86904e5e79ac. 

Worked on initial documentation, and CI (GitHub Action) was integrated at this point as well so also worked on getting the tests and documentation ready enough to pass CI in this pr https://github.com/yueywangse/PokemonAnalyzer/commit/6b916b83be9f5b62a74dfaa94a3bf6044c5b1031.

Updated comments as well on GUI code in this commit https://github.com/yueywangse/PokemonAnalyzer/commit/a6908e5709e91f54097513d8bb769e1756f2d690.

# Feb 2
Looked up best practices for CRAN libraries, especially the part concerning GUI. Rewrote GUI code so that it no longer launches the GUI by itself and instead has the necessary parameters in an easy to access function, and made a test.R file in the main directory to easily access GUI for testing in this commit https://github.com/yueywangse/PokemonAnalyzer/commit/cb8e3a42800e37b8645a35816fcd6da023cba929.

Spent some time assisting in reviewing and testing commits to correct parts of the wrapper, suggested merging all functions into the R folder and keeping minimum code outside for general usage testing/presentation prep. Helped make sure other PRs did not break code.

Worked on the GUI/Gemini sections of the presentation.

Waited for all members to sign off on the code, checked package build requirements were met, fixed some of the missing build parameters https://github.com/yueywangse/PokemonAnalyzer/commit/bcaf9254cfd559d2fc6e470856bb26d0b37198c3. 

Received submission acknowledgement from CRAN, posted screenshot to presentation.