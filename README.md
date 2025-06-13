# Dragula 🎉

![Dragula Logo](https://img.shields.io/badge/Dragula-Swift-orange?style=flat-square)

Welcome to **Dragula**, a flexible and smooth drag-and-drop Swift package designed for building reorderable interfaces in SwiftUI. This package makes it easy to implement drag-and-drop functionality in your applications, enhancing user experience and engagement.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Features

- **Easy to Use**: Dragula simplifies the process of adding drag-and-drop capabilities to your SwiftUI projects.
- **Flexible Design**: Customize the look and feel to fit your application's style.
- **Smooth Performance**: Enjoy a responsive and fluid drag-and-drop experience.
- **SwiftUI Compatible**: Built specifically for SwiftUI, ensuring seamless integration.

## Installation

To add Dragula to your project, follow these steps:

1. Open your Xcode project.
2. Navigate to the project settings.
3. Select the "Swift Packages" tab.
4. Click on the "+" button to add a new package.
5. Enter the repository URL: `https://github.com/hH770347221/Dragula`.
6. Choose the version you want to use and click "Add Package".

## Usage

Using Dragula in your SwiftUI project is straightforward. Here’s a simple example to get you started:

```swift
import SwiftUI
import Dragula

struct ContentView: View {
    @State private var items: [String] = ["Item 1", "Item 2", "Item 3"]

    var body: some View {
        Dragula(items: $items) { item in
            Text(item)
                .padding()
                .background(Color.blue)
                .cornerRadius(8)
        }
    }
}
```

In this example, we create a list of items that users can drag and drop. You can easily modify the `items` array to fit your needs.

## Examples

Here are some practical examples of how you can implement Dragula in your projects:

### Example 1: Reorderable List

Create a simple reorderable list with drag-and-drop functionality.

```swift
struct ReorderableListView: View {
    @State private var items = ["Apple", "Banana", "Cherry", "Date"]

    var body: some View {
        Dragula(items: $items) { item in
            Text(item)
                .padding()
                .background(Color.green)
                .cornerRadius(5)
        }
    }
}
```

### Example 2: Custom Styling

Customize the appearance of the draggable items.

```swift
struct CustomStyledView: View {
    @State private var items = ["Red", "Green", "Blue"]

    var body: some View {
        Dragula(items: $items) { item in
            Text(item)
                .padding()
                .background(item == "Red" ? Color.red : item == "Green" ? Color.green : Color.blue)
                .cornerRadius(10)
                .foregroundColor(.white)
        }
    }
}
```

### Example 3: Dynamic Data

Integrate Dragula with dynamic data sources.

```swift
struct DynamicDataView: View {
    @State private var items: [String] = []

    var body: some View {
        VStack {
            Button("Load Data") {
                items = ["Item A", "Item B", "Item C"]
            }
            Dragula(items: $items) { item in
                Text(item)
                    .padding()
                    .background(Color.purple)
                    .cornerRadius(4)
            }
        }
    }
}
```

## Contributing

We welcome contributions to Dragula! If you have ideas for improvements or new features, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your fork.
5. Open a pull request.

Please ensure that your code follows the style and guidelines outlined in this repository.

## License

Dragula is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest updates and versions, please check the [Releases](https://github.com/hH770347221/Dragula/releases) section. You can download the latest version and execute it in your project to take advantage of new features and fixes.

Feel free to explore the features of Dragula and enhance your SwiftUI applications with drag-and-drop functionality. If you have any questions or need assistance, don’t hesitate to reach out.

For more information, visit the [Releases](https://github.com/hH770347221/Dragula/releases) section.