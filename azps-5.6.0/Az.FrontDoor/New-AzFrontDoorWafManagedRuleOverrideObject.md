---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970849"
---
# <span data-ttu-id="79b41-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="79b41-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="79b41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b41-102">SYNOPSIS</span></span>
<span data-ttu-id="79b41-103">Tworzenie obiektu zastępowania reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="79b41-103">Create managed rule override object</span></span>

## <span data-ttu-id="79b41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79b41-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79b41-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79b41-105">DESCRIPTION</span></span>
<span data-ttu-id="79b41-106">Utwórz obiekt PSAzureManagedRuleOverride dla zarządzanej grupy reguł WAF, zastępując tworzenie obiektów.</span><span class="sxs-lookup"><span data-stu-id="79b41-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="79b41-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79b41-107">EXAMPLES</span></span>

### <span data-ttu-id="79b41-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79b41-108">Example 1</span></span>
<span data-ttu-id="79b41-109">Utwórz obiekt reguły zarządzanej zastępujący regułę 942250 (która znajduje się w grupie SQLI).</span><span class="sxs-lookup"><span data-stu-id="79b41-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="79b41-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79b41-110">PARAMETERS</span></span>

### <span data-ttu-id="79b41-111">— Akcja</span><span class="sxs-lookup"><span data-stu-id="79b41-111">-Action</span></span>
<span data-ttu-id="79b41-112">Akcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="79b41-112">Override Action</span></span>

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

### <span data-ttu-id="79b41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b41-113">-DefaultProfile</span></span>
<span data-ttu-id="79b41-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79b41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b41-115">— Wyłączone</span><span class="sxs-lookup"><span data-stu-id="79b41-115">-Disabled</span></span>
<span data-ttu-id="79b41-116">Stan wyłączenia</span><span class="sxs-lookup"><span data-stu-id="79b41-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b41-117">— Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="79b41-117">-Exclusion</span></span>
<span data-ttu-id="79b41-118">Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="79b41-118">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b41-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="79b41-119">-RuleId</span></span>
<span data-ttu-id="79b41-120">Identyfikator reguły</span><span class="sxs-lookup"><span data-stu-id="79b41-120">Rule ID</span></span>

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

### <span data-ttu-id="79b41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b41-121">CommonParameters</span></span>
<span data-ttu-id="79b41-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b41-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79b41-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b41-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79b41-124">INPUTS</span></span>

### <span data-ttu-id="79b41-125">Brak</span><span class="sxs-lookup"><span data-stu-id="79b41-125">None</span></span>

## <span data-ttu-id="79b41-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79b41-126">OUTPUTS</span></span>

### <span data-ttu-id="79b41-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="79b41-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="79b41-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79b41-128">NOTES</span></span>

## <span data-ttu-id="79b41-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79b41-129">RELATED LINKS</span></span>

[<span data-ttu-id="79b41-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="79b41-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)