---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
ms.openlocfilehash: 1a1aa0675637bd5bbe8a8b0d4007ab426aba6592
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716920"
---
# <span data-ttu-id="467c8-101">Get-AzureRmSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="467c8-101">Get-AzureRmSecurityCompliance</span></span>

## <span data-ttu-id="467c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="467c8-102">SYNOPSIS</span></span>
<span data-ttu-id="467c8-103">Uzyskiwanie zgodności z zabezpieczeniami subskrypcji w czasie</span><span class="sxs-lookup"><span data-stu-id="467c8-103">Get the security compliance of a subscription over time</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="467c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="467c8-104">SYNTAX</span></span>

### <span data-ttu-id="467c8-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="467c8-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="467c8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="467c8-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="467c8-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="467c8-107">ResourceId</span></span>
```
Get-AzureRmSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="467c8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="467c8-108">DESCRIPTION</span></span>
<span data-ttu-id="467c8-109">Pobiera zgodność z zabezpieczeniami subskrypcji na podstawie bieżącego stosunku zasobów zdrowych i niezabezpieczonych w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="467c8-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="467c8-110">Zgodność zabezpieczeń jest obliczana codziennie, a historia jest zapisywana.</span><span class="sxs-lookup"><span data-stu-id="467c8-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="467c8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="467c8-111">EXAMPLES</span></span>

### <span data-ttu-id="467c8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="467c8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="467c8-113">Pobiera zgodność subskrypcji w ciągu ostatnich 14 dni</span><span class="sxs-lookup"><span data-stu-id="467c8-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="467c8-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="467c8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="467c8-115">Pobiera zgodność z zabezpieczeniami subskrypcji w określonym dniu</span><span class="sxs-lookup"><span data-stu-id="467c8-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="467c8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="467c8-116">PARAMETERS</span></span>

### <span data-ttu-id="467c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467c8-117">-DefaultProfile</span></span>
<span data-ttu-id="467c8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="467c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="467c8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="467c8-119">-Name</span></span>
<span data-ttu-id="467c8-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="467c8-120">Resource name.</span></span>

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

### <span data-ttu-id="467c8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="467c8-121">-ResourceId</span></span>
<span data-ttu-id="467c8-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="467c8-122">Resource ID.</span></span>

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

### <span data-ttu-id="467c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467c8-123">CommonParameters</span></span>
<span data-ttu-id="467c8-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467c8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467c8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467c8-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="467c8-126">INPUTS</span></span>

### <span data-ttu-id="467c8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="467c8-127">System.String</span></span>

## <span data-ttu-id="467c8-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="467c8-128">OUTPUTS</span></span>

### <span data-ttu-id="467c8-129">Microsoft. Azure. Commands. Security. MODELES. zgodności. PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="467c8-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="467c8-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="467c8-130">NOTES</span></span>

## <span data-ttu-id="467c8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="467c8-131">RELATED LINKS</span></span>
