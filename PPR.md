---
layout: page
title: 
description: Home page
hide: true
---


<!-- 🎯 AP CSP Personalized Project Reference (PPR) FRQ -->
<section style="background-color: #e3f2fd; padding: 20px; border-left: 5px solid #1e88e5; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #1565c0;">🚀 AP CSP Personalized Project Reference (PPR) FRQ</h2>
    <p>
        Below are my <b>code segments</b> that meet the <b>AP CSP requirements</b>.
    </p>
</section>

<!-- 📌 Summary -->
<section style="background-color: #fff3cd; padding: 15px; border-left: 5px solid #ffc107; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #d39e00;">📌 Summary</h2>
    <ul>
        <li>✔ <b>List Creation:</b> Initializes and stores student class data.</li>
        <li>✔ <b>List Processing:</b> Retrieves and processes stored class data.</li>
        <li>✔ <b>Function with Sequencing, Selection, and Iteration:</b> A function that iterates over a list, applies conditional logic, and processes data.</li>
        <li>✔ <b>Call to Function:</b> A function call that modifies a user’s profile dynamically.</li>
    </ul>
</section>

<!-- 📂 List Creation -->
<section style="background-color: #e8f5e9; padding: 20px; border-left: 5px solid #43a047; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #2e7d32;">📂 List Creation</h2>
    <p>This segment initializes student profiles and creates a list of classes.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="color: #f92672;">p1</code> = Profile(name=<span style="color:#e6db74;">"Arush Shah"</span>, classes=[<span style="color:#e6db74;">"Math"</span>, <span style="color:#e6db74;">"Science"</span>, <span style="color:#e6db74;">"History"</span>], 
             favorite_class=<span style="color:#e6db74;">"Science"</span>, grade=<span style="color:#e6db74;">"A"</span>)
p2 = Profile(name=<span style="color:#e6db74;">"Jackson Patrick"</span>, classes=[<span style="color:#e6db74;">"Art"</span>, <span style="color:#e6db74;">"Music"</span>, <span style="color:#e6db74;">"Literature"</span>], 
             favorite_class=<span style="color:#e6db74;">"Art"</span>, grade=<span style="color:#e6db74;">"A+"</span>)
p3 = Profile(name=<span style="color:#e6db74;">"Armaghan Zarak"</span>, classes=[<span style="color:#e6db74;">"Computer Science"</span>, <span style="color:#e6db74;">"Physics"</span>, <span style="color:#e6db74;">"Biology"</span>], 
             favorite_class=<span style="color:#e6db74;">"Computer Science"</span>, grade=<span style="color:#e6db74;">"B+"</span>)

p1.create()
p2.create()
p3.create()
    </pre>

    <p><b>📝 Explanation:</b> This code initializes multiple student profiles and assigns them lists of classes. The <b>.create()</b> method ensures that each profile is stored in the database.</p>
</section>

<!-- 🔄 List Processing -->
<section style="background-color: #fbe9e7; padding: 20px; border-left: 5px solid #e53935; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #b71c1c;">🔄 List Processing</h2>
    <p>This function retrieves all stored profiles and processes their class lists.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="color:#a6e22e;">def</code> get(self):
    <code style="color:#f92672;">try:</code>
        profiles = Profile.query.all()
        <code style="color:#f92672;">return</code> jsonify([profile.read() <code style="color:#f92672;">for</code> profile <code style="color:#f92672;">in</code> profiles])
    <code style="color:#f92672;">except</code> Exception as e:
        <code style="color:#f92672;">return</code> {<span style="color:#e6db74;">'message'</span>: f<span style="color:#e6db74;">"An error occurred: {str(e)}"</span>}, 500
    </pre>

    <p><b>📝 Explanation:</b> This function retrieves all profiles from the database and converts them into JSON format using <b>profile.read()</b>. This allows the list of classes to be accessed dynamically.</p>
</section>

<!-- 🛠️ Function with Sequencing, Selection & Iteration -->
<section style="background-color: #fff3cd; padding: 20px; border-left: 5px solid #ff9800; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #ef6c00;">🛠️ Function with Sequencing, Selection & Iteration</h2>
    <p>This function modifies a student’s class list by iterating over it and applying conditional logic.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="color:#a6e22e;">def</code> update_classes(self, new_classes):
    <code style="color:#f92672;">for</code> class_name <code style="color:#f92672;">in</code> new_classes:
        <code style="color:#f92672;">if</code> class_name <code style="color:#f92672;">not in</code> self._classes:
            self._classes.append(class_name)
    db.session.commit()
    <code style="color:#f92672;">return</code> self._classes
    </pre>

    <h3>📌 Explanation of Key Concepts:</h3>
    <ul>
        <li><b>✔ Sequencing:</b> The function follows a structured process, first iterating through the new classes, checking conditions, and then modifying the list before saving to the database.</li>
        <li><b>✔ Selection:</b> The <b>if</b> statement ensures that only new classes are added, preventing duplicate entries.</li>
        <li><b>✔ Iteration:</b> The <b>for</b> loop iterates over the list of new classes and processes them dynamically.</li>
    </ul>
</section>

<!-- 📞 Call to Function -->
<section style="background-color: #e3f2fd; padding: 20px; border-left: 5px solid #1e88e5; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #1565c0;">📞 Call to Function</h2>
    <p>This function call updates a student's class list dynamically.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="color:#f92672;">profile</code> = Profile.query.get(data[<span style="color:#e6db74;">'id'</span>])
<code style="color:#f92672;">if</code> profile:
    profile.update_classes(data[<span style="color:#e6db74;">'new_classes'</span>])
    </pre>

    <p><b>📝 Explanation:</b> This retrieves a student profile by ID and updates their class list with new classes. The function ensures that only missing classes are added.</p>
</section>






<script src="https://utteranc.es/client.js"
        repo="arushah2007/arushStudent"
        issue-term="pathname"
        theme="github-dark"
        crossorigin="anonymous"
        async>
    </script> 
