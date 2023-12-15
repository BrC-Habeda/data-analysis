# A new way of looking at statistics.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Description

I have prepared a summary of new ways to look at data that will try and make it more like oil in the hopes that we will one day have a new appreciation of the oil rigs in the permian basin and the contribution of George P. Mitchell.

## Table of Contents

- [Definition](#Definition)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Definition

Statistics is a branch of mathematics that involves the **collection**, **analysis**, **interpretation, presentation**, and **organization** of data. It plays a crucial role in various fields, including science, business, economics, social sciences, and more.
The goal of statistics is to **extract meaningful information from data**, make inferences, and **support decision-making processes**.
We are going to focus on the extraction of "meaningful" information from data that supports the decision-making processes.

As trivial as it may be, defining meaningful information is a necessary step in understanding the misconceptions we have built (for good reason) thus far.

**Meaningful information** - information that _contributes to decision-making, problem-solving, or achieving specific goals_.

Descriptive statistics provide a summary of key aspects of a dataset, making it easier to understand and interpret. However, it's important to note that ease of understanding and interpretation do not allow for the generalization of findings to a larger population; for that purpose, another type of statistics is used.

Inferential statistics allows researchers and analysts to draw conclusions about populations based on sample data, taking into account the inherent uncertainty involved in the process. It plays a critical role in scientific research, decision-making, and data-driven strategies

The concept of meaningful information underscores the importance of data quality. It emphasizes the idea that _not all information is equally valuable, and the focus should be on acquiring, processing, and utilizing information that has real significance and utility in decision making and problem-solving_

Consider the following SQL query

```bash
SELECT students.student_id, students.name, students.class, SUM(marks.marks) AS total_marks
FROM students
INNER JOIN marks ON students.student_id = marks.student_id
WHERE students.year = 2023 AND students.class = 6
GROUP BY students.student_id, students.name
ORDER BY total_marks DESC;
```

If the objective of the school is to recognize and award the top performing student in class 6, then the 👆 query provides a solution to the problem; therefore it is meaningful

However, based on these results, we do not have sufficient evidence that the student with the most marks this year will have the same performance next year.

If our problem becomes "Lets find the aptitude of the class 6 students" then these results are meaningless in that context.
