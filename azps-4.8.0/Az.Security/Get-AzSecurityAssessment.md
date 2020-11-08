---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063228"
---
# <span data-ttu-id="442f6-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="442f6-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="442f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="442f6-102">SYNOPSIS</span></span>
<span data-ttu-id="442f6-103">Pobiera oceny zabezpieczeń i ich wyniki w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="442f6-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="442f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="442f6-104">SYNTAX</span></span>

### <span data-ttu-id="442f6-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="442f6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442f6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="442f6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442f6-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="442f6-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="442f6-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="442f6-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="442f6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="442f6-109">DESCRIPTION</span></span>
<span data-ttu-id="442f6-110">Pobiera ocenę zabezpieczeń i ich wyniki na abonament.</span><span class="sxs-lookup"><span data-stu-id="442f6-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="442f6-111">Oceny zabezpieczeń umożliwiają zapoznanie się z najważniejszymi wskazówkami dla usługi Azure Security Center, które zostaną złagodzone w ramach subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="442f6-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="442f6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="442f6-112">EXAMPLES</span></span>

### <span data-ttu-id="442f6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="442f6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="442f6-114">Pobiera wszystkie oceny zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="442f6-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="442f6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="442f6-115">PARAMETERS</span></span>

### <span data-ttu-id="442f6-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="442f6-116">-AssessedResourceId</span></span>
<span data-ttu-id="442f6-117">Pełny identyfikator zasobu, dla którego jest obliczana Ocena.</span><span class="sxs-lookup"><span data-stu-id="442f6-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442f6-118">-DefaultProfile</span></span>
<span data-ttu-id="442f6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="442f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442f6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="442f6-120">-Name</span></span>
<span data-ttu-id="442f6-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="442f6-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442f6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="442f6-122">-ResourceId</span></span>
<span data-ttu-id="442f6-123">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="442f6-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="442f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442f6-124">CommonParameters</span></span>
<span data-ttu-id="442f6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442f6-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="442f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442f6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="442f6-127">INPUTS</span></span>

### <span data-ttu-id="442f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="442f6-128">System.String</span></span>

## <span data-ttu-id="442f6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="442f6-129">OUTPUTS</span></span>

### <span data-ttu-id="442f6-130">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="442f6-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="442f6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="442f6-131">NOTES</span></span>

## <span data-ttu-id="442f6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="442f6-132">RELATED LINKS</span></span>
