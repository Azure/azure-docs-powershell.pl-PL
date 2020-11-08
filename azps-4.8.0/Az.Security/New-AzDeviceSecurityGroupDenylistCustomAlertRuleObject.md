---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219868"
---
# <span data-ttu-id="28eb1-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="28eb1-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="28eb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="28eb1-103">Tworzenie nowej niestandardowej reguły alertu listy odrzuconych dla grupy zabezpieczeń urządzenia (z zabezpieczeniami IoT)</span><span class="sxs-lookup"><span data-stu-id="28eb1-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="28eb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28eb1-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28eb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="28eb1-106">Polecenie cmdlet New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject tworzy nową listę odrzuconych niestandardowych reguł alertów dla grupy zabezpieczeń urządzenia w rozwiązaniu bezpieczeństwa IoT.</span><span class="sxs-lookup"><span data-stu-id="28eb1-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="28eb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="28eb1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28eb1-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="28eb1-109">Tworzenie nowej niestandardowej reguły alertu listy odrzuconych z typem Rull "SomeRuleType" i stanem ustawionym na desable</span><span class="sxs-lookup"><span data-stu-id="28eb1-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="28eb1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28eb1-110">PARAMETERS</span></span>

### <span data-ttu-id="28eb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28eb1-111">-DefaultProfile</span></span>
<span data-ttu-id="28eb1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28eb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28eb1-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="28eb1-113">-DenylistValue</span></span>
<span data-ttu-id="28eb1-114">Odmowa wartości listy.</span><span class="sxs-lookup"><span data-stu-id="28eb1-114">Deny list values.</span></span>

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

### <span data-ttu-id="28eb1-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="28eb1-115">-Enabled</span></span>
<span data-ttu-id="28eb1-116">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="28eb1-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="28eb1-117">-Type</span><span class="sxs-lookup"><span data-stu-id="28eb1-117">-Type</span></span>
<span data-ttu-id="28eb1-118">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="28eb1-118">Rule type.</span></span>

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

### <span data-ttu-id="28eb1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28eb1-119">CommonParameters</span></span>
<span data-ttu-id="28eb1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28eb1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28eb1-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28eb1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28eb1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28eb1-122">INPUTS</span></span>

### <span data-ttu-id="28eb1-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="28eb1-123">None</span></span>

## <span data-ttu-id="28eb1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28eb1-124">OUTPUTS</span></span>

### <span data-ttu-id="28eb1-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="28eb1-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="28eb1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28eb1-126">NOTES</span></span>

## <span data-ttu-id="28eb1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28eb1-127">RELATED LINKS</span></span>
