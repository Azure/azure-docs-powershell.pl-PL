---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 80e322fe589fbfe8d13ab9a754c98bec2fff741f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867699"
---
# <span data-ttu-id="d14c1-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="d14c1-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="d14c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d14c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d14c1-103">Pobiera uaktualnioną definicję dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="d14c1-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="d14c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d14c1-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d14c1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d14c1-105">DESCRIPTION</span></span>
<span data-ttu-id="d14c1-106">Polecenie cmdlet **Get-AzLogicAppUpgradedDefinition** pobiera uaktualnioną definicję dla wersji schematu i aplikacji logicznej z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d14c1-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="d14c1-107">To polecenie cmdlet zwraca obiekt reprezentujący definicję uaktualnionej aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="d14c1-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="d14c1-108">Określ nazwę grupy zasobów, nazwę aplikacji logicznej i wersję schematu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d14c1-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="d14c1-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="d14c1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d14c1-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d14c1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d14c1-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="d14c1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d14c1-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="d14c1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d14c1-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d14c1-113">EXAMPLES</span></span>

### <span data-ttu-id="d14c1-114">Przykład 1: uzyskiwanie definicji uaktualnionej przez aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="d14c1-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="d14c1-115">W pierwszym poleceniu jest pobierana definicja aplikacji logicznej uaktualnionej do określonej wersji schematu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d14c1-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="d14c1-116">Polecenie zapisuje definicję w zmiennej $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="d14c1-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="d14c1-117">Drugie polecenie wyświetla zawartość $UpgradedDefinition jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="d14c1-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="d14c1-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d14c1-118">PARAMETERS</span></span>

### <span data-ttu-id="d14c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14c1-119">-DefaultProfile</span></span>
<span data-ttu-id="d14c1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d14c1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d14c1-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d14c1-121">-Name</span></span>
<span data-ttu-id="d14c1-122">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="d14c1-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="d14c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="d14c1-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d14c1-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d14c1-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="d14c1-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="d14c1-126">Określa wersję schematu docelowego definicji.</span><span class="sxs-lookup"><span data-stu-id="d14c1-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="d14c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14c1-127">CommonParameters</span></span>
<span data-ttu-id="d14c1-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14c1-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d14c1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14c1-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d14c1-130">INPUTS</span></span>

### <span data-ttu-id="d14c1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d14c1-131">System.String</span></span>

## <span data-ttu-id="d14c1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d14c1-132">OUTPUTS</span></span>

### <span data-ttu-id="d14c1-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="d14c1-133">System.Object</span></span>

## <span data-ttu-id="d14c1-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d14c1-134">NOTES</span></span>

## <span data-ttu-id="d14c1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d14c1-135">RELATED LINKS</span></span>

[<span data-ttu-id="d14c1-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d14c1-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


