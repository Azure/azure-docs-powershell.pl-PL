---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323237"
---
# <span data-ttu-id="002fa-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="002fa-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="002fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="002fa-102">SYNOPSIS</span></span>
<span data-ttu-id="002fa-103">Pobiera typy oceny zabezpieczeń i metadta w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="002fa-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="002fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="002fa-104">SYNTAX</span></span>

### <span data-ttu-id="002fa-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="002fa-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="002fa-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="002fa-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="002fa-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="002fa-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="002fa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="002fa-108">DESCRIPTION</span></span>
<span data-ttu-id="002fa-109">Pobiera typy oceny zabezpieczeń i metadta w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="002fa-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="002fa-110">Metadane oceny bezpieczeństwa obejmują oceny Built-In i niestandardowe typy ocen, które użytkownik może zdefiniować.</span><span class="sxs-lookup"><span data-stu-id="002fa-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="002fa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="002fa-111">EXAMPLES</span></span>

### <span data-ttu-id="002fa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="002fa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="002fa-113">Pobiera wszystkie wbudowane oceny oraz oceny niestandardowe skonfigurowane w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="002fa-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="002fa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="002fa-114">PARAMETERS</span></span>

### <span data-ttu-id="002fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002fa-115">-DefaultProfile</span></span>
<span data-ttu-id="002fa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="002fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="002fa-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="002fa-117">-Name</span></span>
<span data-ttu-id="002fa-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="002fa-118">Resource name.</span></span>

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

### <span data-ttu-id="002fa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="002fa-119">-ResourceId</span></span>
<span data-ttu-id="002fa-120">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="002fa-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="002fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002fa-121">CommonParameters</span></span>
<span data-ttu-id="002fa-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002fa-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="002fa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002fa-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="002fa-124">INPUTS</span></span>

### <span data-ttu-id="002fa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="002fa-125">System.String</span></span>

## <span data-ttu-id="002fa-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="002fa-126">OUTPUTS</span></span>

### <span data-ttu-id="002fa-127">Microsoft. Azure. Commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="002fa-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="002fa-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="002fa-128">NOTES</span></span>

## <span data-ttu-id="002fa-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="002fa-129">RELATED LINKS</span></span>
