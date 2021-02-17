---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: ca4f0d39b0023d641e2f95ceb4eddf90f19a51f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198730"
---
# <span data-ttu-id="191db-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="191db-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="191db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="191db-102">SYNOPSIS</span></span>
<span data-ttu-id="191db-103">Pobiera skonfigurowane ustawienia obszaru roboczego zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="191db-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="191db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="191db-104">SYNTAX</span></span>

### <span data-ttu-id="191db-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="191db-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="191db-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="191db-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="191db-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="191db-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="191db-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="191db-108">DESCRIPTION</span></span>
<span data-ttu-id="191db-109">To polecenie cmdlet umożliwia odnajdowanie skonfigurowanego obszaru roboczego, który będzie zawierać dane zabezpieczeń, które zostały zebrane przez agenta zabezpieczeń zainstalowanego w maszyny wirtualnej w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="191db-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="191db-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="191db-110">EXAMPLES</span></span>

### <span data-ttu-id="191db-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="191db-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="191db-112">Pobiera ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="191db-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="191db-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="191db-113">PARAMETERS</span></span>

### <span data-ttu-id="191db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191db-114">-DefaultProfile</span></span>
<span data-ttu-id="191db-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="191db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="191db-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="191db-116">-Name</span></span>
<span data-ttu-id="191db-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="191db-117">Resource name.</span></span>

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

### <span data-ttu-id="191db-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="191db-118">-ResourceId</span></span>
<span data-ttu-id="191db-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="191db-119">Resource ID.</span></span>

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

### <span data-ttu-id="191db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191db-120">CommonParameters</span></span>
<span data-ttu-id="191db-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191db-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="191db-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191db-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="191db-123">INPUTS</span></span>

### <span data-ttu-id="191db-124">System.String</span><span class="sxs-lookup"><span data-stu-id="191db-124">System.String</span></span>

## <span data-ttu-id="191db-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="191db-125">OUTPUTS</span></span>

### <span data-ttu-id="191db-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="191db-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="191db-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="191db-127">NOTES</span></span>

## <span data-ttu-id="191db-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="191db-128">RELATED LINKS</span></span>
