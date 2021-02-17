---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198795"
---
# <span data-ttu-id="b30e0-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b30e0-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="b30e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b30e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b30e0-103">Pobiera informacje o mapowaniach zestawów danych w ramach subskrypcji udostępniania</span><span class="sxs-lookup"><span data-stu-id="b30e0-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="b30e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b30e0-104">SYNTAX</span></span>

### <span data-ttu-id="b30e0-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b30e0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b30e0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b30e0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b30e0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b30e0-107">DESCRIPTION</span></span>
<span data-ttu-id="b30e0-108">Polecenie **cmdlet Get-AzDataShareDataSetMapping** pobiera informacje o mapowaniu określonego zestawu danych, jeśli zostanie określona nazwa.</span><span class="sxs-lookup"><span data-stu-id="b30e0-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="b30e0-109">W przeciwnym razie otrzymuje informacje o wszystkich mapowaniach zestawów danych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="b30e0-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="b30e0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b30e0-110">EXAMPLES</span></span>

### <span data-ttu-id="b30e0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b30e0-111">Example 1</span></span>
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

 <span data-ttu-id="b30e0-112">To polecenie wyświetla informacje o wszystkich mapowaniach zestawów danych w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="b30e0-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="b30e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b30e0-113">PARAMETERS</span></span>

### <span data-ttu-id="b30e0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b30e0-114">-AccountName</span></span>
<span data-ttu-id="b30e0-115">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b30e0-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="b30e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30e0-116">-DefaultProfile</span></span>
<span data-ttu-id="b30e0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b30e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30e0-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b30e0-118">-Name</span></span>
<span data-ttu-id="b30e0-119">Nazwa mapowania zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b30e0-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="b30e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="b30e0-121">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="b30e0-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="b30e0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b30e0-122">-ResourceId</span></span>
<span data-ttu-id="b30e0-123">Identyfikator zasobu mapowania zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b30e0-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="b30e0-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b30e0-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="b30e0-125">Nazwa subskrypcji udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b30e0-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="b30e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30e0-126">CommonParameters</span></span>
<span data-ttu-id="b30e0-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30e0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b30e0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30e0-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b30e0-129">INPUTS</span></span>

### <span data-ttu-id="b30e0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b30e0-130">System.String</span></span>

## <span data-ttu-id="b30e0-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b30e0-131">OUTPUTS</span></span>

### <span data-ttu-id="b30e0-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b30e0-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="b30e0-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b30e0-133">NOTES</span></span>

## <span data-ttu-id="b30e0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b30e0-134">RELATED LINKS</span></span>
