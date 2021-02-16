---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194234"
---
# <span data-ttu-id="ffa26-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="ffa26-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="ffa26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa26-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa26-103">Pobiera uaktualnioną definicję dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="ffa26-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="ffa26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ffa26-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa26-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ffa26-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa26-106">Polecenie **cmdlet Get-AzLogicAppUpgradedDefinition** pobiera uaktualnioną definicję wersji schematu i aplikację logiki z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffa26-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="ffa26-107">To polecenie cmdlet zwraca obiekt reprezentujący definicję uaktualnionej aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="ffa26-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="ffa26-108">Określ nazwę grupy zasobów, nazwę aplikacji logiki i wersję schematu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ffa26-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="ffa26-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ffa26-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ffa26-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ffa26-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ffa26-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="ffa26-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ffa26-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="ffa26-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ffa26-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ffa26-113">EXAMPLES</span></span>

### <span data-ttu-id="ffa26-114">Przykład 1. Uzyskiwanie uaktualnionej definicji aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="ffa26-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="ffa26-115">Pierwsze polecenie pobiera definicję aplikacji logiki uaktualnioną do określonej wersji schematu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ffa26-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="ffa26-116">Polecenie przechowuje definicję w $UpgradedDefinition zmienną.</span><span class="sxs-lookup"><span data-stu-id="ffa26-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="ffa26-117">Drugie polecenie wyświetla zawartość $UpgradedDefinition w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="ffa26-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="ffa26-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffa26-118">PARAMETERS</span></span>

### <span data-ttu-id="ffa26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa26-119">-DefaultProfile</span></span>
<span data-ttu-id="ffa26-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ffa26-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa26-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ffa26-121">-Name</span></span>
<span data-ttu-id="ffa26-122">Określa nazwę aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="ffa26-122">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa26-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffa26-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffa26-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa26-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="ffa26-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="ffa26-126">Określa wersję definicji w schemacie docelowym.</span><span class="sxs-lookup"><span data-stu-id="ffa26-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa26-127">CommonParameters</span></span>
<span data-ttu-id="ffa26-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa26-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa26-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa26-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa26-130">INPUTS</span></span>

### <span data-ttu-id="ffa26-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ffa26-131">System.String</span></span>

## <span data-ttu-id="ffa26-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa26-132">OUTPUTS</span></span>

### <span data-ttu-id="ffa26-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="ffa26-133">System.Object</span></span>

## <span data-ttu-id="ffa26-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ffa26-134">NOTES</span></span>

## <span data-ttu-id="ffa26-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffa26-135">RELATED LINKS</span></span>

[<span data-ttu-id="ffa26-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ffa26-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


