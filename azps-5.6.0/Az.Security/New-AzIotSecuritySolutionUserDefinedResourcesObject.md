---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: 2b524234b18e84247c3789119fbfe1d214514fec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984145"
---
# <span data-ttu-id="06953-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="06953-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="06953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06953-102">SYNOPSIS</span></span>
<span data-ttu-id="06953-103">Tworzenie nowych zasobów zdefiniowanych przez użytkownika dla rozwiązania zabezpieczeń IOT</span><span class="sxs-lookup"><span data-stu-id="06953-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="06953-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06953-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06953-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06953-105">DESCRIPTION</span></span>
<span data-ttu-id="06953-106">Polecenie cmdlet AzIotSecuritySolutionUserDefinedResourcesObject tworzy nowy obiekt zasobów zdefiniowany przez użytkownika dla rozwiązania zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="06953-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="06953-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06953-107">EXAMPLES</span></span>

### <span data-ttu-id="06953-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06953-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="06953-109">Tworzenie nowych zasobów zdefiniowanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="06953-109">Create new user defined resources</span></span>

## <span data-ttu-id="06953-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06953-110">PARAMETERS</span></span>

### <span data-ttu-id="06953-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06953-111">-DefaultProfile</span></span>
<span data-ttu-id="06953-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06953-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06953-113">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="06953-113">-Query</span></span>
<span data-ttu-id="06953-114">Zapytanie.</span><span class="sxs-lookup"><span data-stu-id="06953-114">Query.</span></span>

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

### <span data-ttu-id="06953-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="06953-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="06953-116">Zapytania dotyczące subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="06953-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="06953-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06953-117">CommonParameters</span></span>
<span data-ttu-id="06953-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06953-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06953-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06953-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06953-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06953-120">INPUTS</span></span>

### <span data-ttu-id="06953-121">Brak</span><span class="sxs-lookup"><span data-stu-id="06953-121">None</span></span>

## <span data-ttu-id="06953-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06953-122">OUTPUTS</span></span>

### <span data-ttu-id="06953-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="06953-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="06953-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06953-124">NOTES</span></span>

## <span data-ttu-id="06953-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06953-125">RELATED LINKS</span></span>
