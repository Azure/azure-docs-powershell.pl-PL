---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062114"
---
# <span data-ttu-id="cfaea-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="cfaea-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="cfaea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfaea-102">SYNOPSIS</span></span>
<span data-ttu-id="cfaea-103">Uzyskiwanie rozwiązania dotyczącego zabezpieczeń zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="cfaea-103">Get external security solution</span></span> 

## <span data-ttu-id="cfaea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfaea-104">SYNTAX</span></span>

### <span data-ttu-id="cfaea-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cfaea-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaea-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="cfaea-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaea-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="cfaea-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfaea-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="cfaea-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfaea-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cfaea-109">DESCRIPTION</span></span>
<span data-ttu-id="cfaea-110">Uzyskiwanie rozwiązania dotyczącego zabezpieczeń zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="cfaea-110">Get external security solution</span></span>

## <span data-ttu-id="cfaea-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfaea-111">EXAMPLES</span></span>

### <span data-ttu-id="cfaea-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cfaea-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="cfaea-113">Uzyskaj wszystkie rozwiązania dotyczące zabezpieczeń zewnętrznych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cfaea-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="cfaea-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cfaea-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="cfaea-115">Uzyskiwanie określonego zewnętrznego rozwiązania dotyczącego zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="cfaea-115">Get a specific external security solution</span></span>

## <span data-ttu-id="cfaea-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfaea-116">PARAMETERS</span></span>

### <span data-ttu-id="cfaea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfaea-117">-DefaultProfile</span></span>
<span data-ttu-id="cfaea-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfaea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfaea-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cfaea-119">-Location</span></span>
<span data-ttu-id="cfaea-120">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="cfaea-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfaea-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfaea-121">-Name</span></span>
<span data-ttu-id="cfaea-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cfaea-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfaea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfaea-123">-ResourceGroupName</span></span>
<span data-ttu-id="cfaea-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cfaea-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfaea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfaea-125">-ResourceId</span></span>
<span data-ttu-id="cfaea-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cfaea-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfaea-127">CommonParameters</span></span>
<span data-ttu-id="cfaea-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfaea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfaea-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfaea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfaea-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfaea-130">INPUTS</span></span>

### <span data-ttu-id="cfaea-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cfaea-131">System.String</span></span>

## <span data-ttu-id="cfaea-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfaea-132">OUTPUTS</span></span>

### <span data-ttu-id="cfaea-133">Microsoft. Azure. Commands. Security. models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="cfaea-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="cfaea-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfaea-134">NOTES</span></span>

## <span data-ttu-id="cfaea-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfaea-135">RELATED LINKS</span></span>
