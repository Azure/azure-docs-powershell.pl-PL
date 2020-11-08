---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: cf8b235d0035955f809b167ba4d532cdae0538c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049679"
---
# <span data-ttu-id="3834a-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3834a-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="3834a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3834a-102">SYNOPSIS</span></span>
<span data-ttu-id="3834a-103">Pobiera informacje o mapowaniach zestawów danych w subskrypcji udostępniania</span><span class="sxs-lookup"><span data-stu-id="3834a-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="3834a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3834a-104">SYNTAX</span></span>

### <span data-ttu-id="3834a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3834a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3834a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3834a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3834a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3834a-107">DESCRIPTION</span></span>
<span data-ttu-id="3834a-108">Polecenie cmdlet **Get-AzDataShareDataSetMapping** pobiera informacje na temat konkretnego mapowania zestawu danych, jeśli nazwa jest określona.</span><span class="sxs-lookup"><span data-stu-id="3834a-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="3834a-109">W przeciwnym razie pobiera informacje o wszystkich mapowaniach zestawów danych w subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="3834a-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="3834a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3834a-110">EXAMPLES</span></span>

### <span data-ttu-id="3834a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3834a-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="3834a-112">To polecenie wyświetla informacje o wszystkich mapowaniach zestawów danych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="3834a-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="3834a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3834a-113">PARAMETERS</span></span>

### <span data-ttu-id="3834a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3834a-114">-AccountName</span></span>
<span data-ttu-id="3834a-115">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3834a-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="3834a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3834a-116">-DefaultProfile</span></span>
<span data-ttu-id="3834a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3834a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3834a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3834a-118">-Name</span></span>
<span data-ttu-id="3834a-119">Nazwa mapowania zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3834a-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="3834a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3834a-120">-ResourceGroupName</span></span>
<span data-ttu-id="3834a-121">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="3834a-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="3834a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3834a-122">-ResourceId</span></span>
<span data-ttu-id="3834a-123">Identyfikator zasobu mapowania zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3834a-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="3834a-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3834a-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="3834a-125">Nazwa subskrypcji udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3834a-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="3834a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3834a-126">CommonParameters</span></span>
<span data-ttu-id="3834a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3834a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3834a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3834a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3834a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3834a-129">INPUTS</span></span>

### <span data-ttu-id="3834a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3834a-130">System.String</span></span>

## <span data-ttu-id="3834a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3834a-131">OUTPUTS</span></span>

### <span data-ttu-id="3834a-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3834a-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="3834a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3834a-133">NOTES</span></span>

## <span data-ttu-id="3834a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3834a-134">RELATED LINKS</span></span>
