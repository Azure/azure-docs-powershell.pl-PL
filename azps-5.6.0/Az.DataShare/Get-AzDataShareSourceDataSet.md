---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 97a72b9dbeb50d1710625f7a6142151834a84d92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012209"
---
# <span data-ttu-id="da03f-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="da03f-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="da03f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da03f-102">SYNOPSIS</span></span>
<span data-ttu-id="da03f-103">Pobiera informacje o źródłowych zestawach danych w ramach subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="da03f-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="da03f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da03f-104">SYNTAX</span></span>

### <span data-ttu-id="da03f-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="da03f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da03f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da03f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da03f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="da03f-107">DESCRIPTION</span></span>
<span data-ttu-id="da03f-108">Polecenie **cmdlet Get-AzDataShareSourceDataSet** dostarcza informacji o źródłowych zestawach danych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="da03f-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="da03f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da03f-109">EXAMPLES</span></span>

### <span data-ttu-id="da03f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da03f-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="da03f-111">Pobiera zestawy danych dostępne w udziałze źródłowym</span><span class="sxs-lookup"><span data-stu-id="da03f-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="da03f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da03f-112">PARAMETERS</span></span>

### <span data-ttu-id="da03f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da03f-113">-AccountName</span></span>
<span data-ttu-id="da03f-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="da03f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="da03f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da03f-115">-DefaultProfile</span></span>
<span data-ttu-id="da03f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da03f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da03f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da03f-117">-ResourceGroupName</span></span>
<span data-ttu-id="da03f-118">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="da03f-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="da03f-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="da03f-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="da03f-120">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="da03f-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="da03f-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="da03f-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="da03f-122">Identyfikator zasobu subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="da03f-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="da03f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da03f-123">CommonParameters</span></span>
<span data-ttu-id="da03f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da03f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da03f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da03f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da03f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da03f-126">INPUTS</span></span>

### <span data-ttu-id="da03f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="da03f-127">System.String</span></span>

## <span data-ttu-id="da03f-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da03f-128">OUTPUTS</span></span>

### <span data-ttu-id="da03f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="da03f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="da03f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da03f-130">NOTES</span></span>

## <span data-ttu-id="da03f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da03f-131">RELATED LINKS</span></span>
