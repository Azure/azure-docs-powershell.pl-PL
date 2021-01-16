---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377503"
---
# <span data-ttu-id="73748-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="73748-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="73748-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73748-102">SYNOPSIS</span></span>
<span data-ttu-id="73748-103">Pobiera informacje o zestawach danych w usłudze Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="73748-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="73748-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73748-104">SYNTAX</span></span>

### <span data-ttu-id="73748-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73748-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73748-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73748-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73748-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73748-107">DESCRIPTION</span></span>
<span data-ttu-id="73748-108">Polecenie cmdlet **Get-AzDataShareDataSet** pobiera informacje o zestawach danych dodanych w udziale na koncie usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="73748-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="73748-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="73748-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="73748-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w udziale. Prób</span><span class="sxs-lookup"><span data-stu-id="73748-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="73748-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73748-111">EXAMPLES</span></span>

### <span data-ttu-id="73748-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73748-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="73748-113">To polecenie wyświetla informacje na temat zestawu danych AdsDataSet w AdsShare udostępniania danych konta usługi Azure Data Share WikiAdsAccount i reklamy grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="73748-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="73748-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73748-114">PARAMETERS</span></span>

### <span data-ttu-id="73748-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73748-115">-AccountName</span></span>
<span data-ttu-id="73748-116">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="73748-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="73748-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73748-117">-DefaultProfile</span></span>
<span data-ttu-id="73748-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73748-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73748-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73748-119">-Name</span></span>
<span data-ttu-id="73748-120">Nazwa zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="73748-120">Azure data set name.</span></span>

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

### <span data-ttu-id="73748-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73748-121">-ResourceGroupName</span></span>
<span data-ttu-id="73748-122">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="73748-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="73748-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73748-123">-ResourceId</span></span>
<span data-ttu-id="73748-124">Identyfikator zasobu zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="73748-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="73748-125">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="73748-125">-ShareName</span></span>
<span data-ttu-id="73748-126">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="73748-126">Azure data share name.</span></span>

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

### <span data-ttu-id="73748-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73748-127">CommonParameters</span></span>
<span data-ttu-id="73748-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73748-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73748-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73748-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73748-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73748-130">INPUTS</span></span>

### <span data-ttu-id="73748-131">System. String</span><span class="sxs-lookup"><span data-stu-id="73748-131">System.String</span></span>

## <span data-ttu-id="73748-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73748-132">OUTPUTS</span></span>

### <span data-ttu-id="73748-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="73748-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="73748-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73748-134">NOTES</span></span>

## <span data-ttu-id="73748-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73748-135">RELATED LINKS</span></span>
