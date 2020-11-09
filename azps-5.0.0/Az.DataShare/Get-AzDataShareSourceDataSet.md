---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305280"
---
# <span data-ttu-id="2fdce-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="2fdce-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="2fdce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fdce-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdce-103">Pobiera informacje o zestawach danych źródłowych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="2fdce-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="2fdce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fdce-104">SYNTAX</span></span>

### <span data-ttu-id="2fdce-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2fdce-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fdce-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdce-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fdce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fdce-107">DESCRIPTION</span></span>
<span data-ttu-id="2fdce-108">Polecenie cmdlet **Get-AzDataShareSourceDataSet** zawiera informacje dotyczące zestawów danych źródłowych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="2fdce-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="2fdce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fdce-109">EXAMPLES</span></span>

### <span data-ttu-id="2fdce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fdce-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="2fdce-111">Pobiera zestawy danych dostępne w udziale źródłowym.</span><span class="sxs-lookup"><span data-stu-id="2fdce-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="2fdce-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fdce-112">PARAMETERS</span></span>

### <span data-ttu-id="2fdce-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2fdce-113">-AccountName</span></span>
<span data-ttu-id="2fdce-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="2fdce-114">Azure data share account name</span></span>

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

### <span data-ttu-id="2fdce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdce-115">-DefaultProfile</span></span>
<span data-ttu-id="2fdce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fdce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdce-117">-ResourceGroupName</span></span>
<span data-ttu-id="2fdce-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="2fdce-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2fdce-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2fdce-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="2fdce-120">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="2fdce-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2fdce-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="2fdce-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="2fdce-122">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="2fdce-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="2fdce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdce-123">CommonParameters</span></span>
<span data-ttu-id="2fdce-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fdce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdce-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fdce-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdce-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fdce-126">INPUTS</span></span>

### <span data-ttu-id="2fdce-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2fdce-127">System.String</span></span>

## <span data-ttu-id="2fdce-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fdce-128">OUTPUTS</span></span>

### <span data-ttu-id="2fdce-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="2fdce-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="2fdce-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fdce-130">NOTES</span></span>

## <span data-ttu-id="2fdce-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fdce-131">RELATED LINKS</span></span>
