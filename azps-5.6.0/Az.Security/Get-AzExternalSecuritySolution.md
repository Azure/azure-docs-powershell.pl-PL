---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: a39fdd3c61c7060eec38d93f4d8ae07b6c9a1105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995968"
---
# <span data-ttu-id="f1c57-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f1c57-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="f1c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c57-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c57-103">Uzyskaj rozwiązanie do zabezpieczeń zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="f1c57-103">Get external security solution</span></span> 

## <span data-ttu-id="f1c57-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1c57-104">SYNTAX</span></span>

### <span data-ttu-id="f1c57-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f1c57-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c57-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f1c57-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c57-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f1c57-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1c57-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c57-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1c57-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1c57-109">DESCRIPTION</span></span>
<span data-ttu-id="f1c57-110">Uzyskaj rozwiązanie do zabezpieczeń zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="f1c57-110">Get external security solution</span></span>

## <span data-ttu-id="f1c57-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1c57-111">EXAMPLES</span></span>

### <span data-ttu-id="f1c57-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1c57-112">Example 1</span></span>
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

<span data-ttu-id="f1c57-113">Pobierz wszystkie zewnętrzne rozwiązania zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f1c57-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="f1c57-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f1c57-114">Example 2</span></span>
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

<span data-ttu-id="f1c57-115">Uzyskaj konkretne rozwiązanie do zabezpieczeń zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="f1c57-115">Get a specific external security solution</span></span>

## <span data-ttu-id="f1c57-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1c57-116">PARAMETERS</span></span>

### <span data-ttu-id="f1c57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c57-117">-DefaultProfile</span></span>
<span data-ttu-id="f1c57-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c57-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f1c57-119">-Location</span></span>
<span data-ttu-id="f1c57-120">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="f1c57-120">Location.</span></span>

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

### <span data-ttu-id="f1c57-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1c57-121">-Name</span></span>
<span data-ttu-id="f1c57-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f1c57-122">Resource name.</span></span>

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

### <span data-ttu-id="f1c57-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c57-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1c57-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1c57-124">Resource group name.</span></span>

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

### <span data-ttu-id="f1c57-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c57-125">-ResourceId</span></span>
<span data-ttu-id="f1c57-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f1c57-126">Resource ID.</span></span>

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

### <span data-ttu-id="f1c57-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c57-127">CommonParameters</span></span>
<span data-ttu-id="f1c57-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c57-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c57-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1c57-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c57-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1c57-130">INPUTS</span></span>

### <span data-ttu-id="f1c57-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f1c57-131">System.String</span></span>

## <span data-ttu-id="f1c57-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1c57-132">OUTPUTS</span></span>

### <span data-ttu-id="f1c57-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f1c57-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="f1c57-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1c57-134">NOTES</span></span>

## <span data-ttu-id="f1c57-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1c57-135">RELATED LINKS</span></span>
