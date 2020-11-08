---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222948"
---
# <span data-ttu-id="4f5a9-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4f5a9-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="4f5a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5a9-103">Tworzenie nowej konfiguracji rekomendacji dotyczącej rozwiązania zabezpieczającego IoT</span><span class="sxs-lookup"><span data-stu-id="4f5a9-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="4f5a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f5a9-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f5a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4f5a9-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5a9-106">AzIotSecuritySolutionRecommendationConfigurationObject tworzy nowy obiekt konfiguracji rekomendacji dla rozwiązania zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="4f5a9-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="4f5a9-107">W ten sposób jest konfigurowany stan rekomendacji, niezależnie od tego, czy jest włączony, czy wyłączony.</span><span class="sxs-lookup"><span data-stu-id="4f5a9-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="4f5a9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f5a9-108">EXAMPLES</span></span>

### <span data-ttu-id="4f5a9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4f5a9-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="4f5a9-110">Tworzenie nowej konfiguracji rekomendacji dla typu rekomendacji "IoT_ACRAuthentication" z ustawionym stanem wyłączone</span><span class="sxs-lookup"><span data-stu-id="4f5a9-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="4f5a9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f5a9-111">PARAMETERS</span></span>

### <span data-ttu-id="4f5a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5a9-112">-DefaultProfile</span></span>
<span data-ttu-id="4f5a9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5a9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f5a9-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4f5a9-114">-Enabled</span></span>
<span data-ttu-id="4f5a9-115">Stan.</span><span class="sxs-lookup"><span data-stu-id="4f5a9-115">Status .</span></span>

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

### <span data-ttu-id="4f5a9-116">-Rekomendacja</span><span class="sxs-lookup"><span data-stu-id="4f5a9-116">-RecommendationType</span></span>
<span data-ttu-id="4f5a9-117">Typ rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="4f5a9-117">Recommendation type.</span></span>

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

### <span data-ttu-id="4f5a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5a9-118">CommonParameters</span></span>
<span data-ttu-id="4f5a9-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5a9-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f5a9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5a9-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f5a9-121">INPUTS</span></span>

### <span data-ttu-id="4f5a9-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4f5a9-122">None</span></span>

## <span data-ttu-id="4f5a9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f5a9-123">OUTPUTS</span></span>

### <span data-ttu-id="4f5a9-124">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f5a9-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="4f5a9-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f5a9-125">NOTES</span></span>

## <span data-ttu-id="4f5a9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f5a9-126">RELATED LINKS</span></span>
