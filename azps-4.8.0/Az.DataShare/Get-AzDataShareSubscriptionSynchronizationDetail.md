---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222619"
---
# <span data-ttu-id="9ee1b-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9ee1b-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="9ee1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ee1b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee1b-103">Pobiera informacje o synchonizationie subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="9ee1b-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="9ee1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ee1b-104">SYNTAX</span></span>

### <span data-ttu-id="9ee1b-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ee1b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ee1b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ee1b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee1b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ee1b-107">DESCRIPTION</span></span>
<span data-ttu-id="9ee1b-108">Polecenie cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** zawiera szczegółowe informacje o synchronizacji zainicjowanej dla subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="9ee1b-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="9ee1b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ee1b-109">EXAMPLES</span></span>

### <span data-ttu-id="9ee1b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ee1b-110">Example 1</span></span>
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

<span data-ttu-id="9ee1b-111">To polecenie zawiera informacje na temat synchronizacji zainicjowanej dla subskrypcji udziału AdsShareSubscription w obszarze WikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="9ee1b-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="9ee1b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ee1b-112">PARAMETERS</span></span>

### <span data-ttu-id="9ee1b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ee1b-113">-AccountName</span></span>
<span data-ttu-id="9ee1b-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="9ee1b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="9ee1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee1b-115">-DefaultProfile</span></span>
<span data-ttu-id="9ee1b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ee1b-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="9ee1b-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9ee1b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ee1b-119">-ResourceId</span></span>
<span data-ttu-id="9ee1b-120">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="9ee1b-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="9ee1b-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9ee1b-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="9ee1b-122">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="9ee1b-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9ee1b-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="9ee1b-123">-SynchronizationId</span></span>
<span data-ttu-id="9ee1b-124">Identyfikator synchronizacji synchronizacji subskrypcji udziału</span><span class="sxs-lookup"><span data-stu-id="9ee1b-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="9ee1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee1b-125">CommonParameters</span></span>
<span data-ttu-id="9ee1b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee1b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ee1b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee1b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ee1b-128">INPUTS</span></span>

### <span data-ttu-id="9ee1b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9ee1b-129">System.String</span></span>

## <span data-ttu-id="9ee1b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ee1b-130">OUTPUTS</span></span>

### <span data-ttu-id="9ee1b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9ee1b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="9ee1b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ee1b-132">NOTES</span></span>

## <span data-ttu-id="9ee1b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ee1b-133">RELATED LINKS</span></span>
