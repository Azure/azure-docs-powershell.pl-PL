---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197938"
---
# <span data-ttu-id="269f5-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="269f5-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="269f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="269f5-102">SYNOPSIS</span></span>
<span data-ttu-id="269f5-103">Pobiera typy i metadta oceny zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="269f5-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="269f5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="269f5-104">SYNTAX</span></span>

### <span data-ttu-id="269f5-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="269f5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="269f5-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="269f5-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="269f5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="269f5-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="269f5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="269f5-108">DESCRIPTION</span></span>
<span data-ttu-id="269f5-109">Pobiera typy i metadta oceny zabezpieczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="269f5-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="269f5-110">Metadane oceny zabezpieczeń obejmują Built-In oceny i niestandardowe typy formularzy oceniania, które użytkownik może zdefiniować.</span><span class="sxs-lookup"><span data-stu-id="269f5-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="269f5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="269f5-111">EXAMPLES</span></span>

### <span data-ttu-id="269f5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="269f5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="269f5-113">Pobiera wszystkie wbudowane testy i oceny niestandardowe skonfigurowane w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="269f5-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="269f5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="269f5-114">PARAMETERS</span></span>

### <span data-ttu-id="269f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="269f5-115">-DefaultProfile</span></span>
<span data-ttu-id="269f5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="269f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="269f5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="269f5-117">-Name</span></span>
<span data-ttu-id="269f5-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="269f5-118">Resource name.</span></span>

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

### <span data-ttu-id="269f5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="269f5-119">-ResourceId</span></span>
<span data-ttu-id="269f5-120">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="269f5-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="269f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269f5-121">CommonParameters</span></span>
<span data-ttu-id="269f5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="269f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269f5-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="269f5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269f5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="269f5-124">INPUTS</span></span>

### <span data-ttu-id="269f5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="269f5-125">System.String</span></span>

## <span data-ttu-id="269f5-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="269f5-126">OUTPUTS</span></span>

### <span data-ttu-id="269f5-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="269f5-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="269f5-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="269f5-128">NOTES</span></span>

## <span data-ttu-id="269f5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="269f5-129">RELATED LINKS</span></span>
