---
description: Check out the implementation recipes collected in the Prefect Recipes library.
tags:
---

# Prefect Recipes

[Prefect recipes](https://github.com/PrefectHQ/prefect-recipes) are common, extensible patterns for setting up Prefect in your execution environment with ready-made ingredients such as Dockerfiles, Terraform files, and GitHub Actions.

Recipes are useful when you are looking to deploy an agent, use event-driven flows, set up unit testing, and more.

The following are Prefect recipes specific to Prefect 2. You can find a full repository of recipes at [https://github.com/PrefectHQ/prefect-recipes](https://github.com/PrefectHQ/prefect-recipes) and additional recipes at [Prefect Discourse](https://discourse.prefect.io/).

### Contributing recipes

We're always looking for new recipe contributions! See the [Prefect Recipes](https://github.com/PrefectHQ/prefect-recipes#contributing--swag-) repository for details on how you can add your Prefect 2 recipe, share flow best practices with fellow Prefect users, and earn some swag.

## Recipe catalog

<!-- The code below is a jinja2 template that will be rendered by generate_catalog.py -->
<div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1rem; margin: 1rem 0 3rem">
{% for collection in collections %}
    <div style="padding: 1rem; box-shadow: 0 6px 16px rgba(0, 0, 0, .3); border-radius: 5px">
        <a href="{{ collection['recipeUrl'] }}">
            <h3 style="margin: 0">{{collection['recipeName']}}</h3>
        </a>
        <div style="height: 110px;">
            <p style="font-size: 0.8rem">
                {{ collection["description"] }}
            </p>
        </div>
        <p style="font-size: 0.6rem">
            Maintained by <a href="{{ collection["authorUrl"] }}">{{ collection["author"] }}</a>
        </p>
        <p style="font-size: 0.6rem">
            This recipe uses:
        </p>
        <p>
            {% for icon in collection['iconUrl'] %}
                <img src="{{ icon }}" style="max-height: 48px; max-width: 48px; margin: 0 0.5em 0 auto;">
            {% endfor %}
        </p>
    </div>
{% endfor %}
</div >
