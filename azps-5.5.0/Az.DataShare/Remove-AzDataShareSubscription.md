---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200538"
---
# <span data-ttu-id="3b898-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3b898-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="3b898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b898-102">SYNOPSIS</span></span>
<span data-ttu-id="3b898-103">usuwa subskrypcję udostępniania</span><span class="sxs-lookup"><span data-stu-id="3b898-103">removes a share subscription</span></span>

## <span data-ttu-id="3b898-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b898-104">SYNTAX</span></span>

### <span data-ttu-id="3b898-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3b898-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b898-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b898-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b898-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b898-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b898-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b898-108">DESCRIPTION</span></span>
<span data-ttu-id="3b898-109">Polecenie **cmdlet Remove-AzDataShareSubscription** usuwa subskrypcję udostępniania</span><span class="sxs-lookup"><span data-stu-id="3b898-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="3b898-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b898-110">EXAMPLES</span></span>

### <span data-ttu-id="3b898-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b898-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3b898-112">Te polecenia usuwają indeks współużytkowania o nazwie AdsShareSubscription z kont WikiAds.</span><span class="sxs-lookup"><span data-stu-id="3b898-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="3b898-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b898-113">PARAMETERS</span></span>

### <span data-ttu-id="3b898-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b898-114">-AccountName</span></span>
<span data-ttu-id="3b898-115">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b898-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="3b898-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3b898-116">-AsJob</span></span>
<span data-ttu-id="3b898-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3b898-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3b898-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b898-118">-DefaultProfile</span></span>
<span data-ttu-id="3b898-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b898-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b898-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b898-120">-InputObject</span></span>
<span data-ttu-id="3b898-121">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3b898-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="3b898-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3b898-122">-Name</span></span>
<span data-ttu-id="3b898-123">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3b898-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3b898-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b898-124">-PassThru</span></span>
<span data-ttu-id="3b898-125">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="3b898-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="3b898-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b898-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b898-127">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3b898-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3b898-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b898-128">-ResourceId</span></span>
<span data-ttu-id="3b898-129">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="3b898-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="3b898-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b898-130">-Confirm</span></span>
<span data-ttu-id="3b898-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b898-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b898-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b898-132">-WhatIf</span></span>
<span data-ttu-id="3b898-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b898-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b898-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b898-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b898-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b898-135">CommonParameters</span></span>
<span data-ttu-id="3b898-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b898-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b898-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b898-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b898-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b898-138">INPUTS</span></span>

### <span data-ttu-id="3b898-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3b898-139">System.String</span></span>

### <span data-ttu-id="3b898-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3b898-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="3b898-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b898-141">OUTPUTS</span></span>

### <span data-ttu-id="3b898-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b898-142">System.Boolean</span></span>

## <span data-ttu-id="3b898-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b898-143">NOTES</span></span>

## <span data-ttu-id="3b898-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b898-144">RELATED LINKS</span></span>
