---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966529"
---
# <span data-ttu-id="bdc57-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="bdc57-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="bdc57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc57-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc57-103">usuwa wyzwalacz</span><span class="sxs-lookup"><span data-stu-id="bdc57-103">removes a trigger</span></span>

## <span data-ttu-id="bdc57-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdc57-104">SYNTAX</span></span>

### <span data-ttu-id="bdc57-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bdc57-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdc57-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdc57-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc57-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdc57-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc57-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdc57-108">DESCRIPTION</span></span>
<span data-ttu-id="bdc57-109">Polecenie **cmdlet Remove-AzDataShareTrigger** usuwa wyzwalacz udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="bdc57-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="bdc57-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdc57-110">EXAMPLES</span></span>

### <span data-ttu-id="bdc57-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdc57-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bdc57-112">Te polecenia usuwają wyzwalacz o nazwie AdsTrigger z subskrypcji subskrypcji AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="bdc57-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="bdc57-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdc57-113">PARAMETERS</span></span>

### <span data-ttu-id="bdc57-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bdc57-114">-AccountName</span></span>
<span data-ttu-id="bdc57-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc57-115">Azure data share account name</span></span>

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

### <span data-ttu-id="bdc57-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bdc57-116">-AsJob</span></span>
<span data-ttu-id="bdc57-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="bdc57-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="bdc57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc57-118">-DefaultProfile</span></span>
<span data-ttu-id="bdc57-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc57-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdc57-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdc57-120">-InputObject</span></span>
<span data-ttu-id="bdc57-121">Obiekt wyzwalacza udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc57-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc57-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bdc57-122">-Name</span></span>
<span data-ttu-id="bdc57-123">Nazwa wyzwalacza udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc57-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="bdc57-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdc57-124">-PassThru</span></span>
<span data-ttu-id="bdc57-125">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="bdc57-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="bdc57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc57-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdc57-127">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc57-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bdc57-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdc57-128">-ResourceId</span></span>
<span data-ttu-id="bdc57-129">Identyfikator zasobu wyzwalacza udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc57-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="bdc57-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bdc57-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="bdc57-131">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc57-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="bdc57-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdc57-132">-Confirm</span></span>
<span data-ttu-id="bdc57-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdc57-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc57-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc57-134">-WhatIf</span></span>
<span data-ttu-id="bdc57-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc57-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc57-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bdc57-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc57-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc57-137">CommonParameters</span></span>
<span data-ttu-id="bdc57-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc57-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc57-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdc57-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc57-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc57-140">INPUTS</span></span>

### <span data-ttu-id="bdc57-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc57-141">System.String</span></span>

### <span data-ttu-id="bdc57-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="bdc57-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="bdc57-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc57-143">OUTPUTS</span></span>

### <span data-ttu-id="bdc57-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdc57-144">System.Boolean</span></span>

## <span data-ttu-id="bdc57-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdc57-145">NOTES</span></span>

## <span data-ttu-id="bdc57-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdc57-146">RELATED LINKS</span></span>
