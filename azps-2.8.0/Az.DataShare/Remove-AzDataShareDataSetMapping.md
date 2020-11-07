---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 249f166bcf4dd61d9b8da7cf4d67a2ac20f705ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705658"
---
# <span data-ttu-id="4c903-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="4c903-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="4c903-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c903-102">SYNOPSIS</span></span>
<span data-ttu-id="4c903-103">Usuwa mapowanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="4c903-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="4c903-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c903-104">SYNTAX</span></span>

### <span data-ttu-id="4c903-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4c903-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c903-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c903-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c903-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c903-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c903-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4c903-108">DESCRIPTION</span></span>
<span data-ttu-id="4c903-109">Polecenie cmdlet **Remove-AzDataShareDataSetMapping** usuwa mapowania zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="4c903-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="4c903-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c903-110">EXAMPLES</span></span>

### <span data-ttu-id="4c903-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c903-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4c903-112">To polecenie usuwa zestaw danych o nazwie DSM z sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="4c903-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="4c903-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c903-113">PARAMETERS</span></span>

### <span data-ttu-id="4c903-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4c903-114">-AccountName</span></span>
<span data-ttu-id="4c903-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="4c903-115">Azure data share account name</span></span>

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

### <span data-ttu-id="4c903-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c903-116">-DefaultProfile</span></span>
<span data-ttu-id="4c903-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c903-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c903-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4c903-118">-InputObject</span></span>
<span data-ttu-id="4c903-119">Obiekt mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4c903-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="4c903-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c903-120">-Name</span></span>
<span data-ttu-id="4c903-121">Nazwa mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4c903-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="4c903-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c903-122">-PassThru</span></span>
<span data-ttu-id="4c903-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="4c903-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="4c903-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c903-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c903-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="4c903-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4c903-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c903-126">-ResourceId</span></span>
<span data-ttu-id="4c903-127">Identyfikator zasobu mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4c903-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="4c903-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4c903-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="4c903-129">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="4c903-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4c903-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c903-130">-Confirm</span></span>
<span data-ttu-id="4c903-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c903-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c903-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c903-132">-WhatIf</span></span>
<span data-ttu-id="4c903-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c903-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c903-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c903-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c903-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c903-135">CommonParameters</span></span>
<span data-ttu-id="4c903-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c903-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c903-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c903-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c903-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c903-138">INPUTS</span></span>

### <span data-ttu-id="4c903-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4c903-139">System.String</span></span>

### <span data-ttu-id="4c903-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="4c903-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="4c903-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c903-141">OUTPUTS</span></span>

### <span data-ttu-id="4c903-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c903-142">System.Boolean</span></span>

## <span data-ttu-id="4c903-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c903-143">NOTES</span></span>

## <span data-ttu-id="4c903-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c903-144">RELATED LINKS</span></span>
