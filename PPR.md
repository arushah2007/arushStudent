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
        Below are my <b>code segments</b> that meet the <b>AP CSP requirements</b>
    </p>
</section>

<!-- 🛠️ Procedure Section -->
<section style="background-color: #fff3cd; padding: 20px; border-left: 5px solid #ffc107; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #d39e00;">🛠️ Procedure</h2>

    <h3>📌 Requirement:</h3>
    <ul>
        <li>✔ Defines the <b>procedure name</b> and <b>return type</b> (if necessary).</li>
        <li>✔ Uses <b>one or more parameters</b> that affect functionality.</li>
        <li>✔ Implements <b>sequencing, selection, and iteration</b>.</li>
    </ul>

    <!-- i. Student-Developed Procedure -->
    <h3>💡 i. Student-Developed Procedure</h3>
    <p>The procedure below defines a method to add a class to a student's profile, ensuring no duplicates.</p>
    
    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="font-family: monospace; color: #f92672;">def</code> <code style="color: #a6e22e;">add_class</code>(self, class_name):
    <code style="color: #f92672;">if</code> class_name <code style="color: #f92672;">not in</code> self._classes:
        self._classes.append(class_name)
        db.session.commit()
        <code style="color: #f92672;">return</code> True
    <code style="color: #f92672;">return</code> False
    </pre>

    <p><b>📝 Explanation:</b> This function checks if a class already exists in the list before adding it, ensuring data integrity.</p>

    <!-- ii. Procedure Call in Program -->
    <h3>📞 ii. Procedure Call in Program</h3>
    <p>The procedure is called inside the <b>Profile API</b> when modifying a user’s profile.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="font-family: monospace; color: #f92672;">profile</code> = Profile.query.get(data['id'])
<code style="color: #f92672;">if</code> profile:
    profile.add_class(data['new_class'])
    </pre>

    <p><b>📌 Why This is Important?</b></p>
    <ul>
        <li>✔ Ensures <b>data integrity</b> by checking for duplicates.</li>
        <li>✔ Makes the code <b>modular and reusable</b>.</li>
    </ul>
</section>

<!-- 📋 Lists Section -->
<section style="background-color: #fbe9e7; padding: 20px; border-left: 5px solid #e53935; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #b71c1c;">📋 Lists</h2>

    <h3>📌 Requirement:</h3>
    <ul>
        <li>✔ First Code Segment: Shows how data is stored in the list.</li>
        <li>✔ Second Code Segment: Shows how the list data is accessed and used.</li>
    </ul>

    <!-- i. Storing Data in a List -->
    <h3>📂 i. Storing Data in a List</h3>
    <p>This code segment initializes a student profile and stores multiple classes in a list.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="font-family: monospace; color: #f92672;">p1</code> = Profile(name='Arush Shah', classes=['Math', 'Science', 'History'],
             favorite_class='Science', grade='A')
p1.create()
    </pre>

    <p><b>📝 Explanation:</b> The list stores multiple class names inside a 'Profile' object and persists it in the database.</p>

    <!-- ii. Using Data from the List -->
    <h3>📊 ii. Using Data from the List</h3>
    <p>This function retrieves stored classes and formats them for easy display.</p>

    <pre style="background-color: #272822; color: #f8f8f2; padding: 15px; border-radius: 8px; overflow-x: auto;">
<code style="font-family: monospace; color: #f92672;">def</code> read(self):
    <code style="color: #f92672;">return</code> {
        'id': self.id,
        'name': self.name,
        'classes': self.classes,
        'favorite_class': self.favorite_class,
        'grade': self.grade,
    }
    </pre>

    <p><b>📝 Explanation:</b> This function dynamically accesses the stored list and returns it in a structured format.</p>
</section>

<!-- 🌟 Summary & Takeaways -->
<section style="background-color: #ede7f6; padding: 15px; border-left: 5px solid #673ab7; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #4527a0;">🌟 Summary & Takeaways</h2>
    <ul>
        <li>✅ Implemented a <b>student-developed procedure</b> with sequencing, selection, and iteration.</li>
        <li>✅ Used <b>lists to manage complexity</b> by storing and retrieving multiple class values.</li>
        <li>✅ Ensured <b>modular and efficient</b> programming with reusable functions.</li>
    </ul>
</section>





<!-- 📜 CPT Requirements Table -->
<section style="background-color: #f1f8e9; padding: 20px; border-left: 5px solid #7cb342; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #558b2f;">📜 CPT Requirements</h2>

    <table style="width: 100%; border-collapse: collapse; background-color: #ffffff; border-radius: 8px; overflow: hidden; box-shadow: 2px 2px 10px rgba(0,0,0,0.1);">
        <tr style="background-color: #8bc34a; color: #ffffff;">
            <th style="padding: 12px; text-align: left;">📝 Concept</th>
            <th style="padding: 12px; text-align: left;">💡 How My Code Implements It</th>
        </tr>
        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 List</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                Stores multiple classes in a list inside a <code>Profile</code> object, allowing efficient retrieval and modification of user data.
                This ensures scalability, as new classes can be added or removed dynamically without modifying the entire data structure.
            </td>
        </tr>
        <tr style="background-color: #f9fbe7;">
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 Sequencing</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                Executes steps in a logical order—first checking if a class already exists, then modifying the list, and finally saving changes to the database.
                This structured flow ensures that data consistency is maintained and that unintended duplicates do not occur.
            </td>
        </tr>
        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 Selection</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                Uses <code>if class_name not in self._classes</code> to determine whether to add a class to the list.
                This decision-making process prevents redundancy and ensures that only new, relevant data is stored in the user's profile.
            </td>
        </tr>
        <tr style="background-color: #f9fbe7;">
            <td style="padding: 10px;">📌 Iteration</td>
            <td style="padding: 10px;">
                The list is modified dynamically over time, interacting with API calls to update the stored data when users modify their class selections.
                This approach allows for seamless integration with user actions, ensuring real-time updates in the system.
            </td>
        </tr>
    </table>
</section>



<div>






</div>



<!-- 📊 AP CSP MCQ Performance -->
<section style="background-color: #f1f8e9; padding: 20px; border-left: 5px solid #7cb342; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #558b2f;">🧠 AP CSP MCQ Performance & Improvement Plan</h2>

    <p>
        I recently took an <b>AP CSP Multiple-Choice Quiz</b> on AP Classroom and scored <b>46/67</b>. Below is my performance breakdown across different 
        <b>Big Ideas</b> and <b>Skills</b>, and how I can improve. 📈
    </p>
</section>

<!-- 🌎 Performance by Big Idea -->
<section style="background-color: #e3f2fd; padding: 20px; border-left: 5px solid #1e88e5; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #1565c0;">🌎 Performance by Big Idea</h2>

    <table style="width: 100%; border-collapse: collapse; background-color: #ffffff; border-radius: 8px; overflow: hidden; box-shadow: 2px 2px 10px rgba(0,0,0,0.1);">
        <tr style="background-color: #64b5f6; color: #ffffff;">
            <th style="padding: 12px; text-align: left;">📌 Big Idea</th>
            <th style="padding: 12px; text-align: center;">📝 Number of Questions</th>
            <th style="padding: 12px; text-align: center;">📊 Average Performance %</th>
        </tr>
        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 AAP: Algorithms and Programming</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">38</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">66%</td>
        </tr>
        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 CRD: Creative Development</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">9</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">78%</td>
        </tr>
        <tr style="background-color: #f1f8e9;">
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 CSN: Computing Systems & Networks</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">6</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;"><b>100%</b> ✅</td>
        </tr>
        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">📌 DAT: Data</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">13</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;"><b>62%</b> ❗</td>
        </tr>
        <tr>
            <td style="padding: 10px;">📌 IOC: Impact of Computing</td>
            <td style="padding: 10px; text-align: center;">9</td>
            <td style="padding: 10px; text-align: center;">67%</td>
        </tr>
    </table>
</section>

<!-- 🏆 Performance by Skill Type -->
<section style="background-color: #fff3cd; padding: 20px; border-left: 5px solid #ffc107; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #d39e00;">🏆 Performance by Skill Type</h2>

    <table style="width: 100%; border-collapse: collapse; background-color: #ffffff; border-radius: 8px; overflow: hidden; box-shadow: 2px 2px 10px rgba(0,0,0,0.1);">
        <tr style="background-color: #ffa726; color: #ffffff;">
            <th style="padding: 12px; text-align: left;">📌 Skill</th>
            <th style="padding: 12px; text-align: center;">📝 Number of Questions</th>
            <th style="padding: 12px; text-align: center;">📊 Average Performance %</th>
        </tr>

        <tr style="background-color: #c8e6c9;">
            <td style="padding: 10px;">Skill 1.A: Investigate the situation</td>
            <td style="padding: 10px; text-align: center;">2</td>
            <td style="padding: 10px; text-align: center;">100% ✅</td>
        </tr>

        <tr style="background-color: #c8e6c9;">
            <td style="padding: 10px;">Skill 1.B: Design an approach to achieve the purpose</td>
            <td style="padding: 10px; text-align: center;">1</td>
            <td style="padding: 10px; text-align: center;">100% ✅</td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px;">Skill 1.C: Explain how collaboration affects a solution</td>
            <td style="padding: 10px; text-align: center;">2</td>
            <td style="padding: 10px; text-align: center;"><b>50%</b> ❗</td>
        </tr>

        <tr style="background-color: #f1f8e9;">
            <td style="padding: 10px;">Skill 1.D: Evaluate solution options</td>
            <td style="padding: 10px; text-align: center;">12</td>
            <td style="padding: 10px; text-align: center;">75%</td>
        </tr>

        <tr style="background-color: #c8e6c9;">
            <td style="padding: 10px;">Skill 2.A: Represent algorithmic processes</td>
            <td style="padding: 10px; text-align: center;">2</td>
            <td style="padding: 10px; text-align: center;">100% ✅</td>
        </tr>

        <tr>
            <td style="padding: 10px;">Skill 2.B: Implement and apply an algorithm</td>
            <td style="padding: 10px; text-align: center;">11</td>
            <td style="padding: 10px; text-align: center;">82%</td>
        </tr>

        <tr style="background-color: #e0e0e0;">
            <td style="padding: 10px;">Skill 3.A: Generalize data sources through variables</td>
            <td style="padding: 10px; text-align: center;">0</td>
            <td style="padding: 10px; text-align: center;">NA</td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px;">Skill 3.B: Use abstraction to manage complexity</td>
            <td style="padding: 10px; text-align: center;">5</td>
            <td style="padding: 10px; text-align: center;"><b>40%</b> ❗</td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px;">Skill 3.C: Explain how abstraction manages complexity</td>
            <td style="padding: 10px; text-align: center;">2</td>
            <td style="padding: 10px; text-align: center;"><b>50%</b> ❗</td>
        </tr>

        <tr style="background-color: #e0e0e0;">
            <td style="padding: 10px;">Skill 4.A: Explain how a code segment functions</td>
            <td style="padding: 10px; text-align: center;">0</td>
            <td style="padding: 10px; text-align: center;">NA</td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px;">Skill 4.B: Determine the result of code segments</td>
            <td style="padding: 10px; text-align: center;">5</td>
            <td style="padding: 10px; text-align: center;"><b>20%</b> ❗</td>
        </tr>

        <tr>
            <td style="padding: 10px;">Skill 4.C: Identify and correct errors in algorithms</td>
            <td style="padding: 10px; text-align: center;">7</td>
            <td style="padding: 10px; text-align: center;">71%</td>
        </tr>

        <tr style="background-color: #c8e6c9;">
            <td style="padding: 10px;">Skill 5.A: Explain how computing systems work</td>
            <td style="padding: 10px; text-align: center;">4</td>
            <td style="padding: 10px; text-align: center;">100% ✅</td>
        </tr>

        <tr>
            <td style="padding: 10px;">Skill 5.B: Explain how knowledge can be generated from data</td>
            <td style="padding: 10px; text-align: center;">7</td>
            <td style="padding: 10px; text-align: center;">57%</td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px;">Skill 5.C: Describe the impact of a computing innovation</td>
            <td style="padding: 10px; text-align: center;">1</td>
            <td style="padding: 10px; text-align: center;"><b>0%</b> ❗</td>
        </tr>

        <tr style="background-color: #c8e6c9;">
            <td style="padding: 10px;">Skill 5.D: Describe the impact of gathering data</td>
            <td style="padding: 10px; text-align: center;">2</td>
            <td style="padding: 10px; text-align: center;">100% ✅</td>
        </tr>

        <tr>
            <td style="padding: 10px;">Skill 5.E: Evaluate the use of computing based on legal and ethical factors</td>
            <td style="padding: 10px; text-align: center;">4</td>
            <td style="padding: 10px; text-align: center;">75%</td>
        </tr>

    </table>
</section>


<!-- 📉 Review & Improvement Plan -->
<section style="background-color: #ffebee; padding: 20px; border-left: 5px solid #d32f2f; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #b71c1c;">📉 Skill Review & How to Improve</h2>

    <p>
        After analyzing my performance, I identified <b>three key areas</b> where I struggled the most. Below is a breakdown of these skills and how I plan to improve.
    </p>

    <h3>❗ 1. Skill 4.B: Determine the result of code segments (20%)</h3>
    <p>
        <b>Problem:</b> I struggled with predicting outputs of code snippets, especially involving loops, conditionals, and recursion.<br>
        <b>Improvement Plan:</b>  
        - Practice <b>tracing code line-by-line</b> to mentally execute logic before answering.  
        - Solve more <b>AP-style code tracing problems</b> to reinforce pattern recognition.  
        - Use <b>Python or JavaScript</b> to run snippets and compare expected vs. actual outputs.
    </p>

    <h3>❗ 2. Skill 3.B: Use abstraction to manage complexity (40%)</h3>
    <p>
        <b>Problem:</b> I had difficulty understanding how abstraction helps in organizing code efficiently.<br>
        <b>Improvement Plan:</b>  
        - Study examples of <b>modular programming</b> (e.g., breaking down large problems into functions).  
        - Practice writing <b>functions that generalize repetitive tasks</b>.  
        - Look at <b>AP CSP reference sheet</b> to see how abstraction is tested.
    </p>

    <h3>❗ 3. Skill 5.C: Describe the impact of a computing innovation (0%)</h3>
    <p>
        <b>Problem:</b> I wasn’t able to fully analyze real-world computing innovations and their effects on society.<br>
        <b>Improvement Plan:</b>  
        - Read about <b>recent technological innovations</b> (AI, blockchain, cybersecurity).  
        - Study how <b>computing affects privacy, security, and ethics</b>.  
        - Practice writing <b>short explanations</b> about how innovations impact industries.
    </p>

    <p>By focusing on these areas, I can significantly improve my performance for the AP CSP exam. 🚀</p>
</section>

<!-- ❌ Mistakes & Explanations Table -->
<section style="background-color: #ffebee; padding: 20px; border-left: 5px solid #d32f2f; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #b71c1c;">❌ Mistakes & Explanations Of My Hardest Questions</h2>

    <table style="width: 100%; border-collapse: collapse; background-color: #ffffff; border-radius: 8px; overflow: hidden; box-shadow: 2px 2px 10px rgba(0,0,0,0.1);">
        <tr style="background-color: #e57373; color: #ffffff;">
            <th style="padding: 12px; text-align: left;">❓ Question</th>
            <th style="padding: 12px; text-align: center;">❌ My Answer</th>
            <th style="padding: 12px; text-align: center;">✅ Correct Answer</th>
            <th style="padding: 12px; text-align: left;">💡 Explanation</th>
        </tr>

        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Q65: Calls to concat and substring</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">B, D</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">B, C</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                The correct segments correctly concatenate and extract substrings to form "jackalope". My mistake was choosing option D instead of C.
            </td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Q60: Number of elements in one list but not both</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">D</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">A</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                The logic incorrectly calculates the unique count. The correct method properly differentiates between unique and overlapping elements.
            </td>
        </tr>

        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Q41: TrimLeft and TrimRight</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">B</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">C</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                The correct sequence removes the rightmost characters first, then the leftmost, preserving the desired description.
            </td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Q37: DrawLine on a coordinate grid</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">C</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">A</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                The loop systematically reduces the y-coordinates, making A the correct choice for the drawn lines.
            </td>
        </tr>

        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Q30: Which value cannot be displayed in selection</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">C</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">D</td>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">
                The condition ensures that "out of range" is never displayed, making D the only correct answer.
            </td>
        </tr>

        <tr style="background-color: #fbe9e7;">
            <td style="padding: 10px;">Q28: Swap alpha and beta</td>
            <td style="padding: 10px; text-align: center;">D</td>
            <td style="padding: 10px; text-align: center;">B</td>
            <td style="padding: 10px;">
                The correct segment follows the correct swapping logic using a temporary variable, while option D does not preserve both values.
            </td>
        </tr>

    </table>
</section>



<!-- ⏳ Time Analysis Table -->
<section style="background-color: #e3f2fd; padding: 20px; border-left: 5px solid #1e88e5; border-radius: 8px; margin-top: 20px;">
    <h2 style="color: #1565c0;">⏳ Time Analysis</h2>

    <table style="width: 100%; border-collapse: collapse; background-color: #ffffff; border-radius: 8px; overflow: hidden; box-shadow: 2px 2px 10px rgba(0,0,0,0.1);">
        <tr style="background-color: #64b5f6; color: #ffffff;">
            <th style="padding: 12px; text-align: left;">📝 Metric</th>
            <th style="padding: 12px; text-align: center;">⏳ Time</th>
        </tr>
        <tr>
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Total Time Spent</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">2 hours, 58 minutes, 28 seconds</td>
        </tr>
        <tr style="background-color: #f1f8e9;">
            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Average Time per Question</td>
            <td style="padding: 10px; text-align: center; border-bottom: 1px solid #ddd;">~2 minutes 40 seconds</td>
        </tr>
    </table>
</section>
