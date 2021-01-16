---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377125"
---
# <span data-ttu-id="b5b77-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b5b77-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="b5b77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5b77-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b77-103">Usuwa mapowanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="b5b77-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="b5b77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5b77-104">SYNTAX</span></span>

### <span data-ttu-id="b5b77-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5b77-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b77-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b77-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b77-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b77-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b77-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b5b77-108">DESCRIPTION</span></span>
<span data-ttu-id="b5b77-109">Polecenie cmdlet **Remove-AzDataShareDataSetMapping** usuwa mapowania zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="b5b77-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="b5b77-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5b77-110">EXAMPLES</span></span>

### <span data-ttu-id="b5b77-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5b77-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b5b77-112">To polecenie usuwa zestaw danych o nazwie DSM z sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b5b77-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="b5b77-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5b77-113">PARAMETERS</span></span>

### <span data-ttu-id="b5b77-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5b77-114">-AccountName</span></span>
<span data-ttu-id="b5b77-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="b5b77-115">Azure data share account name</span></span>

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

### <span data-ttu-id="b5b77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b77-116">-DefaultProfile</span></span>
<span data-ttu-id="b5b77-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b77-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b5b77-118">-InputObject</span></span>
<span data-ttu-id="b5b77-119">Obiekt mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b5b77-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b77-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5b77-120">-Name</span></span>
<span data-ttu-id="b5b77-121">Nazwa mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b5b77-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="b5b77-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5b77-122">-PassThru</span></span>
<span data-ttu-id="b5b77-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="b5b77-123">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b77-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5b77-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="b5b77-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b5b77-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5b77-126">-ResourceId</span></span>
<span data-ttu-id="b5b77-127">Identyfikator zasobu mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b5b77-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="b5b77-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b5b77-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="b5b77-129">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="b5b77-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b5b77-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5b77-130">-Confirm</span></span>
<span data-ttu-id="b5b77-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b77-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b77-132">-WhatIf</span></span>
<span data-ttu-id="b5b77-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b77-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5b77-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b77-135">CommonParameters</span></span>
<span data-ttu-id="b5b77-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b77-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5b77-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b77-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5b77-138">INPUTS</span></span>

### <span data-ttu-id="b5b77-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b77-139">System.String</span></span>

### <span data-ttu-id="b5b77-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b5b77-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="b5b77-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5b77-141">OUTPUTS</span></span>

### <span data-ttu-id="b5b77-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5b77-142">System.Boolean</span></span>

## <span data-ttu-id="b5b77-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5b77-143">NOTES</span></span>

## <span data-ttu-id="b5b77-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5b77-144">RELATED LINKS</span></span>
