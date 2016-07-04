Automatic Download Tracking
=====================================

Downloads (i.e. pdf, zip, doc files) can be tracked automatically without manually adding code to each download link.

Requirements for this are:

- files are linked directly (not via redirection or javascript)
- files are opened in a new browser window

Installation
------------

Upload wm_autotrack.min.js javascript file to the webserver and embed it to each page.

.. code-block:: html

    <script type="text/javascript" src="../dist/wm_autotrack.min.js"></script>

    <script>
        var wmAutoTrackObj = new wmAutoTrack({
              trackDownlodsWithPath: false
        });
        if (window.addEventListener) {
            window.addEventListener('load', wmAutoTrackObj.init, false);
        } else if (window.attachEvent) {
            window.attachEvent('onload', wmAutoTrackObj.init);
        }
    </script>

features of this script:

- automatic tracking of documents/files
- automatic tracking of outbound links
- automatic tracking of "mailto" links

milestones
------------

follwing milestones are set automatically (can be configured in the .js file):
- „Downloads“ - when a file/document ins clicked
- „E-Mail Angeklickt“ - when a mailto:// link is clicked

Please test the correct behavior with different browsers, to make sure tracking is working as expected.

Disclaimer
------------

As stated in the MIT license you should have received with this software:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

.. toctree::
   :maxdepth: 2
