---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 8e3513621b94a7fc98a00b7eb443bef18d2a8141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988233"
---
# <span data-ttu-id="1b439-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="1b439-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="1b439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b439-102">SYNOPSIS</span></span>
<span data-ttu-id="1b439-103">Usuwa mapowanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="1b439-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="1b439-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b439-104">SYNTAX</span></span>

### <span data-ttu-id="1b439-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1b439-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b439-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b439-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b439-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b439-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b439-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b439-108">DESCRIPTION</span></span>
<span data-ttu-id="1b439-109">Polecenie **cmdlet Remove-AzDataShareDataSetMapping** usuwa mapowania zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="1b439-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="1b439-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b439-110">EXAMPLES</span></span>

### <span data-ttu-id="1b439-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b439-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="1b439-112">Te polecenia usuwają zestaw danych o nazwie DSM z witryny WikiAds subskrypcji udziałów.</span><span class="sxs-lookup"><span data-stu-id="1b439-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="1b439-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b439-113">PARAMETERS</span></span>

### <span data-ttu-id="1b439-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b439-114">-AccountName</span></span>
<span data-ttu-id="1b439-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1b439-115">Azure data share account name</span></span>

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

### <span data-ttu-id="1b439-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b439-116">-DefaultProfile</span></span>
<span data-ttu-id="1b439-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b439-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b439-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b439-118">-InputObject</span></span>
<span data-ttu-id="1b439-119">Obiekt mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1b439-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="1b439-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1b439-120">-Name</span></span>
<span data-ttu-id="1b439-121">Nazwa mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1b439-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="1b439-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b439-122">-PassThru</span></span>
<span data-ttu-id="1b439-123">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="1b439-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="1b439-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b439-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b439-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="1b439-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1b439-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b439-126">-ResourceId</span></span>
<span data-ttu-id="1b439-127">Identyfikator zasobu mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1b439-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="1b439-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1b439-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="1b439-129">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1b439-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1b439-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b439-130">-Confirm</span></span>
<span data-ttu-id="1b439-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b439-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b439-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b439-132">-WhatIf</span></span>
<span data-ttu-id="1b439-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b439-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b439-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1b439-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b439-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b439-135">CommonParameters</span></span>
<span data-ttu-id="1b439-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b439-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b439-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b439-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b439-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b439-138">INPUTS</span></span>

### <span data-ttu-id="1b439-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1b439-139">System.String</span></span>

### <span data-ttu-id="1b439-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="1b439-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="1b439-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b439-141">OUTPUTS</span></span>

### <span data-ttu-id="1b439-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1b439-142">System.Boolean</span></span>

## <span data-ttu-id="1b439-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b439-143">NOTES</span></span>

## <span data-ttu-id="1b439-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b439-144">RELATED LINKS</span></span>
