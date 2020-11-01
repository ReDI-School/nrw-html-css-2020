---
title: Forms
nav_order: 9
---

## Review

-   `<span>`
-   `<button>`
-   `<input>`

## New Tags

-   `<textarea>` ([documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea))
-   `<select>` & `<option>` ([documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select))
-   `<form>` ([documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)).

## Bringing it Together: Build a Form

```
   <form id="contact" action="" method="post">
        <h3>Quick Contact</h3>
        <h4>Contact us today, and get reply with in 24 hours!</h4>
        <fieldset>
            <input
                placeholder="Your name"
                type="text"
                tabindex="1"
                required
                autofocus
            />
        </fieldset>

        <fieldset>
            <input
                placeholder="Your Email Address"
                type="email"
                tabindex="2"
                required
            />
        </fieldset>

        <fieldset>
            <input
                placeholder="Your Phone Number"
                type="tel"
                tabindex="3"
                required
            />
        </fieldset>

        <fieldset>
            <input
                placeholder="Your Web Site starts with http://"
                type="url"
                tabindex="4"
                required
            />
        </fieldset>

        <fieldset>
            <textarea
                placeholder="Type your Message Here...."
                tabindex="5"
                required
            ></textarea>
        </fieldset>


        <fieldset>
            <p>Select a maintenance drone:</p>

            <div>
                <input
                    type="radio"
                    id="huey"
                    name="drone"
                    value="huey"
                    checked
                />
                <label for="huey">Huey</label>
            </div>

            <div>
                <input
                    type="radio"
                    id="dewey"
                    name="drone"
                    value="dewey"
                />
                <label for="dewey">Dewey</label>
            </div>
        </fieldset>


        <fieldset>
            <button
                name="submit"
                type="submit"
                id="contact-submit"
                data-submit="...Sending"
            >
                Submit
            </button>
        </fieldset>

    </form>
```
