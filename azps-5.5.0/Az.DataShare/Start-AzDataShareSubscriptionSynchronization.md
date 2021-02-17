---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186090"
---
# <span data-ttu-id="eefe4-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="eefe4-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="eefe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefe4-102">SYNOPSIS</span></span>
<span data-ttu-id="eefe4-103">Inicjuje synchronizację dla subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="eefe4-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="eefe4-104">Subskrypcję udostępniania można określić za pomocą identyfikatora zasobu lub jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="eefe4-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="eefe4-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eefe4-105">SYNTAX</span></span>

### <span data-ttu-id="eefe4-106">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="eefe4-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefe4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eefe4-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefe4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eefe4-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefe4-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="eefe4-109">DESCRIPTION</span></span>
<span data-ttu-id="eefe4-110">Polecenie **cmdlet Start-AzDataShareSubscriptionSynchronization** inicjuje synchronizację dla subskrypcji udostępniania</span><span class="sxs-lookup"><span data-stu-id="eefe4-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="eefe4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eefe4-111">EXAMPLES</span></span>

### <span data-ttu-id="eefe4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eefe4-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="eefe4-113">To polecenia inicjują synchronizację subskrypcji współużytkowania o nazwie AdsShareSubscription na stronie WikiAds konta.</span><span class="sxs-lookup"><span data-stu-id="eefe4-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="eefe4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefe4-114">PARAMETERS</span></span>

### <span data-ttu-id="eefe4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eefe4-115">-AccountName</span></span>
<span data-ttu-id="eefe4-116">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eefe4-116">Azure data share account name</span></span>

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

### <span data-ttu-id="eefe4-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="eefe4-117">-AsJob</span></span>
<span data-ttu-id="eefe4-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="eefe4-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="eefe4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefe4-119">-DefaultProfile</span></span>
<span data-ttu-id="eefe4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eefe4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eefe4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eefe4-121">-InputObject</span></span>
<span data-ttu-id="eefe4-122">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eefe4-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="eefe4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefe4-123">-ResourceGroupName</span></span>
<span data-ttu-id="eefe4-124">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="eefe4-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eefe4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eefe4-125">-ResourceId</span></span>
<span data-ttu-id="eefe4-126">Identyfikator zasobu subskrypcji usługi Azure Share</span><span class="sxs-lookup"><span data-stu-id="eefe4-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="eefe4-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="eefe4-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="eefe4-128">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eefe4-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="eefe4-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="eefe4-129">-SynchronizationMode</span></span>
<span data-ttu-id="eefe4-130">Tryb synchronizacji (FullSync lub przyrostowy)</span><span class="sxs-lookup"><span data-stu-id="eefe4-130">Synchronization mode (FullSync or Incremental)</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefe4-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eefe4-131">-Confirm</span></span>
<span data-ttu-id="eefe4-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eefe4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eefe4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefe4-133">-WhatIf</span></span>
<span data-ttu-id="eefe4-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefe4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefe4-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eefe4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eefe4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefe4-136">CommonParameters</span></span>
<span data-ttu-id="eefe4-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefe4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefe4-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eefe4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefe4-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eefe4-139">INPUTS</span></span>

### <span data-ttu-id="eefe4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="eefe4-140">System.String</span></span>

### <span data-ttu-id="eefe4-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="eefe4-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="eefe4-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eefe4-142">OUTPUTS</span></span>

### <span data-ttu-id="eefe4-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="eefe4-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="eefe4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eefe4-144">NOTES</span></span>

## <span data-ttu-id="eefe4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eefe4-145">RELATED LINKS</span></span>
