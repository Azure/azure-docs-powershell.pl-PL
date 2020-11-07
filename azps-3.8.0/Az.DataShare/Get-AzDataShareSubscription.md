---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: ba4fc6a58cd345c149e551263ddf5880f099a54e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895245"
---
# <span data-ttu-id="16e78-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="16e78-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="16e78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16e78-102">SYNOPSIS</span></span>
<span data-ttu-id="16e78-103">Pobiera informacje o subskrypcji udziału w koncie udziału danych.</span><span class="sxs-lookup"><span data-stu-id="16e78-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="16e78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16e78-104">SYNTAX</span></span>

### <span data-ttu-id="16e78-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16e78-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16e78-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e78-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16e78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="16e78-107">DESCRIPTION</span></span>
<span data-ttu-id="16e78-108">Polecenie cmdlet **Get-AzDataShareSubscription** zawiera informacje dotyczące udostępniania subskrypcji na koncie udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="16e78-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="16e78-109">Jeśli jest podana nazwa subskrypcji udziału, polecenie cmdlet udostępnia informacje dotyczące konkretnej subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="16e78-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="16e78-110">W przeciwnym razie polecenie cmdlet udostępnia listę abonamentów udostępniania na koncie udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="16e78-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="16e78-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16e78-111">EXAMPLES</span></span>

### <span data-ttu-id="16e78-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16e78-112">Example 1</span></span>
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

<span data-ttu-id="16e78-113">To polecenie zawiera informacje dotyczące udostępniania AdsShareSubscription subskrypcji w WikiAds kont udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="16e78-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="16e78-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16e78-114">PARAMETERS</span></span>

### <span data-ttu-id="16e78-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16e78-115">-AccountName</span></span>
<span data-ttu-id="16e78-116">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="16e78-116">Azure data share account name</span></span>

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

### <span data-ttu-id="16e78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e78-117">-DefaultProfile</span></span>
<span data-ttu-id="16e78-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16e78-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e78-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16e78-119">-Name</span></span>
<span data-ttu-id="16e78-120">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="16e78-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="16e78-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e78-121">-ResourceGroupName</span></span>
<span data-ttu-id="16e78-122">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="16e78-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="16e78-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e78-123">-ResourceId</span></span>
<span data-ttu-id="16e78-124">Identyfikator zasobu subskrypcji udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="16e78-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="16e78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e78-125">CommonParameters</span></span>
<span data-ttu-id="16e78-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e78-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e78-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e78-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16e78-128">INPUTS</span></span>

### <span data-ttu-id="16e78-129">System. String</span><span class="sxs-lookup"><span data-stu-id="16e78-129">System.String</span></span>

## <span data-ttu-id="16e78-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16e78-130">OUTPUTS</span></span>

### <span data-ttu-id="16e78-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="16e78-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="16e78-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16e78-132">NOTES</span></span>

## <span data-ttu-id="16e78-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16e78-133">RELATED LINKS</span></span>
