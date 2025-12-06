import React from 'react';

// GitHub redesign example (single-file React component)
// Tailwind CSS utility classes assumed available.
// Uses shadcn/ui style imports as placeholders (optional).

export default function GitHubRedesign() {
  return (
    <div className="min-h-screen bg-slate-50 text-slate-900">
      {/* Top bar */}
      <header className="flex items-center justify-between px-6 py-3 bg-white shadow-sm">
        <div className="flex items-center gap-4">
          <div className="text-xl font-semibold">MyHub</div>
          <div className="hidden md:flex items-center gap-2 bg-slate-100 rounded-md p-1">
            <input
              className="bg-transparent outline-none px-2 py-1 text-sm"
              placeholder="Search or jump to..."
            />
            <button className="text-sm opacity-70">/</button>
          </div>
        </div>

        <nav className="flex items-center gap-4">
          <a className="hidden sm:inline-block text-sm hover:underline">Pull requests</a>
          <a className="hidden sm:inline-block text-sm hover:underline">Issues</a>
          <a className="hidden sm:inline-block text-sm hover:underline">Marketplace</a>
          <div className="flex items-center gap-2">
            <button className="px-3 py-1 text-sm rounded-md hover:bg-slate-100">New</button>
            <div className="w-8 h-8 rounded-full bg-gradient-to-br from-indigo-400 to-pink-400 flex items-center justify-center text-white font-medium">A</div>
          </div>
        </nav>
      </header>

      <main className="p-6 grid grid-cols-12 gap-6">
        {/* Sidebar */}
        <aside className="col-span-12 md:col-span-3 lg:col-span-2 bg-white rounded-lg shadow-sm p-4">
          <div className="flex items-center gap-3 mb-4">
            <div className="w-10 h-10 bg-slate-200 rounded-md"></div>
            <div>
              <div className="text-sm font-medium">octocat / hello-world</div>
              <div className="text-xs text-slate-500">Public • JavaScript</div>
            </div>
          </div>

          <nav className="flex flex-col gap-1 text-sm">
            <a className="px-3 py-2 rounded hover:bg-slate-50">Code</a>
            <a className="px-3 py-2 rounded hover:bg-slate-50">Issues</a>
            <a className="px-3 py-2 rounded hover:bg-slate-50">Pull requests</a>
            <a className="px-3 py-2 rounded hover:bg-slate-50">Actions</a>
            <a className="px-3 py-2 rounded hover:bg-slate-50">Projects</a>
            <a className="px-3 py-2 rounded hover:bg-slate-50">Wiki</a>
            <a className="px-3 py-2 rounded hover:bg-slate-50">Settings</a>
          </nav>

          <div className="mt-6 text-xs text-slate-500">
            <div>Branch: <span className="font-medium text-slate-700">main</span></div>
            <div className="mt-2">Last commit: <span className="font-medium">Fix README</span></div>
          </div>
        </aside>

        {/* Main content - file list + readme */}
        <section className="col-span-12 md:col-span-9 lg:col-span-7">
          <div className="bg-white rounded-lg shadow-sm p-4">
            <header className="flex items-center justify-between mb-4">
              <h1 className="text-lg font-semibold">Code</h1>
              <div className="flex items-center gap-2">
                <button className="px-3 py-1 text-sm rounded-md bg-slate-100">Add file</button>
                <button className="px-3 py-1 text-sm rounded-md bg-indigo-600 text-white">New pull request</button>
              </div>
            </header>

            <div className="border rounded-md overflow-hidden">
              <div className="flex items-center justify-between px-4 py-2 bg-slate-50 text-sm text-slate-600">
                <div>Path: /</div>
                <div>2 items</div>
              </div>

              <ul className="divide-y">
                <li className="flex items-center justify-between px-4 py-3">
                  <div className="flex items-center gap-3">
                    <div className="w-8 h-8 rounded-md bg-slate-100 flex items-center justify-center">📄</div>
                    <div>
                      <div className="font-medium">README.md</div>
                      <div className="text-xs text-slate-500">Updated 2 days ago</div>
                    </div>
                  </div>
                  <div className="text-xs text-slate-500">2 commits</div>
                </li>

                <li className="flex items-center justify-between px-4 py-3">
                  <div className="flex items-center gap-3">
                    <div className="w-8 h-8 rounded-md bg-slate-100 flex items-center justify-center">📁</div>
                    <div>
                      <div className="font-medium">src</div>
                      <div className="text-xs text-slate-500">JavaScript files</div>
                    </div>
                  </div>
                  <div className="text-xs text-slate-500">5 files</div>
                </li>
              </ul>
            </div>
          </div>

          <div className="mt-4 bg-white rounded-lg shadow-sm p-4">
            <h2 className="text-md font-semibold mb-2">README</h2>
            <article className="prose max-w-full">
              <p>This is a clean, focused README area. Use markdown rendering, support for images and badges.</p>
              <ul>
                <li>Quick start</li>
                <li>Usage</li>
                <li>Contributing</li>
              </ul>
            </article>
          </div>
        </section>

        {/* Right column - activity, commits, insights */}
        <aside className="col-span-12 lg:col-span-3">
          <div className="bg-white rounded-lg shadow-sm p-4 mb-4">
            <h3 className="font-semibold text-sm mb-2">Recent activity</h3>
            <ul className="text-sm text-slate-600">
              <li className="mb-2">@alice pushed to <span className="font-medium">main</span></li>
              <li className="mb-2">New issue #24 opened</li>
              <li className="mb-2">PR #5 merged</li>
            </ul>
          </div>

          <div className="bg-white rounded-lg shadow-sm p-4">
            <h3 className="font-semibold text-sm mb-2">Contributors</h3>
            <div className="flex -space-x-2">
              <div className="w-8 h-8 rounded-full border-2 border-white bg-slate-200" />
              <div className="w-8 h-8 rounded-full border-2 border-white bg-slate-200" />
              <div className="w-8 h-8 rounded-full border-2 border-white bg-slate-200" />
              <div className="w-8 h-8 rounded-full border-2 border-white bg-slate-200" />
            </div>
          </div>
        </aside>
      </main>

      <footer className="p-6 text-center text-xs text-slate-500">
        Designed prototype — adjust spacing, color tokens and interactions as needed.
      </footer>
    </div>
  );
}
