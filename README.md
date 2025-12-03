<h2 align="center"> Hi, I'm Nadia </h2>


---


## Education

![Education](https://cardivo.vercel.app/api?name=SMKN%201%20Pedan&description=Major%3A%20Software%20and%20Game%20Development%20%28PPLG%29&image=https://github.com/ndianrhdyh/ndianrhdyh/raw/main/smkn1pedan.png&backgroundColor=%23ffffff&nameColor=%23000000&descriptionColor=%23000000&titleColor=%23000000&descColor=%23000000&theme=light)



## ━━ Most Used Languages ━━

import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { BarChart, Bar, XAxis, YAxis, Tooltip, ResponsiveContainer } from "recharts";
import { LayoutDashboard, FolderGit2, Code2, GitBranch } from "lucide-react";

const data = [
  { name: "HTML", value: 85 },
  { name: "CSS", value: 80 },
  { name: "JavaScript", value: 70 },
  { name: "PHP", value: 65 },
];

export default function Dashboard() {
  return (
    <div className="min-h-screen w-full bg-gray-950 text-white p-6">
      <header className="flex items-center gap-3 mb-10">
        <LayoutDashboard className="w-8 h-8" />
        <h1 className="text-3xl font-bold tracking-tight">Most Used Languages — Dashboard</h1>
      </header>

      <div className="grid grid-cols-1 md:grid-cols-3 gap-6 mb-10">
        <Card className="bg-gray-900 border-gray-800 shadow-xl">
          <CardContent className="p-6 flex items-center gap-4">
            <FolderGit2 className="w-10 h-10" />
            <div>
              <h2 className="text-lg font-semibold">Total Repositories</h2>
              <p className="text-3xl font-bold mt-1">27</p>
            </div>
          </CardContent>
        </Card>

        <Card className="bg-gray-900 border-gray-800 shadow-xl">
          <CardContent className="p-6 flex items-center gap-4">
            <Code2 className="w-10 h-10" />
            <div>
              <h2 className="text-lg font-semibold">Main Language</h2>
              <p className="text-3xl font-bold mt-1">JavaScript</p>
            </div>
          </CardContent>
        </Card>

        <Card className="bg-gray-900 border-gray-800 shadow-xl">
          <CardContent className="p-6 flex items-center gap-4">
            <GitBranch className="w-10 h-10" />
            <div>
              <h2 className="text-lg font-semibold">Active Projects</h2>
              <p className="text-3xl font-bold mt-1">6</p>
            </div>
          </CardContent>
        </Card>
      </div>

      <Card className="bg-gray-900 border-gray-800 shadow-xl p-6">
        <h2 className="text-xl font-semibold mb-4">Language Usage Chart</h2>
        <div className="w-full h-72">
          <ResponsiveContainer width="100%" height="100%">
            <BarChart data={data}>
              <XAxis dataKey="name" stroke="#fff" />
              <YAxis stroke="#fff" />
              <Tooltip cursor={{ opacity: 0.1 }} />
              <Bar dataKey="value" />
            </BarChart>
          </ResponsiveContainer>
        </div>
      </Card>
    </div>
  );
}





















