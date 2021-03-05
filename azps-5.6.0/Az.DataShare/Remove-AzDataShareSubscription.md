---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 4cb023fecb020e37535f47823df6f02ee9f5050e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007962"
---
# <span data-ttu-id="83893-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="83893-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="83893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83893-102">SYNOPSIS</span></span>
<span data-ttu-id="83893-103">usuwa subskrypcję udostępniania</span><span class="sxs-lookup"><span data-stu-id="83893-103">removes a share subscription</span></span>

## <span data-ttu-id="83893-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83893-104">SYNTAX</span></span>

### <span data-ttu-id="83893-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="83893-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83893-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83893-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83893-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83893-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83893-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="83893-108">DESCRIPTION</span></span>
<span data-ttu-id="83893-109">Polecenie **cmdlet Remove-AzDataShareSubscription** usuwa subskrypcję udostępniania</span><span class="sxs-lookup"><span data-stu-id="83893-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="83893-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83893-110">EXAMPLES</span></span>

### <span data-ttu-id="83893-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83893-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="83893-112">Te polecenia usuwają indeks współużytkowania o nazwie AdsShareSubscription z kont WikiAds.</span><span class="sxs-lookup"><span data-stu-id="83893-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="83893-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83893-113">PARAMETERS</span></span>

### <span data-ttu-id="83893-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="83893-114">-AccountName</span></span>
<span data-ttu-id="83893-115">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83893-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="83893-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="83893-116">-AsJob</span></span>
<span data-ttu-id="83893-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="83893-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="83893-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83893-118">-DefaultProfile</span></span>
<span data-ttu-id="83893-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83893-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83893-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83893-120">-InputObject</span></span>
<span data-ttu-id="83893-121">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="83893-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83893-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="83893-122">-Name</span></span>
<span data-ttu-id="83893-123">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="83893-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="83893-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83893-124">-PassThru</span></span>
<span data-ttu-id="83893-125">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="83893-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="83893-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83893-126">-ResourceGroupName</span></span>
<span data-ttu-id="83893-127">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="83893-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="83893-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83893-128">-ResourceId</span></span>
<span data-ttu-id="83893-129">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="83893-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="83893-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83893-130">-Confirm</span></span>
<span data-ttu-id="83893-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="83893-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83893-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83893-132">-WhatIf</span></span>
<span data-ttu-id="83893-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83893-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83893-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="83893-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83893-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83893-135">CommonParameters</span></span>
<span data-ttu-id="83893-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83893-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83893-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83893-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83893-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83893-138">INPUTS</span></span>

### <span data-ttu-id="83893-139">System.String</span><span class="sxs-lookup"><span data-stu-id="83893-139">System.String</span></span>

### <span data-ttu-id="83893-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="83893-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="83893-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83893-141">OUTPUTS</span></span>

### <span data-ttu-id="83893-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83893-142">System.Boolean</span></span>

## <span data-ttu-id="83893-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83893-143">NOTES</span></span>

## <span data-ttu-id="83893-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83893-144">RELATED LINKS</span></span>
