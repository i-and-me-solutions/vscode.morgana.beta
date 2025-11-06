# Morgana IBM i Outline and more for Visual Studio Code

Welcome to **Morgana IBM i Outline**, a project by a dedicated team with the goal of making life easier for IBM i developers and saving them more and more time in their daily work.
RPG development has long been tied to legacy workflows, and we believe it’s time for a change. Morgana is a Visual Studio Code extension designed to make working with RPG code more intuitive, efficient, and enjoyable. Whether you’re maintaining fixed-format RPG or preparing for mixed and free-format RPG, Morgana is here to support you every step of the way.

## 🛠️ Using Morgana Outline

Morgana Outline is designed to simplify your RPG development workflow. Here's how you can get started:

1. **Open an RPGLE or SQLRPGLE File**: Simply open any RPGLE or SQLRPGLE file in Visual Studio Code.
2. **View the Outline**: The Morgana Outline will automatically appear in the Explorer section of the Activity Bar, providing a structured overview of your code. If you have the "Code for IBM i" extension open, you may need to switch to the Explorer view in the Activity Bar to access the Morgana Outline. You can also drag the Morgana Outline to any other view you prefer. For example, feel free to move it to the "Code for IBM i" section if that fits your workflow better.
3. **Navigate Your Code**: Use the outline to quickly jump to fields, subroutines, procedures, and other key elements in your code.

With Morgana Outline, navigating complex RPG programs has never been easier!

## 🌟 Why Morgana?

RPG development doesn’t have to be stuck in the past. Morgana is here to:

- **Simplify Your Workflow**: With a structured outline view, you’ll always have a clear overview of your RPGLE and SQLRPGLE files.
- **Focus on Fixed-Format RPG (For Now)**: Our current focus is on fixed-format RPG, but we’re actively working on adding support for hybrid (mixed-format) and free-format RPG, as well as CL/CLLE. These enhancements are part of our roadmap.
- **RPG-II, OCL, RPG-III and Cobol**: Could be also added if you want it. Please tell us, if there is a need and we will add this to our roadmap.
- **Boost Your Productivity**: Quickly navigate large programs, jump to definitions, and resolve file issues with ease.
- **Enhanced Outline Features**: In the first step we added a GOTO Marker, as well as the very effective Feature that opens any Source Code which is related to your program, like CALLed Programs or Subprocedures.
- **Integrate Seamlessly**: Morgana works alongside the [Code for IBM i](https://marketplace.visualstudio.com/items?itemName=HalcyonTechLtd.code-for-ibmi) extension, ensuring a smooth development experience.

## 📝 What is MORGANA Outline?

MORGANA Outline is an IBM i Outline for Visual Studio Code that looks very similar to the one you already know from other IBM i editors but with significantly expanded functionality.

## ❓ Why not use the VS Code Outline?

The VS Code outline was developed for all possible programming languages, but as we all know, column-oriented or fixed-format RPG is unique in the programming world. Also, old RPG programs were often not developed modularly, while the features included in VS Code are strongly geared towards modular development. This means that the functionality integrated into VS Code is also suitable for very modern, totally free RPGs that are modularized.

## ⚙️ How does MORGANA Outline work?

Unlike other tools that support an IBM i outline function, MORGANA Outline retrieves it's information not only from the compile List and (File) Objects but also directly from the source code. To do this, the source code is first divided into so-called tokens using a special parser. We originally developed this functionality purely for our AI-based analysis tools, but then realized that it could be used wonderfully as an outline in VS Code. In addition to the pure source code that is open, Morgana also accesses sources used in RPG, such as display files, printer files, database files as well as Subprocedures in Modules/Service Programs or CALLs.

## 📂 Which languages / source types does Beta 1 support?

MORGANA Outline was originally developed specifically for older and more complex RPG applications and, in Beta 1, exclusively supports column RPG in ILE format (RPG IV). Since the IBM command CVTRPGSRC makes it very easy to convert RPG-III and RPG/400 source code into ILE code, we always take this approach with our customers and do not intend to support RPG-III or RPG/400 directly unless there is demand for it. We also convert RPG-II and OCL source code into ILE RPG and ILE CL internally using a special tool. If you are interested in this, please contact us.

## 🔮 Which languages / source types will be supported next?

In the next step, we will support ILE-based Hybrid RPG and (total) Free RPG. In addition, embedded SQL in RPG will be supported for the above variants. This will be followed by CL / CLLE. RPG-II, OCL, RPG-III, Cobol and ILE Cobol developers, please contact us.

## 🚀 Which Features does Beta 1 provide?

Beta 1 supports:

- **Field Recognition**: Identify where a field is defined, used, and modified, including fields defined within the C specification.
- **Screen File Record Formats**: Recognize record formats in screen files, including fields defined therein and their usage. Directly open the source code with a simple mouse click.
- **Print File Record Formats**: Recognize record formats in print files, including fields defined therein and their usage. Directly open the source code with a simple mouse click.
- **Database File Record Formats**: Recognize record formats in database files, including fields defined therein and their usage. Directly open the source code with a simple mouse click.
- **Data Structures**: Recognize data structures and their subfields, including their usage.
- **Arrays**: Recognize arrays and their usage.
- **Subroutines**: Recognize subroutines and their usage.
- **Subprocedures**: Recognize subprocedures and their usage.
- **Indicators**: Recognize indicators and their usage. Morgana also recognizes MOVEA changes to *IN()!
- **Key Lists (KLIST)**: Recognize key lists, including the fields used therein.
- **Parameter Lists (PLIST)**: Recognize parameter lists, including the fields used therein.
- **Subprocedure Navigation**: Directly open the source code of a subprocedure with a simple mouse click based on the library list and binding directories.
- **Program CALLs**: Recognize CALLs to programs and directly open the source code of a called program with a simple mouse click.
- **GOTO Marker Function**: Highlight TAGs and GOTOs to specific TAGs in the same color in the MORGANA Outline header. This function helps when scrolling through code extensively. For specific GOTOs to a TAG, you can also use the Outline function itself.

## 🌟 Our Vision

Our goal is to provide IBM i developers with modern tools that make their work more efficient and enjoyable. With Morgana, we aim to:

- Make RPG development accessible and intuitive for both legacy and modern codebases.
- Empower developers to confidently work with RPG code.
- Build a community of RPG enthusiasts who share ideas and collaborate on improving the development experience.

## 🔧 What’s Next?

We’re committed to continuous improvement. Here’s what’s on our roadmap:

- **Hybrid RPG and (total) free RPG Support**: Expanding Morgana’s capabilities to handle modern RPG code styles.
- **Embedded SQL RPG**: In all combinations.
- **Blazing-Fast Performance**: Optimizing the extension for large projects.
- **Global Reach**: Adding localization to support developers worldwide.
- **A few real gems. Prepare to be surprised...**
- **Community-Driven Features**: Incorporating feedback and ideas from our users.

## 🎉 Join the Beta

Morgana is currently in **BETA**, and we'd love for you to try it out! Send us an email at [morgana@iandme.rocks](mailto:morgana@iandme.rocks) to request the latest version. Your feedback will help us shape the future of Morgana.

## 📺 See Morgana in Action

Want to see how Morgana transforms your RPG development experience? Check out our demonstration video that showcases the key features and capabilities of the Morgana extension in action.

[**🎬 Watch Morgana Demo on YouTube**](https://www.youtube.com/watch?v=PaBFrVJN4xY)

This video walks you through the main features of Morgana, demonstrating how the outline view works with real RPG code and how it can streamline your development workflow. See firsthand how Morgana makes navigating complex RPG programs intuitive and efficient.

## 💡 Get Involved

This repository is a space for collaboration and innovation. Here’s how you can contribute:

- **Report Issues**: Found a bug? Let us know!
- **Start a Discussion**: Have an idea? Share it with the community.
- **Contribute Code**: We welcome pull requests and suggestions.

## 📬 Contact Us

Have questions or feedback? Reach out to us at [morgana@iandme.rocks](mailto:morgana@iandme.rocks). We’d love to hear from you.

---

Thank you for supporting Morgana. Together, we can make RPG development more modern and efficient. Let’s build the future of RPG tools!
