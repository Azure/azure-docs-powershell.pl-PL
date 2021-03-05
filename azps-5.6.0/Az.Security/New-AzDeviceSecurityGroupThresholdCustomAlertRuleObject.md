---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984177"
---
# <span data-ttu-id="9755b-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="9755b-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="9755b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9755b-102">SYNOPSIS</span></span>
<span data-ttu-id="9755b-103">Tworzenie nowej niestandardowej reguły alertu progowego dla grupy zabezpieczeń urządzeń (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="9755b-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="9755b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9755b-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9755b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9755b-105">DESCRIPTION</span></span>
<span data-ttu-id="9755b-106">Polecenie New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet tworzy nową listę próg niestandardowych reguł alertów dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="9755b-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="9755b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9755b-107">EXAMPLES</span></span>

### <span data-ttu-id="9755b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9755b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="9755b-109">Tworzenie nowej niestandardowej reguły alertu progu z typu "SomeRuleType" z włączonymi wartościamiantów stanu dla progu minimalnego i maksymalnego</span><span class="sxs-lookup"><span data-stu-id="9755b-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="9755b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9755b-110">PARAMETERS</span></span>

### <span data-ttu-id="9755b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9755b-111">-DefaultProfile</span></span>
<span data-ttu-id="9755b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9755b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9755b-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="9755b-113">-Enabled</span></span>
<span data-ttu-id="9755b-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="9755b-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9755b-115">- MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="9755b-115">-MaxThreshold</span></span>
<span data-ttu-id="9755b-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="9755b-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="9755b-117">- MinThreshold</span><span class="sxs-lookup"><span data-stu-id="9755b-117">-MinThreshold</span></span>
<span data-ttu-id="9755b-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="9755b-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="9755b-119">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="9755b-119">-Type</span></span>
<span data-ttu-id="9755b-120">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="9755b-120">Rule type.</span></span>

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

### <span data-ttu-id="9755b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9755b-121">CommonParameters</span></span>
<span data-ttu-id="9755b-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9755b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9755b-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9755b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9755b-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9755b-124">INPUTS</span></span>

### <span data-ttu-id="9755b-125">Brak</span><span class="sxs-lookup"><span data-stu-id="9755b-125">None</span></span>

## <span data-ttu-id="9755b-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9755b-126">OUTPUTS</span></span>

### <span data-ttu-id="9755b-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="9755b-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="9755b-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9755b-128">NOTES</span></span>

## <span data-ttu-id="9755b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9755b-129">RELATED LINKS</span></span>
