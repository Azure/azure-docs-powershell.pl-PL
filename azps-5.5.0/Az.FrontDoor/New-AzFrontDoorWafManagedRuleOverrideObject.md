---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237820"
---
# <span data-ttu-id="8810b-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="8810b-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="8810b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8810b-102">SYNOPSIS</span></span>
<span data-ttu-id="8810b-103">Tworzenie obiektu zastępowania reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="8810b-103">Create managed rule override object</span></span>

## <span data-ttu-id="8810b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8810b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8810b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8810b-105">DESCRIPTION</span></span>
<span data-ttu-id="8810b-106">Tworzenie obiektu PSAzureManagedRuleOverride dla zarządzanej grupy reguł WAF zastępuje tworzenie obiektów.</span><span class="sxs-lookup"><span data-stu-id="8810b-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="8810b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8810b-107">EXAMPLES</span></span>

### <span data-ttu-id="8810b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8810b-108">Example 1</span></span>
<span data-ttu-id="8810b-109">Utwórz obiekt reguły zarządzanej zastępujący regułę 942250 (która znajduje się w grupie SQLI).</span><span class="sxs-lookup"><span data-stu-id="8810b-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="8810b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8810b-110">PARAMETERS</span></span>

### <span data-ttu-id="8810b-111">— akcja</span><span class="sxs-lookup"><span data-stu-id="8810b-111">-Action</span></span>
<span data-ttu-id="8810b-112">Akcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="8810b-112">Override Action</span></span>

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

### <span data-ttu-id="8810b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8810b-113">-DefaultProfile</span></span>
<span data-ttu-id="8810b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8810b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8810b-115">— Wyłączone</span><span class="sxs-lookup"><span data-stu-id="8810b-115">-Disabled</span></span>
<span data-ttu-id="8810b-116">Stan wyłączenia</span><span class="sxs-lookup"><span data-stu-id="8810b-116">Disabled state</span></span>

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

### <span data-ttu-id="8810b-117">— Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="8810b-117">-Exclusion</span></span>
<span data-ttu-id="8810b-118">Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="8810b-118">Exclusion</span></span>

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

### <span data-ttu-id="8810b-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="8810b-119">-RuleId</span></span>
<span data-ttu-id="8810b-120">Identyfikator reguły</span><span class="sxs-lookup"><span data-stu-id="8810b-120">Rule ID</span></span>

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

### <span data-ttu-id="8810b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8810b-121">CommonParameters</span></span>
<span data-ttu-id="8810b-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8810b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8810b-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8810b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8810b-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8810b-124">INPUTS</span></span>

### <span data-ttu-id="8810b-125">Brak</span><span class="sxs-lookup"><span data-stu-id="8810b-125">None</span></span>

## <span data-ttu-id="8810b-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8810b-126">OUTPUTS</span></span>

### <span data-ttu-id="8810b-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8810b-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="8810b-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8810b-128">NOTES</span></span>

## <span data-ttu-id="8810b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8810b-129">RELATED LINKS</span></span>

[<span data-ttu-id="8810b-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="8810b-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)