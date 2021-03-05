---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: f0de174ac85fb4247ac8af55f8a8ab9cb64d6446
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973505"
---
# <span data-ttu-id="e0ffd-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e0ffd-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e0ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ffd-103">Pobiera skonfigurowane ustawienia obszaru roboczego zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="e0ffd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0ffd-104">SYNTAX</span></span>

### <span data-ttu-id="e0ffd-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e0ffd-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ffd-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e0ffd-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ffd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ffd-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ffd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0ffd-108">DESCRIPTION</span></span>
<span data-ttu-id="e0ffd-109">To polecenie cmdlet umożliwia odnajdowanie skonfigurowanego obszaru roboczego, który będzie zawierać dane zabezpieczeń, które zostały zebrane przez agenta zabezpieczeń zainstalowanego w maszyny wirtualnej w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="e0ffd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0ffd-110">EXAMPLES</span></span>

### <span data-ttu-id="e0ffd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0ffd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="e0ffd-112">Pobiera ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="e0ffd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0ffd-113">PARAMETERS</span></span>

### <span data-ttu-id="e0ffd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ffd-114">-DefaultProfile</span></span>
<span data-ttu-id="e0ffd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ffd-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0ffd-116">-Name</span></span>
<span data-ttu-id="e0ffd-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ffd-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ffd-118">-ResourceId</span></span>
<span data-ttu-id="e0ffd-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-119">Resource ID.</span></span>

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

### <span data-ttu-id="e0ffd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ffd-120">CommonParameters</span></span>
<span data-ttu-id="e0ffd-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ffd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ffd-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ffd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ffd-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ffd-123">INPUTS</span></span>

### <span data-ttu-id="e0ffd-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ffd-124">System.String</span></span>

## <span data-ttu-id="e0ffd-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ffd-125">OUTPUTS</span></span>

### <span data-ttu-id="e0ffd-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e0ffd-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e0ffd-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0ffd-127">NOTES</span></span>

## <span data-ttu-id="e0ffd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0ffd-128">RELATED LINKS</span></span>
