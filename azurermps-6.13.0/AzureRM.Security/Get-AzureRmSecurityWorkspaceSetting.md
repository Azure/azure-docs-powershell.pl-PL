---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717372"
---
# <span data-ttu-id="b6c13-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b6c13-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b6c13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6c13-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c13-103">Pobiera skonfigurowane ustawienia obszaru roboczego zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6c13-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6c13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6c13-104">SYNTAX</span></span>

### <span data-ttu-id="b6c13-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6c13-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c13-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b6c13-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6c13-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b6c13-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6c13-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b6c13-108">DESCRIPTION</span></span>
<span data-ttu-id="b6c13-109">To polecenie cmdlet umożliwia odnajdowanie skonfigurowanego obszaru roboczego, który będzie zawierać dane zabezpieczeń, które zostały pobrane przez agenta zabezpieczeń zainstalowanego na maszynach wirtualnych w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6c13-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="b6c13-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6c13-110">EXAMPLES</span></span>

### <span data-ttu-id="b6c13-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6c13-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="b6c13-112">Pobiera ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6c13-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="b6c13-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6c13-113">PARAMETERS</span></span>

### <span data-ttu-id="b6c13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c13-114">-DefaultProfile</span></span>
<span data-ttu-id="b6c13-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c13-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6c13-116">-Name</span></span>
<span data-ttu-id="b6c13-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b6c13-117">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c13-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c13-118">-ResourceId</span></span>
<span data-ttu-id="b6c13-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b6c13-119">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c13-120">CommonParameters</span></span>
<span data-ttu-id="b6c13-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c13-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c13-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c13-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6c13-123">INPUTS</span></span>

### <span data-ttu-id="b6c13-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c13-124">System.String</span></span>

## <span data-ttu-id="b6c13-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6c13-125">OUTPUTS</span></span>

### <span data-ttu-id="b6c13-126">Microsoft. Azure. Commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b6c13-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b6c13-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6c13-127">NOTES</span></span>

## <span data-ttu-id="b6c13-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6c13-128">RELATED LINKS</span></span>
