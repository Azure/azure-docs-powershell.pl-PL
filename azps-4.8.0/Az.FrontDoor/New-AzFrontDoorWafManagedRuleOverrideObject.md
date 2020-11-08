---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222540"
---
# <span data-ttu-id="3ea8d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3ea8d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="3ea8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ea8d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea8d-103">Utwórz obiekt zastąpienia reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="3ea8d-103">Create managed rule override object</span></span>

## <span data-ttu-id="3ea8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ea8d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ea8d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ea8d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea8d-106">Tworzenie obiektu PSAzureManagedRuleOverride dla zarządzanej grupy reguł WAF w celu zastąpienia tworzenia obiektu.</span><span class="sxs-lookup"><span data-stu-id="3ea8d-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="3ea8d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ea8d-107">EXAMPLES</span></span>

### <span data-ttu-id="3ea8d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ea8d-108">Example 1</span></span>
<span data-ttu-id="3ea8d-109">Utwórz obiekt zastępowania reguły zarządzanej dla reguły 942250 (która jest w grupie SQLI).</span><span class="sxs-lookup"><span data-stu-id="3ea8d-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="3ea8d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ea8d-110">PARAMETERS</span></span>

### <span data-ttu-id="3ea8d-111">-Action</span><span class="sxs-lookup"><span data-stu-id="3ea8d-111">-Action</span></span>
<span data-ttu-id="3ea8d-112">Akcja przesłonięcia</span><span class="sxs-lookup"><span data-stu-id="3ea8d-112">Override Action</span></span>

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

### <span data-ttu-id="3ea8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea8d-113">-DefaultProfile</span></span>
<span data-ttu-id="3ea8d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ea8d-115">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="3ea8d-115">-Disabled</span></span>
<span data-ttu-id="3ea8d-116">Stan wyłączenia</span><span class="sxs-lookup"><span data-stu-id="3ea8d-116">Disabled state</span></span>

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

### <span data-ttu-id="3ea8d-117">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="3ea8d-117">-Exclusion</span></span>
<span data-ttu-id="3ea8d-118">Wyjątki</span><span class="sxs-lookup"><span data-stu-id="3ea8d-118">Exclusion</span></span>

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

### <span data-ttu-id="3ea8d-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="3ea8d-119">-RuleId</span></span>
<span data-ttu-id="3ea8d-120">Identyfikator reguły</span><span class="sxs-lookup"><span data-stu-id="3ea8d-120">Rule ID</span></span>

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

### <span data-ttu-id="3ea8d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea8d-121">CommonParameters</span></span>
<span data-ttu-id="3ea8d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea8d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea8d-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ea8d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea8d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ea8d-124">INPUTS</span></span>

### <span data-ttu-id="3ea8d-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3ea8d-125">None</span></span>

## <span data-ttu-id="3ea8d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ea8d-126">OUTPUTS</span></span>

### <span data-ttu-id="3ea8d-127">Microsoft. Azure. Commands. FrontDoor. models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3ea8d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="3ea8d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ea8d-128">NOTES</span></span>

## <span data-ttu-id="3ea8d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ea8d-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ea8d-130">Nowe — AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3ea8d-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)