# Zicht CMS

This metapackage is created to keep all dependencies for a CMS in a 
controlled package. The versioning and updating grants stability 
The packages installed through this package should act stable.

## Installation
Simply require this package `composer require zicht/cms`

### Scripts
Add these lines to your projects composer.json

```

    "scripts": {
        "post-install-cmd": [
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::buildBootstrap",
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::clearCache",
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installAssets",
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installRequirementsFile",
            "Zicht\\Bundle\\MoxieManagerBundle\\Composer\\ScriptHandler::createMoxieManagerSymlinks"
        ],
        "post-update-cmd": [
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::buildBootstrap",
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::clearCache",
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installAssets",
            "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installRequirementsFile",
            "Zicht\\Bundle\\MoxieManagerBundle\\Composer\\ScriptHandler::createMoxieManagerSymlinks"

        ]
    },
    
```