 </div>
<h2 id="modifying-an-active-pull-request-locally"><a aria-hidden="" tabindex="-1" class="doctocat-link" href="#modifying-an-active-pull-request-locally"><svg aria-hidden="" role="img" class="octicon-link" viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="display:inline-block;user-select:none;vertical-align:middle"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Modifying an active pull request locally</h2>
<div class="extended-markdown webui">
<ol>
<li>
<p>Under your repository name, click <svg version="1.1" width="16" height="16" viewBox="0 0 16 16" class="octicon octicon-git-pull-request" aria-label="The pull request icon" role="img"><path fill-rule="evenodd" d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5.628a2.251 2.251 0 101.5 0V5A2.5 2.5 0 0011 2.5zm1 10.25a.75.75 0 111.5 0 .75.75 0 01-1.5 0zM3.75 12a.75.75 0 100 1.5.75.75 0 000-1.5z"></path></svg> <strong>Pull requests</strong>.</p>
<p><span class="procedural-image-wrapper"><img src="/assets/cb-24580/images/help/repository/repo-tabs-pull-requests.png" alt="Issues and pull requests tab selection"></span></p>
</li>
<li>
<p>In the list of pull requests, click the pull request you'd like to modify.</p>
</li>
<li>
<p>To choose where you'd like to open the pull request, select the <strong>Open with <svg version="1.1" width="16" height="16" viewBox="0 0 16 16" class="octicon octicon-triangle-down" aria-label="The down triangle icon" role="img"><path d="M4.427 7.427l3.396 3.396a.25.25 0 00.354 0l3.396-3.396A.25.25 0 0011.396 7H4.604a.25.25 0 00-.177.427z"></path></svg></strong> drop-down and click one of the tabs.
<span class="procedural-image-wrapper"><img src="/assets/cb-9451/images/help/pull_requests/open-with-button.png" alt="Link to access command line pull request instructions"></span></p>
</li>
</ol>
</div>
<div class="extended-markdown cli">
<div class="extended-markdown note border rounded-1 mb-4 p-3 color-border-accent-emphasis color-bg-accent f5">
<p>To learn more about GitHub CLI, see "<a href="/en/github-cli/github-cli/about-github-cli">About GitHub CLI</a>."</p>
</div>
<p>To check out a pull request locally, use the <code>gh pr checkout</code> subcommand. Replace <code>pull-request</code> with the number, URL, or head branch of the pull request.</p>
<pre><code class="hljs language-shell">gh pr checkout <em>pull-request</em></code></pre>
</div>
<h2 id="modifying-an-inactive-pull-request-locally"><a aria-hidden="" tabindex="-1" class="doctocat-link" href="#modifying-an-inactive-pull-request-locally"><svg aria-hidden="" role="img" class="octicon-link" viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="display:inline-block;user-select:none;vertical-align:middle"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Modifying an inactive pull request locally</h2>
<p>If a pull request's author is unresponsive to requests or has deleted their fork, the pull request can still be merged. However, if you want to make changes to a pull request and the author is not responding, you'll need to perform some additional steps to update the pull request.</p>
<p>Once a pull request is opened, GitHub stores all of the changes remotely. In other words, commits in a pull request are available in a repository even before the pull request is merged. You can fetch an open pull request and recreate it as your own.</p>
<p>Anyone can work with a previously opened pull request to continue working on it, test it out, or even open a new pull request with additional changes. However, only collaborators with push access can merge pull requests.</p>
<ol>
<li>Under your repository name, click <svg version="1.1" width="16" height="16" viewBox="0 0 16 16" class="octicon octicon-issue-opened" aria-label="The issues icon" role="img"><path d="M8 9.5a1.5 1.5 0 100-3 1.5 1.5 0 000 3z"></path><path fill-rule="evenodd" d="M8 0a8 8 0 100 16A8 8 0 008 0zM1.5 8a6.5 6.5 0 1113 0 6.5 6.5 0 01-13 0z"></path></svg> <strong>Issues</strong> or <svg version="1.1" width="16" height="16" viewBox="0 0 16 16" class="octicon octicon-git-pull-request" aria-label="The pull request icon" role="img"><path fill-rule="evenodd" d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5.628a2.251 2.251 0 101.5 0V5A2.5 2.5 0 0011 2.5zm1 10.25a.75.75 0 111.5 0 .75.75 0 01-1.5 0zM3.75 12a.75.75 0 100 1.5.75.75 0 000-1.5z"></path></svg> <strong>Pull requests</strong>.
<span class="procedural-image-wrapper"><img src="/assets/cb-13785/images/help/repository/repo-settings-issues-pull-requests.png" alt="Issues and pull requests tab selection"></span></li>
<li>In the "Pull Requests" list, click the pull request you'd like to merge.</li>
<li>Find the ID number of the inactive pull request. This is the sequence of digits right after the pull request's title.
<span class="procedural-image-wrapper"><img src="/assets/cb-4458/images/help/pull_requests/pull_request_id_number.png" alt="Pull Requests ID number"></span></li>
<li>Open <span class="platform-mac">Terminal</span><span class="platform-linux">Terminal</span><span class="platform-windows">Git Bash</span>.</li>
<li>Fetch the reference to the pull request based on its ID number, creating a new branch in the process.
<pre><code class="hljs language-shell">$ git fetch origin pull/<em>ID</em>/head:<em>BRANCHNAME</em></code></pre>
</li>
<li>Switch to the new branch that's based on this pull request:
<pre><code class="hljs language-shell">[main] $ git checkout <em>BRANCHNAME</em>
> Switched to a new branch '<em>BRANCHNAME</em>'</code></pre>
</li>
<li>At this point, you can do anything you want with this branch. You can run some local tests, or merge other branches into the branch.</li>
<li>When you're ready, you can push the new branch up:
<pre><code class="hljs language-shell">[pull-inactive-pull-request] $ git push origin <em>BRANCHNAME</em>
> Counting objects: 32, done.
> Delta compression using up to 8 threads.
> Compressing objects: 100% (26/26), done.
> Writing objects: 100% (29/29), 74.94 KiB | 0 bytes/s, done.
> Total 29 (delta 8), reused 0 (delta 0)
> To https://github.com/<em>username</em>/<em>repository</em>.git
>  * [new branch]      <em>BRANCHNAME</em> -> <em>BRANCHNAME</em></code></pre>
</li>
<li><a href="/en/articles/creating-a-pull-request">Create a new pull request</a> with your new branch.</li>
</ol>
<h2 id="error-failed-to-push-some-refs"><a aria-hidden="" tabindex="-1" class="doctocat-link" href="#error-failed-to-push-some-refs"><svg aria-hidden="" role="img" class="octicon-link" viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="display:inline-block;user-select:none;vertical-align:middle"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Error: Failed to push some refs</h2>
<p>The remote <code>refs/pull/</code> namespace is <em>read-only</em>. If you try to push any commits there, you'll see this error:</p>
<pre><code class="hljs language-shell">! [remote rejected] HEAD -> refs/pull/1/head (deny updating a hidden ref)
error: failed to push some refs to 'git@github.local:<em>USERNAME</em>/<em>REPOSITORY</em>.git'</code></pre>
<div class="extended-markdown tip border rounded-1 mb-4 p-3 color-border-accent-emphasis color-bg-accent f5">
<p><strong>Tip:</strong> When you remove or rename a remote reference, your local <code>refs/pull/origin/</code> namespace will not be affected by calls to <code>git-remote</code>.</p>
</div></div></div></div></div></div></main><footer><section class="container-xl mt-lg-8 mt-6 px-3 px-md-6 no-print mx-auto"><div class="container-xl mx-auto py-6 py-lg-6 clearfix border-top border-color-secondary"><div class="col-12 col-lg-6 col-xl-3 mb-6 mb-xl-0 float-left pr-4"><form class="f5" data-testid="survey-form"><h2 class="f4 mb-3">
