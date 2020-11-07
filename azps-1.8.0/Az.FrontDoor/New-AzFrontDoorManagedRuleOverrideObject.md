---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
ms.openlocfilehash: e45abaae34f3b8449920dad122736c46b9d946ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868371"
---
# <span data-ttu-id="7bed7-101">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="7bed7-101">New-AzFrontDoorManagedRuleOverrideObject</span></span>

## <span data-ttu-id="7bed7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7bed7-102">SYNOPSIS</span></span>
<span data-ttu-id="7bed7-103">Utwórz obiekt zastąpienia reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="7bed7-103">Create managed rule override object</span></span>

## <span data-ttu-id="7bed7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7bed7-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleOverrideObject -RuleId <String> [-Action <PSAction>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bed7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7bed7-105">DESCRIPTION</span></span>
<span data-ttu-id="7bed7-106">Tworzenie obiektu PSAzureManagedRuleOverride dla zarządzanej grupy reguł WAF w celu zastąpienia tworzenia obiektu.</span><span class="sxs-lookup"><span data-stu-id="7bed7-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="7bed7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7bed7-107">EXAMPLES</span></span>

### <span data-ttu-id="7bed7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7bed7-108">Example 1</span></span>
<span data-ttu-id="7bed7-109">Utwórz obiekt zastępowania reguły zarządzanej dla reguły 942250 (która jest w grupie SQLI).</span><span class="sxs-lookup"><span data-stu-id="7bed7-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="7bed7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7bed7-110">PARAMETERS</span></span>

### <span data-ttu-id="7bed7-111">-Action</span><span class="sxs-lookup"><span data-stu-id="7bed7-111">-Action</span></span>
<span data-ttu-id="7bed7-112">Akcja przesłonięcia</span><span class="sxs-lookup"><span data-stu-id="7bed7-112">Override Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bed7-113">-DefaultProfile</span></span>
<span data-ttu-id="7bed7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bed7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bed7-115">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="7bed7-115">-Disabled</span></span>
<span data-ttu-id="7bed7-116">Stan wyłączenia</span><span class="sxs-lookup"><span data-stu-id="7bed7-116">Disabled state</span></span>

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

### <span data-ttu-id="7bed7-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="7bed7-117">-RuleId</span></span>
<span data-ttu-id="7bed7-118">Identyfikator reguły</span><span class="sxs-lookup"><span data-stu-id="7bed7-118">Rule ID</span></span>

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

### <span data-ttu-id="7bed7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bed7-119">CommonParameters</span></span>
<span data-ttu-id="7bed7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bed7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bed7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bed7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bed7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bed7-122">INPUTS</span></span>

### <span data-ttu-id="7bed7-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7bed7-123">None</span></span>

## <span data-ttu-id="7bed7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7bed7-124">OUTPUTS</span></span>

### <span data-ttu-id="7bed7-125">Microsoft. Azure. Commands. FrontDoor. models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7bed7-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="7bed7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7bed7-126">NOTES</span></span>

## <span data-ttu-id="7bed7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bed7-127">RELATED LINKS</span></span>

[<span data-ttu-id="7bed7-128">Nowe — AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="7bed7-128">New-AzFrontDoorRuleGroupOverrideObject</span></span>](./New-AzFrontDoorRuleGroupOverrideObject.md)