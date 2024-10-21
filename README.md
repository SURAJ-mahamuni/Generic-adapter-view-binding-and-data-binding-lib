# Generic RecyclerView Adapter with ViewBinding and DataBinding

## Release v1.0.0

We are excited to announce the initial release of our library, which simplifies the creation of RecyclerView adapters in Android development. This release includes a robust, generic RecyclerView adapter that supports both ViewBinding and DataBinding, allowing for more concise, maintainable, and scalable code.

## Features

- **Generic RecyclerView Adapter**: Easily create RecyclerView adapters without boilerplate code. This adapter is designed to be reusable and adaptable for various data types and layouts.
- **ViewBinding Support**: Simplifies the process of binding views, reducing the need for `findViewById` and enhancing code safety with null-safety and type-safety.
- **DataBinding Support**: Enables powerful data-binding capabilities, allowing your layouts to directly bind to your data models and reducing the need for manual updates.
- **Flexible and Extensible**: Customize the adapter for different use cases and easily integrate with existing projects.

## Getting Started

To use this library, add the following dependency to your project's `build.gradle` file:

```groovy
dependencies {
    implementation 'com.yourusername:generic-recycler-view-adapter:1.0.0'
}

Usage
ViewBinding Example
Create your item layout XML file with ViewBinding enabled.
Create your data model class.
Use the generic adapter in your Activity/Fragment:

val adapter = GenericRecyclerViewAdapter(
    layoutId = R.layout.item_layout,
    bind = { item, binding ->
        // Bind your item data to the ViewBinding instance
        binding.textView.text = item.name
    }
)

recyclerView.adapter = adapter
adapter.submitList(yourDataList)

DataBinding Example
Create your item layout XML file with DataBinding enabled.
Create your data model class.
Use the generic adapter in your Activity/Fragment:

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

