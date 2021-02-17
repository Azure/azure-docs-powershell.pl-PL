---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197906"
---
# <span data-ttu-id="d6697-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="d6697-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="d6697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6697-102">SYNOPSIS</span></span>
<span data-ttu-id="d6697-103">Utwórz nową regułę czasu dla grupy zabezpieczeń urządzeń (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="d6697-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d6697-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6697-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6697-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6697-105">DESCRIPTION</span></span>
<span data-ttu-id="d6697-106">Polecenie New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet tworzy nową listę reguł alertów dotyczących czasu w oknie czasowym dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="d6697-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d6697-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6697-107">EXAMPLES</span></span>

### <span data-ttu-id="d6697-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6697-108">Example 1</span></span>
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

<span data-ttu-id="d6697-109">Tworzenie reguły nowego okna czasowego z typu "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="d6697-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="d6697-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6697-110">PARAMETERS</span></span>

### <span data-ttu-id="d6697-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6697-111">-DefaultProfile</span></span>
<span data-ttu-id="d6697-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6697-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6697-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="d6697-113">-Enabled</span></span>
<span data-ttu-id="d6697-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d6697-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="d6697-115">- MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="d6697-115">-MaxThreshold</span></span>
<span data-ttu-id="d6697-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="d6697-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="d6697-117">- MinThreshold</span><span class="sxs-lookup"><span data-stu-id="d6697-117">-MinThreshold</span></span>
<span data-ttu-id="d6697-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="d6697-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="d6697-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="d6697-119">-TimeWindowSize</span></span>
<span data-ttu-id="d6697-120">Rozmiar okna czasu.</span><span class="sxs-lookup"><span data-stu-id="d6697-120">Time window size.</span></span>

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

### <span data-ttu-id="d6697-121">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d6697-121">-Type</span></span>
<span data-ttu-id="d6697-122">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="d6697-122">Rule type.</span></span>

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

### <span data-ttu-id="d6697-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6697-123">CommonParameters</span></span>
<span data-ttu-id="d6697-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6697-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6697-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6697-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6697-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6697-126">INPUTS</span></span>

### <span data-ttu-id="d6697-127">Brak</span><span class="sxs-lookup"><span data-stu-id="d6697-127">None</span></span>

## <span data-ttu-id="d6697-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6697-128">OUTPUTS</span></span>

### <span data-ttu-id="d6697-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d6697-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="d6697-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6697-130">NOTES</span></span>

## <span data-ttu-id="d6697-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6697-131">RELATED LINKS</span></span>
