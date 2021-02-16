---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242379"
---
# <span data-ttu-id="f5f26-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="f5f26-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="f5f26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5f26-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f26-103">Tworzenie nowych zasobów zdefiniowanych przez użytkownika dla rozwiązania zabezpieczeń IOT</span><span class="sxs-lookup"><span data-stu-id="f5f26-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="f5f26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5f26-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f26-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5f26-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f26-106">Polecenie cmdlet AzIotSecuritySolutionUserDefinedResourcesObject tworzy nowy obiekt zasobów zdefiniowanych przez użytkownika dla rozwiązania zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="f5f26-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="f5f26-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5f26-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f26-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5f26-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="f5f26-109">Tworzenie nowych zasobów zdefiniowanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="f5f26-109">Create new user defined resources</span></span>

## <span data-ttu-id="f5f26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5f26-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f26-111">-DefaultProfile</span></span>
<span data-ttu-id="f5f26-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5f26-113">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="f5f26-113">-Query</span></span>
<span data-ttu-id="f5f26-114">Zapytanie.</span><span class="sxs-lookup"><span data-stu-id="f5f26-114">Query.</span></span>

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

### <span data-ttu-id="f5f26-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="f5f26-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="f5f26-116">Zapytania dotyczące subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f5f26-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="f5f26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f26-117">CommonParameters</span></span>
<span data-ttu-id="f5f26-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f26-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5f26-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f26-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f26-120">INPUTS</span></span>

### <span data-ttu-id="f5f26-121">Brak</span><span class="sxs-lookup"><span data-stu-id="f5f26-121">None</span></span>

## <span data-ttu-id="f5f26-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5f26-122">OUTPUTS</span></span>

### <span data-ttu-id="f5f26-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="f5f26-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="f5f26-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5f26-124">NOTES</span></span>

## <span data-ttu-id="f5f26-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5f26-125">RELATED LINKS</span></span>
