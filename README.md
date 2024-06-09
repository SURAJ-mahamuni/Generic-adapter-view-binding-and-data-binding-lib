<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    Generic RecyclerView Adapter
</head>
<body>
    <h1>Generic RecyclerView Adapter with ViewBinding and DataBinding</h1>
    <h2>Release v1.0.0</h2>
    <p>We are excited to announce the initial release of our library, which simplifies the creation of RecyclerView adapters in Android development. This release includes a robust, generic RecyclerView adapter that supports both ViewBinding and DataBinding, allowing for more concise, maintainable, and scalable code.</p>

    <h2>Features</h2>
    <ul>
        <li><strong>Generic RecyclerView Adapter</strong>: Easily create RecyclerView adapters without boilerplate code. This adapter is designed to be reusable and adaptable for various data types and layouts.</li>
        <li><strong>ViewBinding Support</strong>: Simplifies the process of binding views, reducing the need for findViewById and enhancing code safety with null-safety and type-safety.</li>
        <li><strong>DataBinding Support</strong>: Enables powerful data-binding capabilities, allowing your layouts to directly bind to your data models and reducing the need for manual updates.</li>
        <li><strong>Flexible and Extensible</strong>: Customize the adapter for different use cases and easily integrate with existing projects.</li>
    </ul>

    <h2>Getting Started</h2>
    <p>To use this library, add the following dependency to your project's <code>build.gradle</code> file:</p>
    <pre><code class="language-groovy">
dependencies {
    implementation 'com.yourusername:generic-recycler-view-adapter:1.0.0'
}
    </code></pre>

    <h2>Usage</h2>
    <h3>ViewBinding Example</h3>
    <ol>
        <li>Create your item layout XML file with ViewBinding enabled.</li>
        <li>Create your data model class.</li>
        <li>Use the generic adapter in your Activity/Fragment:</li>
    </ol>
    <pre><code class="language-kotlin">
val adapter = GenericRecyclerViewAdapter(
    layoutId = R.layout.item_layout,
    bind = { item, binding ->
        // Bind your item data to the ViewBinding instance
        binding.textView.text = item.name
    }
)

recyclerView.adapter = adapter
adapter.submitList(yourDataList)
    </code></pre>

    <h3>DataBinding Example</h3>
    <ol>
        <li>Create your item layout XML file with DataBinding enabled.</li>
        <li>Create your data model class.</li>
        <li>Use the generic adapter in your Activity/Fragment:</li>
    </ol>
    <pre><code class="language-kotlin">
val adapter = GenericRecyclerViewAdapter(
    layoutId = R.layout.item_layout,
    bind = { item, binding ->
        // Bind your item data to the DataBinding instance
        binding.setVariable(BR.item, item)
        binding.executePendingBindings()
    }
)

recyclerView.adapter = adapter
adapter.submitList(yourDataList)
    </code></pre>

    <h2>Documentation</h2>
    <p>For detailed documentation, examples, and API reference, please visit the <a href="https://github.com/yourusername/generic-recycler-view-adapter/wiki">Wiki</a>.</p>

    <h2>Feedback and Contributions</h2>
    <p>We welcome feedback and contributions! If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request on our <a href="https://github.com/yourusername/generic-recycler-view-adapter">GitHub repository</a>.</p>

    <h2>License</h2>
    <p>This project is licensed under the MIT License. See the <a href="LICENSE">LICENSE</a> file for details.</p>
</body>
</html>
