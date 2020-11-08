---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063214"
---
# <span data-ttu-id="46000-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="46000-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="46000-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46000-102">SYNOPSIS</span></span>
<span data-ttu-id="46000-103">Utwórz nową regułę alertu niestandardowego progu dla grupy zabezpieczeń urządzenia (z zabezpieczeniami IoT)</span><span class="sxs-lookup"><span data-stu-id="46000-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="46000-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46000-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46000-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46000-105">DESCRIPTION</span></span>
<span data-ttu-id="46000-106">Polecenie cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject tworzy nową listę niestandardowych reguł alertów dla grupy zabezpieczeń urządzenia w rozwiązaniu bezpieczeństwa IoT.</span><span class="sxs-lookup"><span data-stu-id="46000-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="46000-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46000-107">EXAMPLES</span></span>

### <span data-ttu-id="46000-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46000-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="46000-109">Utwórz nową regułę alertu niestandardowego progu z typu "SomeRuleType" z włączonym stanem wartości ANT dla progu minimalnego i maksymalnego</span><span class="sxs-lookup"><span data-stu-id="46000-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="46000-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46000-110">PARAMETERS</span></span>

### <span data-ttu-id="46000-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46000-111">-DefaultProfile</span></span>
<span data-ttu-id="46000-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46000-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46000-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="46000-113">-Enabled</span></span>
<span data-ttu-id="46000-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="46000-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="46000-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="46000-115">-MaxThreshold</span></span>
<span data-ttu-id="46000-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="46000-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="46000-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="46000-117">-MinThreshold</span></span>
<span data-ttu-id="46000-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="46000-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="46000-119">-Type</span><span class="sxs-lookup"><span data-stu-id="46000-119">-Type</span></span>
<span data-ttu-id="46000-120">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="46000-120">Rule type.</span></span>

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

### <span data-ttu-id="46000-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46000-121">CommonParameters</span></span>
<span data-ttu-id="46000-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46000-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46000-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46000-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46000-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46000-124">INPUTS</span></span>

### <span data-ttu-id="46000-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="46000-125">None</span></span>

## <span data-ttu-id="46000-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46000-126">OUTPUTS</span></span>

### <span data-ttu-id="46000-127">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="46000-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="46000-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46000-128">NOTES</span></span>

## <span data-ttu-id="46000-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46000-129">RELATED LINKS</span></span>
