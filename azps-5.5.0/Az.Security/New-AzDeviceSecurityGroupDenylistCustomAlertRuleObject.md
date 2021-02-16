---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242387"
---
# <span data-ttu-id="e8974-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="e8974-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="e8974-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8974-102">SYNOPSIS</span></span>
<span data-ttu-id="e8974-103">Utwórz nową niestandardową regułę alertu listy odmów dla grupy zabezpieczeń urządzeń (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="e8974-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="e8974-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8974-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8974-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8974-105">DESCRIPTION</span></span>
<span data-ttu-id="e8974-106">Polecenie New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet tworzy nową listę odrzucanych niestandardowych reguł alertów dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="e8974-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="e8974-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8974-107">EXAMPLES</span></span>

### <span data-ttu-id="e8974-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8974-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="e8974-109">Tworzenie nowej niestandardowej reguły alertów listy odmów z typem rull "SomeRuleType" i ustawionym stanem na "desable"</span><span class="sxs-lookup"><span data-stu-id="e8974-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="e8974-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8974-110">PARAMETERS</span></span>

### <span data-ttu-id="e8974-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8974-111">-DefaultProfile</span></span>
<span data-ttu-id="e8974-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8974-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8974-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="e8974-113">-DenylistValue</span></span>
<span data-ttu-id="e8974-114">Odrzucanie wartości listy.</span><span class="sxs-lookup"><span data-stu-id="e8974-114">Deny list values.</span></span>

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

### <span data-ttu-id="e8974-115">— włączone</span><span class="sxs-lookup"><span data-stu-id="e8974-115">-Enabled</span></span>
<span data-ttu-id="e8974-116">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="e8974-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="e8974-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="e8974-117">-Type</span></span>
<span data-ttu-id="e8974-118">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="e8974-118">Rule type.</span></span>

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

### <span data-ttu-id="e8974-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8974-119">CommonParameters</span></span>
<span data-ttu-id="e8974-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8974-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8974-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8974-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8974-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8974-122">INPUTS</span></span>

### <span data-ttu-id="e8974-123">Brak</span><span class="sxs-lookup"><span data-stu-id="e8974-123">None</span></span>

## <span data-ttu-id="e8974-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8974-124">OUTPUTS</span></span>

### <span data-ttu-id="e8974-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="e8974-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="e8974-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8974-126">NOTES</span></span>

## <span data-ttu-id="e8974-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8974-127">RELATED LINKS</span></span>
