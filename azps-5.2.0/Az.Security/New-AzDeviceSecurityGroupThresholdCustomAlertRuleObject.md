---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337369"
---
# <span data-ttu-id="4b305-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="4b305-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="4b305-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b305-102">SYNOPSIS</span></span>
<span data-ttu-id="4b305-103">Utwórz nową regułę alertu niestandardowego progu dla grupy zabezpieczeń urządzenia (z zabezpieczeniami IoT)</span><span class="sxs-lookup"><span data-stu-id="4b305-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="4b305-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b305-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b305-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b305-105">DESCRIPTION</span></span>
<span data-ttu-id="4b305-106">Polecenie cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject tworzy nową listę niestandardowych reguł alertów dla grupy zabezpieczeń urządzenia w rozwiązaniu bezpieczeństwa IoT.</span><span class="sxs-lookup"><span data-stu-id="4b305-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="4b305-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b305-107">EXAMPLES</span></span>

### <span data-ttu-id="4b305-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4b305-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="4b305-109">Utwórz nową regułę alertu niestandardowego progu z typu "SomeRuleType" z włączonym stanem wartości ANT dla progu minimalnego i maksymalnego</span><span class="sxs-lookup"><span data-stu-id="4b305-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="4b305-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b305-110">PARAMETERS</span></span>

### <span data-ttu-id="4b305-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b305-111">-DefaultProfile</span></span>
<span data-ttu-id="4b305-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b305-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b305-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4b305-113">-Enabled</span></span>
<span data-ttu-id="4b305-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="4b305-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="4b305-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="4b305-115">-MaxThreshold</span></span>
<span data-ttu-id="4b305-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="4b305-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="4b305-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="4b305-117">-MinThreshold</span></span>
<span data-ttu-id="4b305-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="4b305-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="4b305-119">-Type</span><span class="sxs-lookup"><span data-stu-id="4b305-119">-Type</span></span>
<span data-ttu-id="4b305-120">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="4b305-120">Rule type.</span></span>

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

### <span data-ttu-id="4b305-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b305-121">CommonParameters</span></span>
<span data-ttu-id="4b305-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b305-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b305-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b305-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b305-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b305-124">INPUTS</span></span>

### <span data-ttu-id="4b305-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4b305-125">None</span></span>

## <span data-ttu-id="4b305-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b305-126">OUTPUTS</span></span>

### <span data-ttu-id="4b305-127">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="4b305-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="4b305-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b305-128">NOTES</span></span>

## <span data-ttu-id="4b305-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b305-129">RELATED LINKS</span></span>
