---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 92858967d460785af151520c504a4e1cbdb4d3d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008522"
---
# <span data-ttu-id="298a3-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="298a3-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="298a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="298a3-102">SYNOPSIS</span></span>
<span data-ttu-id="298a3-103">Pobiera typy i metadta oceny zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="298a3-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="298a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="298a3-104">SYNTAX</span></span>

### <span data-ttu-id="298a3-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="298a3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="298a3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="298a3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="298a3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="298a3-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="298a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="298a3-108">DESCRIPTION</span></span>
<span data-ttu-id="298a3-109">Pobiera typy i metadta oceny zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="298a3-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="298a3-110">Metadane oceny zabezpieczeń obejmują Built-In oceny i niestandardowe typy formularzy oceniania, które użytkownik może zdefiniować.</span><span class="sxs-lookup"><span data-stu-id="298a3-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="298a3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="298a3-111">EXAMPLES</span></span>

### <span data-ttu-id="298a3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="298a3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="298a3-113">Pobiera wszystkie wbudowane oceny i oceny niestandardowe skonfigurowane w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="298a3-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="298a3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="298a3-114">PARAMETERS</span></span>

### <span data-ttu-id="298a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298a3-115">-DefaultProfile</span></span>
<span data-ttu-id="298a3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="298a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298a3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="298a3-117">-Name</span></span>
<span data-ttu-id="298a3-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="298a3-118">Resource name.</span></span>

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

### <span data-ttu-id="298a3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="298a3-119">-ResourceId</span></span>
<span data-ttu-id="298a3-120">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="298a3-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="298a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298a3-121">CommonParameters</span></span>
<span data-ttu-id="298a3-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="298a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298a3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="298a3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298a3-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="298a3-124">INPUTS</span></span>

### <span data-ttu-id="298a3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="298a3-125">System.String</span></span>

## <span data-ttu-id="298a3-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="298a3-126">OUTPUTS</span></span>

### <span data-ttu-id="298a3-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="298a3-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="298a3-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="298a3-128">NOTES</span></span>

## <span data-ttu-id="298a3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="298a3-129">RELATED LINKS</span></span>
