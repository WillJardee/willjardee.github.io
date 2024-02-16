---
title: 'Directions I Give Students When Writing Papers'
date: 2024-02-11
permalink: /posts/2024/01/writing-guide/
tags:
  - writing
  - humanities
---

As we gear up to submit the first project, I have collected common issues student's have had in previous years. These concepts are reflected in current machine learning research. To get a better grasp on how these expectations all come together to make a complete project, consider reading some recent research papers; however, note that many of these papers have issues and do not deliver on all our expectations. Each project can be seen as a lab you would run in physics or chemistry, and the final paper you submit is the lab report. This works for a computer science course because machine learning is a noisy, application based field, one where empirical tests align well with the problems and the attempted solution (this is very similar to have computer systems and applied algorithms research). Your version of setting up petri dishes, doing titrations, or shining a laser in the right place is setting up a well motivated, cross-validated experiment on datasets. When running your tests, writing your paper, recording your demo, and commenting your code, keep this in mind. What you provide must:
1. meet the writing conventions of the field,
2. be well formulated, motivated, and defendable,
3. be reproducible, assuming hardware and time is available, and
4. draw conclusions and state deficiencies of the experiments. 
How these concepts will be graded can be seen in the rubric attached to each assignment. Please make sure to read it completely, and reach out if you have questions. I also have documents of each rubric that can be cast into an accessible font (OpenDyslexic, Atkinson Hyperlegible,  etc.) if you need. Please email me if you need that service.


# Tips
These are tips for making your life easier. It may seem like more work initially, but these are skills you should learn/have already learned and it will be worth it; if only for the sake of learning.
1. Use latex. JMLR expects latex (and thus is friendly in formatting). Latex is a markup language, just like HTML or markdown, so don't be scared if you're new to it.
2. Use bibtex (or another compiler like biber) for any references! You should not write any of your references by hand. Notice that JMLR uses natbib by default to compile their references, which does not work with biber. So, if you try to run biber (i.e., I do most of my compiling with a call to biber <file name>) the JMLR style sheet will throw an error. Similarly, an error may arise if you use the package biblatex. See the latex references for examples.
3. Use some sort of spell/grammar checker (Grammarly, Writefull, etc.).
4. While writing, consider the story you wish to tell. This will also assist in scaffolding the structure of the paper and motivate post experiment analysis and conversation.
5. If you do use generative models/AI tools in brainstorming or for assistance, challenge yourself to find another source to backup what it is saying. i.e., I use these models for assisting me by asking "what theoretical concepts explain the Bellman Equation", and instead of asking the model for the explanations, I being searching the internet for reliable resources on the topics using my newfound vocabulary. For this reason, consider using models that provide you with references alongside responses (i.e., phind.com). NOTICE: READ THE SYLLABUS DIRECTIONS ON USE OF AI. THIS POINT IS TO ENSURE THAT IF SUCH TOOLS ARE USED, THEY DO NOT COMPROMISE THE FUNDAMENTAL LEARNING OBJECTIVES OF THE COURSE (CRITICAL AND SCIENTIFIC THINKING).
6. Use the rubber duck strategy (placing a rubber duck, or another object to explain to, in front of you and explaining the current bug/problem to it verbally) for both the coding and writing the paper. This promotes writing in such a way that better translates outside of your own mind.

Below, there is a deeper dive into common issues seem in the first assignment. Most of these points line up with the rubric.

# Paper
This goal of this paper is to present your work in such a way that emulates a research paper (or lab report). Consequentially, the expectations of structure and content are the same as a submitted paper.

1. Write in first person plural, specifically using the first person "we" instead of "I", "me", etc. This is the standard in the machine learning domain, and thus is expected.
2. Punctuate your math. Mathematics is a sentence component, and it needs to be treated as such. Read your sentences and replace your mathematical statement with other English statements. For example, if I were incorporating "x = 6" into a sentence, I would be thinking "_blah blah_ Tommy is a horse, _blah blah_", where x is now Tommy and 6 is a horse. Does the logical flow and grammar still make sense? Is this a run-on sentence? Does this sentence have enough 'beef' to mean it is worth keeping? Here are a couple structures that come up a lot:   
   1. end your mathematical expressions with a comma or a period (whichever is appropriate). This punctuation should be inline with the mathematical state; so, if you're using the `equation` environment, the punctuation should be before the `\end{equation}`.
   2. if your terms are not defined in the earlier in the paper, add a comma and continue the sentence with the mathematical statement defining the terms. For our example above: "... // x=6,  // where x is Tommy, and 6 is the number of a horse." Make sure you do not capitalize "where" (it is a continuation of the previous sentence) and define any mathematical expressions if it is not clear what it is; e.g. if you use $\odot$ for the pairwise product, state so as $\odot$ has many other uses.
3. The minimum length is 5 pages and max length is 10 pages. There is no title page. The title blurb, references, appendices, and, figures all count in the length. Writing concisely is an important challenge we often face, thus this is an opportunity to flex those muscles.
4. An abstract is expected. This abstract should include the general problem statement or purpose of the paper, a brief synopsis of your methods, and a sentence on your final conclusions. If I did not want to read 10 pages of your paper, what is everything I should take away? 
5. Your hypothesis should motivate your paper, and analysis done should be with the purpose of answering this question. Writing a hypothesis is a difficult skill you will need to learn. Ask if the hypothesis is large enough to be worth asking, but manageable enough to actually test. There must be some support before reaching the hypothesis to make it a reasonable idea to investigate. I can usually tell how a paper is going to be once I reach their hypothesis.
6. You are expected to do analysis and discussion beyond simply running the experiments. What did you do to better understand the method and the results you got? Common approaches are to do a convergence analysis (performance vs time), to probe the model in some way, such as for explainability, or to offer evidence on a dataset level of why model A performed well and model B did not. Make sure to consider this before starting your experiments so you can make sure to collect the information you need for the analysis.
7. Use proper JMLR style. The first few assignments lose a lot of points from petty mistakes. But, accuracy is important, especially when the tools are provided to you. I expect that you are using the jmlr2e.sty with latex. If you are using word, etc, if I can tell there is a difference, it is not excusable (and I have yet to find a word template that convinces me). There are plenty of JMLR examples out there, templates for overleaf, and I have written my own template on [compact latex](https://github.com/WillJardee/compact_latex). A few notable errors students usually have for the first two assignments are:
    - Use your department's address (or a fake address/no address, I don't quite care) for your address, not your personal address
    - Use an appropriate email for the email line, ensure it is an email you monitor, as this is going to be what I use if I need to contact you.
    - Check when you are importing jmlr2e.sty, if you do this at the wrong time certain rules can be overwritten and break styles, such as staggering left/right page justification like a book would. If it looks off, it probably is.
    - Pass the "preprint" option to the style sheet to remove editor and header fluff. Notice that older copies of jmlr2e.sty may not have this option.
    - Allow figures to float and refer to their figure numbers; this allows you to better use the space. All figures should be numbered and have a standalone caption that properly explains it.
    If you have any jmlr/tex issues, feel free to message me at wjardee1@jh.edu.
8. You are expected to do hyperparameter tuning in every assignment. I know that this is time consuming or seems goofy in some situations, but it is about the principle. You need to tell me the values you tuned, the range/set you used, method you used (grid, iterative, etc), and justify some of the these choices. "Tuning by hand" is only acceptable when you kept track of all the values you used and share that information (that being said, it is often a good place to start, giving an idea on the bounds of your search domain). If you find you do not have time to exhaustively tune every value, do a few values and state what you would have liked to have done if time permitted.
9. Organize your tables by dataset instead of by model. This allows you to compare different models across the same dataset, making analysis much easier. You should also carry your previous results between papers, as this puts your new values into perspective. 
10. If doing a time based analysis, consider how you are controlling for random variability. In general, wall-clock or cpu-clock time measurements are not acceptable, as they are wildly dependent on system wide states and advanced optimization techniques. It is much better to consider function evaluations, epochs, or direct computability calculations. However, consider how you will control measurements between algorithms, as the definition of epoch in one model may be vastly more costly than epoch in another. Wall-clock or cpu-clock measurements may be an acceptable validation of trends seen in these acceptable measures, but should considered with low reliability.
 
== Demo ==
1. I take the video requirements directly from the project outline. So, those are good direction to understand what your video will be graded on.
2. The purpose of the video is to convince me that your code runs and to teach you how to communicate what your code is doing.
3. I must see the code running (if it is a long process, this can be the beginning and end, but I need to see it successfully passes the compiling process and successfully finishes).
4. Do not walk through the code. Consider using a debugger or using print statements. Consider that I understand how these models all work and am looking for proof that your implementation works.
5. Statements like "Demonstrate" and "Show" can be easily accomplished by showing the before, starting of the machine, finishing of the machine, and the final output.
6. Be willing to re-record your video. It is by practice that you will be able to get these videos to fit within the time and effectively communicate your points. Consider using seeded runs and a todo list to provide consistency between takes.
7. There is about a 15 second buffer for the end of the video. If the video is longer than 5:15 (7:15 for the last video), I will stop watching at exactly 5 minutes (7 minutes) and consider the rest of the video as not submitted. 
8. If your video is less than 3 minutes, it is likely that you have not done a satisfactory job. Some students make it work, but double check your video covers all required topics before submitting.
9. If you are submitting a YouTube link, submit a text file with the link at the highest directory in your submission. I have missed students videos in the past when they are submitted in the comments of the submission, and that is a hassle neither of us want to deal with.


== Comments ==
1. Explain your algorithm alongside using javadoc, docstring, or the equivalent for your language.
2. Comment throughout the code. While there is some controversy along the lines of using verbose commenting as documentation, this course currently posits that documentation is done through comments and they are expected as such.

== Code ==
1. Do not submit notebook files. You can use them in writing code or doing analysis, and you are free to submit analysis/experiment runs in notebook format, but the final algorithm code must be in an appropriate, stand alone, format (.py, .c, etc). There is also a performance improvement when running code outside a notebook, so consider running code files directly instead of through a notebook. Rejecting notebook files encourages reusability. Exporting a notebook file to a .py does not satisfy this requirement. If you choose to do this, you must clean up the file for left over artifacts to make it easier to read.
2. Make navigation clear. If your model is buried three directories deep, you need to provide a README with directions to the important code. If I cannot find the model you are using for this assignment, I will deem it not submitted. 
3. Do not submit virtual environments or an abundance of log/experimentation files. This is a) bad practice and b) takes considerable time for my computer to download and unzip projects.
4. Remove purposeless blocks of code; putting them in comments does not solve this issue.

