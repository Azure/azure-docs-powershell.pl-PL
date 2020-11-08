---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234417"
---
# <span data-ttu-id="b9b3d-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="b9b3d-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="b9b3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b3d-103">Utwórz nową regułę alertu niestandardowego listy dozwolonych dla grupy zabezpieczeń urządzenia (z zabezpieczeniami IoT)</span><span class="sxs-lookup"><span data-stu-id="b9b3d-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="b9b3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9b3d-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9b3d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b9b3d-106">Polecenie cmdlet New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject tworzy nową listę dozwolonych niestandardowych reguł alertów dla grupy zabezpieczeń urządzenia w rozwiązaniu bezpieczeństwa IoT.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="b9b3d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9b3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b9b3d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9b3d-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="b9b3d-109">Utwórz nową Rull alertu niestandardowego listy dozwolonych z typu "LocalUserNotAllowed" z ustawionym stanem wyłączone</span><span class="sxs-lookup"><span data-stu-id="b9b3d-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="b9b3d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9b3d-110">PARAMETERS</span></span>

### <span data-ttu-id="b9b3d-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="b9b3d-111">-AllowlistValue</span></span>
<span data-ttu-id="b9b3d-112">Dozwolone wartości listy.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-112">Allow list values.</span></span>

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

### <span data-ttu-id="b9b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="b9b3d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9b3d-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b9b3d-115">-Enabled</span></span>
<span data-ttu-id="b9b3d-116">Czy reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="b9b3d-117">-Type</span><span class="sxs-lookup"><span data-stu-id="b9b3d-117">-Type</span></span>
<span data-ttu-id="b9b3d-118">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-118">Rule type.</span></span>

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

### <span data-ttu-id="b9b3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b3d-119">CommonParameters</span></span>
<span data-ttu-id="b9b3d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b3d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9b3d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b3d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9b3d-122">INPUTS</span></span>

### <span data-ttu-id="b9b3d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9b3d-123">None</span></span>

## <span data-ttu-id="b9b3d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9b3d-124">OUTPUTS</span></span>

### <span data-ttu-id="b9b3d-125">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9b3d-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="b9b3d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9b3d-126">NOTES</span></span>

## <span data-ttu-id="b9b3d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9b3d-127">RELATED LINKS</span></span>
