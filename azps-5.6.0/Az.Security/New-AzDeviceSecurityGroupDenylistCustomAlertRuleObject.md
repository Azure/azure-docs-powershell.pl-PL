---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979274"
---
# <span data-ttu-id="6d9d9-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="6d9d9-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="6d9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9d9-103">Tworzenie nowej niestandardowej reguły alertów listy odmów dla grupy zabezpieczeń urządzeń (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="6d9d9-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="6d9d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6d9d9-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6d9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9d9-106">Polecenie New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet tworzy nową listę odrzucanych niestandardowych reguł alertów dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="6d9d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6d9d9-107">EXAMPLES</span></span>

### <span data-ttu-id="6d9d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d9d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="6d9d9-109">Tworzenie nowej niestandardowej reguły alertów listy odmów z typem rull "SomeRuleType" i ustawionym stanem na "desable"</span><span class="sxs-lookup"><span data-stu-id="6d9d9-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="6d9d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9d9-110">PARAMETERS</span></span>

### <span data-ttu-id="6d9d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9d9-111">-DefaultProfile</span></span>
<span data-ttu-id="6d9d9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9d9-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="6d9d9-113">-DenylistValue</span></span>
<span data-ttu-id="6d9d9-114">Odrzucanie wartości listy.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9d9-115">— włączone</span><span class="sxs-lookup"><span data-stu-id="6d9d9-115">-Enabled</span></span>
<span data-ttu-id="6d9d9-116">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="6d9d9-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="6d9d9-117">-Type</span></span>
<span data-ttu-id="6d9d9-118">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-118">Rule type.</span></span>

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

### <span data-ttu-id="6d9d9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9d9-119">CommonParameters</span></span>
<span data-ttu-id="6d9d9-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9d9-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d9d9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9d9-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d9d9-122">INPUTS</span></span>

### <span data-ttu-id="6d9d9-123">Brak</span><span class="sxs-lookup"><span data-stu-id="6d9d9-123">None</span></span>

## <span data-ttu-id="6d9d9-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d9d9-124">OUTPUTS</span></span>

### <span data-ttu-id="6d9d9-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="6d9d9-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="6d9d9-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6d9d9-126">NOTES</span></span>

## <span data-ttu-id="6d9d9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d9d9-127">RELATED LINKS</span></span>
