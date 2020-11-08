---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 73272c2afd0b3d8ef62a522f2e67f04854c2232e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049931"
---
# <span data-ttu-id="a9399-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a9399-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="a9399-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9399-102">SYNOPSIS</span></span>
<span data-ttu-id="a9399-103">Pobiera informacje o zestawach danych w usłudze Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="a9399-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="a9399-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9399-104">SYNTAX</span></span>

### <span data-ttu-id="a9399-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9399-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9399-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9399-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9399-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a9399-107">DESCRIPTION</span></span>
<span data-ttu-id="a9399-108">Polecenie cmdlet **Get-AzDataShareDataSet** pobiera informacje o zestawach danych dodanych w udziale na koncie usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="a9399-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="a9399-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="a9399-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="a9399-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w udziale. Prób</span><span class="sxs-lookup"><span data-stu-id="a9399-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="a9399-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9399-111">EXAMPLES</span></span>

### <span data-ttu-id="a9399-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9399-112">Example 1</span></span>
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

<span data-ttu-id="a9399-113">To polecenie wyświetla informacje na temat zestawu danych AdsDataSet w AdsShare udostępniania danych konta usługi Azure Data Share WikiAdsAccount i reklamy grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9399-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="a9399-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9399-114">PARAMETERS</span></span>

### <span data-ttu-id="a9399-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9399-115">-AccountName</span></span>
<span data-ttu-id="a9399-116">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="a9399-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="a9399-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9399-117">-DefaultProfile</span></span>
<span data-ttu-id="a9399-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9399-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9399-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9399-119">-Name</span></span>
<span data-ttu-id="a9399-120">Nazwa zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9399-120">Azure data set name.</span></span>

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

### <span data-ttu-id="a9399-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9399-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9399-122">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="a9399-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="a9399-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9399-123">-ResourceId</span></span>
<span data-ttu-id="a9399-124">Identyfikator zasobu zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9399-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="a9399-125">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="a9399-125">-ShareName</span></span>
<span data-ttu-id="a9399-126">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9399-126">Azure data share name.</span></span>

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

### <span data-ttu-id="a9399-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9399-127">CommonParameters</span></span>
<span data-ttu-id="a9399-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9399-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9399-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9399-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9399-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9399-130">INPUTS</span></span>

### <span data-ttu-id="a9399-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a9399-131">System.String</span></span>

## <span data-ttu-id="a9399-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9399-132">OUTPUTS</span></span>

### <span data-ttu-id="a9399-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a9399-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="a9399-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9399-134">NOTES</span></span>

## <span data-ttu-id="a9399-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9399-135">RELATED LINKS</span></span>
