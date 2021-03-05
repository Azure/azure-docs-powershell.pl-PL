---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 677c67ecc2418a4940b4cbe79e2ac7145eada0c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984154"
---
# <span data-ttu-id="2d9f9-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2d9f9-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="2d9f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9f9-103">Utwórz nową konfigurację zaleceń dla rozwiązania zabezpieczeń iot</span><span class="sxs-lookup"><span data-stu-id="2d9f9-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="2d9f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d9f9-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d9f9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d9f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9f9-106">AzIotSecuritySolutionRecommendationConfigurationObject tworzy nowy obiekt konfiguracji zalecenia dla rozwiązania zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="2d9f9-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="2d9f9-107">W ten sposób jest skonfigurowany stan zalecenia, niezależnie od tego, czy zostało włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="2d9f9-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="2d9f9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d9f9-108">EXAMPLES</span></span>

### <span data-ttu-id="2d9f9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d9f9-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="2d9f9-110">Utwórz nową konfigurację rekomendacji dla typu IoT_ACRAuthentication "IoT_ACRAuthentication" ze statusem ustawionym na wyłączenie</span><span class="sxs-lookup"><span data-stu-id="2d9f9-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="2d9f9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d9f9-111">PARAMETERS</span></span>

### <span data-ttu-id="2d9f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9f9-112">-DefaultProfile</span></span>
<span data-ttu-id="2d9f9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d9f9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d9f9-114">— włączone</span><span class="sxs-lookup"><span data-stu-id="2d9f9-114">-Enabled</span></span>
<span data-ttu-id="2d9f9-115">Stan.</span><span class="sxs-lookup"><span data-stu-id="2d9f9-115">Status .</span></span>

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

### <span data-ttu-id="2d9f9-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="2d9f9-116">-RecommendationType</span></span>
<span data-ttu-id="2d9f9-117">Typ zalecenia.</span><span class="sxs-lookup"><span data-stu-id="2d9f9-117">Recommendation type.</span></span>

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

### <span data-ttu-id="2d9f9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9f9-118">CommonParameters</span></span>
<span data-ttu-id="2d9f9-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d9f9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9f9-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d9f9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9f9-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d9f9-121">INPUTS</span></span>

### <span data-ttu-id="2d9f9-122">Brak</span><span class="sxs-lookup"><span data-stu-id="2d9f9-122">None</span></span>

## <span data-ttu-id="2d9f9-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d9f9-123">OUTPUTS</span></span>

### <span data-ttu-id="2d9f9-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d9f9-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="2d9f9-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d9f9-125">NOTES</span></span>

## <span data-ttu-id="2d9f9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d9f9-126">RELATED LINKS</span></span>
