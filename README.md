# Swift architecture

This document describes my architecture of choice for iOS development using Swift.

# Layers

I generally split my architecture into three different layers. The `User Interface` layer, the `Business Logic` layer and the `Data` layer.

![Layers](assets/layers.drawio.svg)

## User Interface

Starting with the first or top level layer, the `User Interface` layer.

This layer contains all kind of Classes which are responsible for displaying content to the user.

This includes all subclasses of `UIViewController`, `UIView` or `UITableViewCell/UICollectionViewCell`.

These classes should not contain any logic and just display the given data in their corresponding place. Every subclass of `UIView` and `UITableViewCell/UICollectionViewCell` should have a dedicated `Model` struct, which contains all data, formatted and ready to display.

## Business Logic

## Data

The data layer, like the `User Interface` layer, should not contain any logic and only contains `Models` and classes to provide these Models from different sources, which are called `Repositories`, which I will discuss later.