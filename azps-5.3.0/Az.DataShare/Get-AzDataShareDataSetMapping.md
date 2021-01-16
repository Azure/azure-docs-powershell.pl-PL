---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377489"
---
# <span data-ttu-id="dfe9a-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="dfe9a-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="dfe9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfe9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe9a-103">Pobiera informacje o mapowaniach zestawów danych w subskrypcji udostępniania</span><span class="sxs-lookup"><span data-stu-id="dfe9a-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="dfe9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfe9a-104">SYNTAX</span></span>

### <span data-ttu-id="dfe9a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dfe9a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfe9a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe9a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfe9a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dfe9a-107">DESCRIPTION</span></span>
<span data-ttu-id="dfe9a-108">Polecenie cmdlet **Get-AzDataShareDataSetMapping** pobiera informacje na temat konkretnego mapowania zestawu danych, jeśli nazwa jest określona.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="dfe9a-109">W przeciwnym razie pobiera informacje o wszystkich mapowaniach zestawów danych w subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="dfe9a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfe9a-110">EXAMPLES</span></span>

### <span data-ttu-id="dfe9a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dfe9a-111">Example 1</span></span>
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

 <span data-ttu-id="dfe9a-112">To polecenie wyświetla informacje o wszystkich mapowaniach zestawów danych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="dfe9a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfe9a-113">PARAMETERS</span></span>

### <span data-ttu-id="dfe9a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dfe9a-114">-AccountName</span></span>
<span data-ttu-id="dfe9a-115">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="dfe9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe9a-116">-DefaultProfile</span></span>
<span data-ttu-id="dfe9a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfe9a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfe9a-118">-Name</span></span>
<span data-ttu-id="dfe9a-119">Nazwa mapowania zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="dfe9a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe9a-120">-ResourceGroupName</span></span>
<span data-ttu-id="dfe9a-121">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="dfe9a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe9a-122">-ResourceId</span></span>
<span data-ttu-id="dfe9a-123">Identyfikator zasobu mapowania zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="dfe9a-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="dfe9a-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="dfe9a-125">Nazwa subskrypcji udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="dfe9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe9a-126">CommonParameters</span></span>
<span data-ttu-id="dfe9a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe9a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfe9a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe9a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfe9a-129">INPUTS</span></span>

### <span data-ttu-id="dfe9a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe9a-130">System.String</span></span>

## <span data-ttu-id="dfe9a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfe9a-131">OUTPUTS</span></span>

### <span data-ttu-id="dfe9a-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="dfe9a-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="dfe9a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfe9a-133">NOTES</span></span>

## <span data-ttu-id="dfe9a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfe9a-134">RELATED LINKS</span></span>
