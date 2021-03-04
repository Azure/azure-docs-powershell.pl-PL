---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 4777b7becf1d0e08d88035253a314a21301bae04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957281"
---
# <span data-ttu-id="585d9-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="585d9-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="585d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="585d9-102">SYNOPSIS</span></span>
<span data-ttu-id="585d9-103">Otrzymuje informacje na temat udostępniania subskrypcji na koncie udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="585d9-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="585d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="585d9-104">SYNTAX</span></span>

### <span data-ttu-id="585d9-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="585d9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="585d9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="585d9-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="585d9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="585d9-107">DESCRIPTION</span></span>
<span data-ttu-id="585d9-108">Polecenie **cmdlet Get-AzDataShareSubscription** dostarcza informacji o subskrypcji udostępniania na koncie udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="585d9-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="585d9-109">Jeśli podano nazwę subskrypcji udostępniania, polecenie cmdlet zawiera informacje o określonej subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="585d9-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="585d9-110">W przeciwnym razie polecenie cmdlet udostępnia listę subskrypcji udostępniania na koncie udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="585d9-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="585d9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="585d9-111">EXAMPLES</span></span>

### <span data-ttu-id="585d9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="585d9-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="585d9-113">To polecenie zawiera informacje o udostępnianiu subskrypcji AdsShareSubscription w danych współużytkowania konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="585d9-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="585d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="585d9-114">PARAMETERS</span></span>

### <span data-ttu-id="585d9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="585d9-115">-AccountName</span></span>
<span data-ttu-id="585d9-116">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="585d9-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585d9-117">-DefaultProfile</span></span>
<span data-ttu-id="585d9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="585d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="585d9-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="585d9-119">-Name</span></span>
<span data-ttu-id="585d9-120">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="585d9-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="585d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="585d9-122">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="585d9-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="585d9-123">-ResourceId</span></span>
<span data-ttu-id="585d9-124">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="585d9-124">The resource id of the azure data share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585d9-125">CommonParameters</span></span>
<span data-ttu-id="585d9-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585d9-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="585d9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585d9-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="585d9-128">INPUTS</span></span>

### <span data-ttu-id="585d9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="585d9-129">System.String</span></span>

## <span data-ttu-id="585d9-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="585d9-130">OUTPUTS</span></span>

### <span data-ttu-id="585d9-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="585d9-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="585d9-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="585d9-132">NOTES</span></span>

## <span data-ttu-id="585d9-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="585d9-133">RELATED LINKS</span></span>
