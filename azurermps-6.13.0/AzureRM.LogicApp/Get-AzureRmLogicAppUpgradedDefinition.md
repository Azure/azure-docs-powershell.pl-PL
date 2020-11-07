---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: b0f4569c123a483db1cceffbcdfd68ef8835a31b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719419"
---
# <span data-ttu-id="203f5-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="203f5-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="203f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="203f5-102">SYNOPSIS</span></span>
<span data-ttu-id="203f5-103">Pobiera uaktualnioną definicję dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="203f5-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="203f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="203f5-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="203f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="203f5-105">DESCRIPTION</span></span>
<span data-ttu-id="203f5-106">Polecenie cmdlet **Get-AzureRmLogicAppUpgradedDefinition** pobiera uaktualnioną definicję dla wersji schematu i aplikacji logicznej z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="203f5-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="203f5-107">To polecenie cmdlet zwraca obiekt reprezentujący definicję uaktualnionej aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="203f5-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="203f5-108">Określ nazwę grupy zasobów, nazwę aplikacji logicznej i wersję schematu docelowego.</span><span class="sxs-lookup"><span data-stu-id="203f5-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="203f5-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="203f5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="203f5-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="203f5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="203f5-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="203f5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="203f5-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="203f5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="203f5-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="203f5-113">EXAMPLES</span></span>

### <span data-ttu-id="203f5-114">Przykład 1: uzyskiwanie definicji uaktualnionej przez aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="203f5-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="203f5-115">W pierwszym poleceniu jest pobierana definicja aplikacji logicznej uaktualnionej do określonej wersji schematu docelowego.</span><span class="sxs-lookup"><span data-stu-id="203f5-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="203f5-116">Polecenie zapisuje definicję w zmiennej $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="203f5-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="203f5-117">Drugie polecenie wyświetla zawartość $UpgradedDefinition jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="203f5-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="203f5-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="203f5-118">PARAMETERS</span></span>

### <span data-ttu-id="203f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203f5-119">-DefaultProfile</span></span>
<span data-ttu-id="203f5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="203f5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203f5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="203f5-121">-Name</span></span>
<span data-ttu-id="203f5-122">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="203f5-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="203f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="203f5-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="203f5-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="203f5-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="203f5-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="203f5-126">Określa wersję schematu docelowego definicji.</span><span class="sxs-lookup"><span data-stu-id="203f5-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="203f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203f5-127">CommonParameters</span></span>
<span data-ttu-id="203f5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203f5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203f5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203f5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="203f5-130">INPUTS</span></span>

### <span data-ttu-id="203f5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="203f5-131">System.String</span></span>

## <span data-ttu-id="203f5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="203f5-132">OUTPUTS</span></span>

### <span data-ttu-id="203f5-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="203f5-133">System.Object</span></span>

## <span data-ttu-id="203f5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="203f5-134">NOTES</span></span>

## <span data-ttu-id="203f5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="203f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="203f5-136">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="203f5-136">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

