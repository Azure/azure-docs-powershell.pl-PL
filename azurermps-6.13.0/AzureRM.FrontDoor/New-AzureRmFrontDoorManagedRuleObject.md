---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717400"
---
# <span data-ttu-id="bb53e-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bb53e-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="bb53e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb53e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb53e-103">Tworzenie obiektu ManagedRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="bb53e-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb53e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb53e-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb53e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb53e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb53e-106">Tworzenie obiektu ManagedRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="bb53e-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="bb53e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb53e-107">EXAMPLES</span></span>

### <span data-ttu-id="bb53e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb53e-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="bb53e-109">Tworzenie obiektu ManagedRule</span><span class="sxs-lookup"><span data-stu-id="bb53e-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="bb53e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb53e-110">PARAMETERS</span></span>

### <span data-ttu-id="bb53e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb53e-111">-DefaultProfile</span></span>
<span data-ttu-id="bb53e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb53e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb53e-113">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="bb53e-113">-Priority</span></span>
<span data-ttu-id="bb53e-114">Opis priorytetu reguły</span><span class="sxs-lookup"><span data-stu-id="bb53e-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb53e-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bb53e-115">-RuleGroupOverride</span></span>
<span data-ttu-id="bb53e-116">Lista zastępowania konfiguracji zarządzanego dostawcy usługi Azure</span><span class="sxs-lookup"><span data-stu-id="bb53e-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb53e-117">-Version</span><span class="sxs-lookup"><span data-stu-id="bb53e-117">-Version</span></span>
<span data-ttu-id="bb53e-118">Wersja zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="bb53e-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb53e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb53e-119">CommonParameters</span></span>
<span data-ttu-id="bb53e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb53e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb53e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb53e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb53e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb53e-122">INPUTS</span></span>

### <span data-ttu-id="bb53e-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bb53e-123">None</span></span>

## <span data-ttu-id="bb53e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb53e-124">OUTPUTS</span></span>

### <span data-ttu-id="bb53e-125">Microsoft. Azure. Commands. FrontDoor. models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="bb53e-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="bb53e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb53e-126">NOTES</span></span>

## <span data-ttu-id="bb53e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb53e-127">RELATED LINKS</span></span>

<span data-ttu-id="bb53e-128">[Nowe — AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Nowe — AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="bb53e-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
