---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197922"
---
# <span data-ttu-id="8ec12-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="8ec12-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="8ec12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec12-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec12-103">Tworzenie nowej niestandardowej reguły alertu progowego dla grupy zabezpieczeń urządzeń (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="8ec12-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="8ec12-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ec12-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec12-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ec12-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec12-106">Polecenie New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet tworzy nową listę próg niestandardowych reguł alertów dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="8ec12-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="8ec12-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ec12-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ec12-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="8ec12-109">Tworzenie nowej niestandardowej reguły alertu progu z typu "SomeRuleType" z włączonymi wartościamiantów stanu dla progu minimalnego i maksymalnego</span><span class="sxs-lookup"><span data-stu-id="8ec12-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="8ec12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec12-110">PARAMETERS</span></span>

### <span data-ttu-id="8ec12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec12-111">-DefaultProfile</span></span>
<span data-ttu-id="8ec12-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ec12-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="8ec12-113">-Enabled</span></span>
<span data-ttu-id="8ec12-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="8ec12-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="8ec12-115">- MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="8ec12-115">-MaxThreshold</span></span>
<span data-ttu-id="8ec12-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="8ec12-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="8ec12-117">- MinThreshold</span><span class="sxs-lookup"><span data-stu-id="8ec12-117">-MinThreshold</span></span>
<span data-ttu-id="8ec12-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="8ec12-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="8ec12-119">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="8ec12-119">-Type</span></span>
<span data-ttu-id="8ec12-120">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="8ec12-120">Rule type.</span></span>

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

### <span data-ttu-id="8ec12-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec12-121">CommonParameters</span></span>
<span data-ttu-id="8ec12-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec12-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec12-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ec12-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec12-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ec12-124">INPUTS</span></span>

### <span data-ttu-id="8ec12-125">Brak</span><span class="sxs-lookup"><span data-stu-id="8ec12-125">None</span></span>

## <span data-ttu-id="8ec12-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ec12-126">OUTPUTS</span></span>

### <span data-ttu-id="8ec12-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="8ec12-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="8ec12-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ec12-128">NOTES</span></span>

## <span data-ttu-id="8ec12-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ec12-129">RELATED LINKS</span></span>
