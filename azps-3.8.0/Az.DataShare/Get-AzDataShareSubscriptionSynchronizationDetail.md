---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: ffa9de86a7ebbb70361752b8c7733129eb024845
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895449"
---
# <span data-ttu-id="c1743-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="c1743-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="c1743-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1743-102">SYNOPSIS</span></span>
<span data-ttu-id="c1743-103">Pobiera informacje o synchonizationie subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="c1743-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="c1743-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1743-104">SYNTAX</span></span>

### <span data-ttu-id="c1743-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c1743-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1743-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1743-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1743-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c1743-107">DESCRIPTION</span></span>
<span data-ttu-id="c1743-108">Polecenie cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** zawiera szczegółowe informacje o synchronizacji zainicjowanej dla subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="c1743-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="c1743-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1743-109">EXAMPLES</span></span>

### <span data-ttu-id="c1743-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1743-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="c1743-111">To polecenie zawiera informacje na temat synchronizacji zainicjowanej dla subskrypcji udziału AdsShareSubscription w obszarze WikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="c1743-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="c1743-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1743-112">PARAMETERS</span></span>

### <span data-ttu-id="c1743-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1743-113">-AccountName</span></span>
<span data-ttu-id="c1743-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="c1743-114">Azure data share account name</span></span>

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

### <span data-ttu-id="c1743-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1743-115">-DefaultProfile</span></span>
<span data-ttu-id="c1743-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1743-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1743-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1743-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1743-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="c1743-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c1743-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1743-119">-ResourceId</span></span>
<span data-ttu-id="c1743-120">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="c1743-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="c1743-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c1743-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="c1743-122">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="c1743-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c1743-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="c1743-123">-SynchronizationId</span></span>
<span data-ttu-id="c1743-124">Identyfikator synchronizacji synchronizacji subskrypcji udziału</span><span class="sxs-lookup"><span data-stu-id="c1743-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="c1743-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1743-125">CommonParameters</span></span>
<span data-ttu-id="c1743-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1743-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1743-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1743-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1743-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1743-128">INPUTS</span></span>

### <span data-ttu-id="c1743-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c1743-129">System.String</span></span>

## <span data-ttu-id="c1743-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1743-130">OUTPUTS</span></span>

### <span data-ttu-id="c1743-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="c1743-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="c1743-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1743-132">NOTES</span></span>

## <span data-ttu-id="c1743-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1743-133">RELATED LINKS</span></span>
