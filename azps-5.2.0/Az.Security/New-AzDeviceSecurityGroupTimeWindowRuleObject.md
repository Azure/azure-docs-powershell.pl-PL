---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337321"
---
# <span data-ttu-id="32b5b-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="32b5b-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="32b5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="32b5b-103">Tworzenie nowej reguły przedziału czasu dla grupy zabezpieczeń urządzenia (zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="32b5b-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="32b5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32b5b-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32b5b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32b5b-105">DESCRIPTION</span></span>
<span data-ttu-id="32b5b-106">Polecenie cmdlet New-AzDeviceSecurityGroupTimeWindowRuleObject służy do tworzenia nowej listy reguł alertów dotyczących okien czasu dla grupy zabezpieczeń urządzenia w rozwiązaniu bezpieczeństwa IoT.</span><span class="sxs-lookup"><span data-stu-id="32b5b-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="32b5b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32b5b-107">EXAMPLES</span></span>

### <span data-ttu-id="32b5b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32b5b-108">Example 1</span></span>
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

<span data-ttu-id="32b5b-109">Tworzenie nowej reguły dotyczącej okien czasu na podstawie typu "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="32b5b-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="32b5b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32b5b-110">PARAMETERS</span></span>

### <span data-ttu-id="32b5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b5b-111">-DefaultProfile</span></span>
<span data-ttu-id="32b5b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32b5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b5b-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="32b5b-113">-Enabled</span></span>
<span data-ttu-id="32b5b-114">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="32b5b-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="32b5b-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="32b5b-115">-MaxThreshold</span></span>
<span data-ttu-id="32b5b-116">Próg maksymalny.</span><span class="sxs-lookup"><span data-stu-id="32b5b-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="32b5b-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="32b5b-117">-MinThreshold</span></span>
<span data-ttu-id="32b5b-118">Próg minimalny.</span><span class="sxs-lookup"><span data-stu-id="32b5b-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="32b5b-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="32b5b-119">-TimeWindowSize</span></span>
<span data-ttu-id="32b5b-120">Rozmiar okna czasu.</span><span class="sxs-lookup"><span data-stu-id="32b5b-120">Time window size.</span></span>

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

### <span data-ttu-id="32b5b-121">-Type</span><span class="sxs-lookup"><span data-stu-id="32b5b-121">-Type</span></span>
<span data-ttu-id="32b5b-122">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="32b5b-122">Rule type.</span></span>

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

### <span data-ttu-id="32b5b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b5b-123">CommonParameters</span></span>
<span data-ttu-id="32b5b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b5b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b5b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32b5b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b5b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32b5b-126">INPUTS</span></span>

### <span data-ttu-id="32b5b-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="32b5b-127">None</span></span>

## <span data-ttu-id="32b5b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32b5b-128">OUTPUTS</span></span>

### <span data-ttu-id="32b5b-129">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="32b5b-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="32b5b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32b5b-130">NOTES</span></span>

## <span data-ttu-id="32b5b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32b5b-131">RELATED LINKS</span></span>
