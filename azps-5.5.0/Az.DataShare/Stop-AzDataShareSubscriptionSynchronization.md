---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238139"
---
# <span data-ttu-id="57cc1-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="57cc1-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="57cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="57cc1-103">Zatrzymuje bieżącą synchronizację dla subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="57cc1-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="57cc1-104">Subskrypcję udostępniania można określić za pomocą identyfikatora zasobu lub jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="57cc1-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="57cc1-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57cc1-105">SYNTAX</span></span>

### <span data-ttu-id="57cc1-106">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="57cc1-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57cc1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57cc1-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57cc1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57cc1-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57cc1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="57cc1-109">DESCRIPTION</span></span>
<span data-ttu-id="57cc1-110">Polecenie **cmdlet Stop-AzDataShareSubscriptionSynchronization** zatrzymuje bieżącą synchronizację dla subskrypcji udostępniania</span><span class="sxs-lookup"><span data-stu-id="57cc1-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="57cc1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57cc1-111">EXAMPLES</span></span>

### <span data-ttu-id="57cc1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57cc1-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="57cc1-113">Zatrzymuje bieżącą synchronizację identyfikowaną za pomocą identyfikatora — 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="57cc1-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="57cc1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57cc1-114">PARAMETERS</span></span>

### <span data-ttu-id="57cc1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57cc1-115">-AccountName</span></span>
<span data-ttu-id="57cc1-116">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57cc1-116">Azure data share account name</span></span>

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

### <span data-ttu-id="57cc1-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="57cc1-117">-AsJob</span></span>
<span data-ttu-id="57cc1-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="57cc1-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="57cc1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cc1-119">-DefaultProfile</span></span>
<span data-ttu-id="57cc1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57cc1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57cc1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57cc1-121">-InputObject</span></span>
<span data-ttu-id="57cc1-122">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57cc1-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="57cc1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57cc1-123">-ResourceGroupName</span></span>
<span data-ttu-id="57cc1-124">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57cc1-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="57cc1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57cc1-125">-ResourceId</span></span>
<span data-ttu-id="57cc1-126">Identyfikator zasobu subskrypcji usługi Azure Share</span><span class="sxs-lookup"><span data-stu-id="57cc1-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="57cc1-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="57cc1-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="57cc1-128">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57cc1-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="57cc1-129">- SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="57cc1-129">-SynchronizationId</span></span>
<span data-ttu-id="57cc1-130">Identyfikator synchronizacji, który należy zatrzymać</span><span class="sxs-lookup"><span data-stu-id="57cc1-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="57cc1-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57cc1-131">-Confirm</span></span>
<span data-ttu-id="57cc1-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="57cc1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57cc1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57cc1-133">-WhatIf</span></span>
<span data-ttu-id="57cc1-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57cc1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57cc1-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="57cc1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57cc1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cc1-136">CommonParameters</span></span>
<span data-ttu-id="57cc1-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57cc1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cc1-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57cc1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cc1-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57cc1-139">INPUTS</span></span>

### <span data-ttu-id="57cc1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="57cc1-140">System.String</span></span>

### <span data-ttu-id="57cc1-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="57cc1-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="57cc1-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57cc1-142">OUTPUTS</span></span>

### <span data-ttu-id="57cc1-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="57cc1-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="57cc1-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57cc1-144">NOTES</span></span>

## <span data-ttu-id="57cc1-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57cc1-145">RELATED LINKS</span></span>
