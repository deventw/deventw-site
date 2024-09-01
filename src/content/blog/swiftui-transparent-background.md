---
title: "Transparent Background for .fullScreenCover"
description: ''
pubDate: 'Aug 27 2024'
heroImage: '/blog-placeholder-3.jpg'
---

```swift
    // ... other code
    .fullScreenCover(isPresented: $isLoading) {
        ZStack{
            Color.black.opacity(0.5).edgesIgnoringSafeArea(.all)
            VStack {
                ProgressView()
                Button("Stop loading") {
                isLoading.toggle()
                }
            }
        }
        .background(BackgroundBlurView())
    }

    struct BackgroundBlurView: UIViewRepresentable {
    func makeUIView(context: Context) -> UIView {
        let view = UIVisualEffectView(effect: UIBlurEffect(style: .light))
        DispatchQueue.main.async {
        view.superview?.superview?.backgroundColor = .clear
        }
        return view
    }

    func updateUIView(_ uiView: UIView, context: Context) {}
}
```

ref: [4SwiftUI](https://github.com/Asperi-Demo/4SwiftUI/blob/master/Answers/Translucent_background_for_fullScreenCover.md)