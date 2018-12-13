# Accessibility
A repository highlighting many different accessibility issues faced in a web app

Tabindex is for keyboard navigation, automatically some elements that are actionable like a, 
button are table able. However sometimes we might want to focus on a non tablindex element, like a heading. 
But when we do this we set the tab index to -1 so the user can’t tab through to it.

Use: `<strong>` instead of `<b>` tag. A screen with shout on a `<b>` but not on a `<strong>`.
Use `<em>` instead of `<i>` tag

## References 

* [Heading Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements#Accessibility_concerns)

## VoiceOver

You can turn on VoiceOver in `system preferences > Accessibility > Enable VoiceOver`

But holding down capslock button and the arrows you can use the keyboard to navigate though VoiceOver. 
You can also use `shift` + `control` + `option` and the arrows too. 

Tabbing in the VoiceOver state is just tabbing and not VoiceOver. 

When you're in VoiceOver mode you can press `k` and then any button to get some help on the buttions.

### Errors 

If we add a `role="alert"` the VoiceOver will read out these messages straight away.

```
<div role="alert">This field is invalid</div>
```

A proplem with this is though that it doesn't focus to those fields with errors. Dru mentioned a good solution is to have inline errors by the fields. Then put a summary of all of these errors with anchors to the input field at the top of the form. So when you click "submit" the focus changes to the summary and then the user can tab though normally. 

### Android 

On Android `select` buttons that are `disabled` still go through all the options. 

## High contrast

Dont use CSS shapes for things as they don't show up in HighContrast mode. Use an SVG instead. 
