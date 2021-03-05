---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: 0f46a0f009085aa7ef7b66ac91d621338a7358b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979281"
---
# <span data-ttu-id="d9050-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="d9050-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="d9050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9050-102">SYNOPSIS</span></span>
<span data-ttu-id="d9050-103">Utwórz nową niestandardową regułę alertu listy zezwalania dla grupy zabezpieczeń urządzenia (Zabezpieczenia IoT)</span><span class="sxs-lookup"><span data-stu-id="d9050-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d9050-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9050-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9050-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9050-105">DESCRIPTION</span></span>
<span data-ttu-id="d9050-106">Polecenie New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet tworzy nową listę dozwolonych niestandardowych reguł alertów dla grupy zabezpieczeń urządzeń w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="d9050-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d9050-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9050-107">EXAMPLES</span></span>

### <span data-ttu-id="d9050-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9050-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="d9050-109">Tworzenie nowej listy alertów niestandardowych z typu "LocalUserNotAllowed" z ustawionym stanem wyłączenia</span><span class="sxs-lookup"><span data-stu-id="d9050-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="d9050-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9050-110">PARAMETERS</span></span>

### <span data-ttu-id="d9050-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="d9050-111">-AllowlistValue</span></span>
<span data-ttu-id="d9050-112">Zezwalaj na wartości listy.</span><span class="sxs-lookup"><span data-stu-id="d9050-112">Allow list values.</span></span>

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

### <span data-ttu-id="d9050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9050-113">-DefaultProfile</span></span>
<span data-ttu-id="d9050-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9050-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9050-115">— włączone</span><span class="sxs-lookup"><span data-stu-id="d9050-115">-Enabled</span></span>
<span data-ttu-id="d9050-116">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d9050-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="d9050-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d9050-117">-Type</span></span>
<span data-ttu-id="d9050-118">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="d9050-118">Rule type.</span></span>

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

### <span data-ttu-id="d9050-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9050-119">CommonParameters</span></span>
<span data-ttu-id="d9050-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9050-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9050-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9050-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9050-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9050-122">INPUTS</span></span>

### <span data-ttu-id="d9050-123">Brak</span><span class="sxs-lookup"><span data-stu-id="d9050-123">None</span></span>

## <span data-ttu-id="d9050-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9050-124">OUTPUTS</span></span>

### <span data-ttu-id="d9050-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d9050-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="d9050-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9050-126">NOTES</span></span>

## <span data-ttu-id="d9050-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9050-127">RELATED LINKS</span></span>
