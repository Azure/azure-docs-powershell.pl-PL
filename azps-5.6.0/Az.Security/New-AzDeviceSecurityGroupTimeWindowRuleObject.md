---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: fb068adcf7a7775106714dce9d91d23ae5e2c240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984161"
---
# <span data-ttu-id="13b5a-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="13b5a-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="13b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="13b5a-103">Utwórz nową regułę czasu dla grupy zabezpieczeń urządzeń (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="13b5a-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="13b5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13b5a-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13b5a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="13b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="13b5a-106">Polecenie New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet tworzy nową listę reguł alertów dotyczących okna czasowego dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="13b5a-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="13b5a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="13b5a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13b5a-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="13b5a-109">Tworzenie reguły nowego okna czasowego z typu "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="13b5a-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="13b5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="13b5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b5a-111">-DefaultProfile</span></span>
<span data-ttu-id="13b5a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13b5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b5a-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="13b5a-113">-Enabled</span></span>
<span data-ttu-id="13b5a-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="13b5a-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="13b5a-115">- MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="13b5a-115">-MaxThreshold</span></span>
<span data-ttu-id="13b5a-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="13b5a-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="13b5a-117">- MinThreshold</span><span class="sxs-lookup"><span data-stu-id="13b5a-117">-MinThreshold</span></span>
<span data-ttu-id="13b5a-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="13b5a-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="13b5a-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="13b5a-119">-TimeWindowSize</span></span>
<span data-ttu-id="13b5a-120">Rozmiar okna czasu.</span><span class="sxs-lookup"><span data-stu-id="13b5a-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b5a-121">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="13b5a-121">-Type</span></span>
<span data-ttu-id="13b5a-122">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="13b5a-122">Rule type.</span></span>

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

### <span data-ttu-id="13b5a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b5a-123">CommonParameters</span></span>
<span data-ttu-id="13b5a-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b5a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b5a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b5a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b5a-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13b5a-126">INPUTS</span></span>

### <span data-ttu-id="13b5a-127">Brak</span><span class="sxs-lookup"><span data-stu-id="13b5a-127">None</span></span>

## <span data-ttu-id="13b5a-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13b5a-128">OUTPUTS</span></span>

### <span data-ttu-id="13b5a-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="13b5a-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="13b5a-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13b5a-130">NOTES</span></span>

## <span data-ttu-id="13b5a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13b5a-131">RELATED LINKS</span></span>
