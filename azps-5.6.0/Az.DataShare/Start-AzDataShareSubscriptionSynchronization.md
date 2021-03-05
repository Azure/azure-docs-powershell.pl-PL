---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: b2fe61d4493fea64f4ee7b07bdd14905fb7661db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966513"
---
# <span data-ttu-id="09a4b-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="09a4b-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="09a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="09a4b-103">Inicjuje synchronizację dla subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="09a4b-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="09a4b-104">Subskrypcję udostępniania można określić za pomocą identyfikatora zasobu lub jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="09a4b-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="09a4b-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09a4b-105">SYNTAX</span></span>

### <span data-ttu-id="09a4b-106">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="09a4b-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a4b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09a4b-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a4b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09a4b-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a4b-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="09a4b-109">DESCRIPTION</span></span>
<span data-ttu-id="09a4b-110">Polecenie **cmdlet Start-AzDataShareSubscriptionSynchronization** inicjuje synchronizację dla subskrypcji udostępniania</span><span class="sxs-lookup"><span data-stu-id="09a4b-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="09a4b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09a4b-111">EXAMPLES</span></span>

### <span data-ttu-id="09a4b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09a4b-112">Example 1</span></span>
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

<span data-ttu-id="09a4b-113">To polecenia inicjują synchronizację subskrypcji shareubskrypcji o nazwie AdsShareSubscription na stronie wikiAds konta.</span><span class="sxs-lookup"><span data-stu-id="09a4b-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="09a4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="09a4b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09a4b-115">-AccountName</span></span>
<span data-ttu-id="09a4b-116">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="09a4b-116">Azure data share account name</span></span>

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

### <span data-ttu-id="09a4b-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="09a4b-117">-AsJob</span></span>
<span data-ttu-id="09a4b-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="09a4b-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="09a4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a4b-119">-DefaultProfile</span></span>
<span data-ttu-id="09a4b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09a4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a4b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a4b-121">-InputObject</span></span>
<span data-ttu-id="09a4b-122">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="09a4b-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="09a4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="09a4b-124">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="09a4b-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="09a4b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09a4b-125">-ResourceId</span></span>
<span data-ttu-id="09a4b-126">Identyfikator zasobu subskrypcji usługi Azure Share</span><span class="sxs-lookup"><span data-stu-id="09a4b-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="09a4b-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="09a4b-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="09a4b-128">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="09a4b-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="09a4b-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="09a4b-129">-SynchronizationMode</span></span>
<span data-ttu-id="09a4b-130">Tryb synchronizacji (FullSync lub przyrostowy)</span><span class="sxs-lookup"><span data-stu-id="09a4b-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="09a4b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09a4b-131">-Confirm</span></span>
<span data-ttu-id="09a4b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09a4b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a4b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a4b-133">-WhatIf</span></span>
<span data-ttu-id="09a4b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09a4b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09a4b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09a4b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a4b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a4b-136">CommonParameters</span></span>
<span data-ttu-id="09a4b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a4b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a4b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09a4b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a4b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09a4b-139">INPUTS</span></span>

### <span data-ttu-id="09a4b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="09a4b-140">System.String</span></span>

### <span data-ttu-id="09a4b-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="09a4b-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="09a4b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09a4b-142">OUTPUTS</span></span>

### <span data-ttu-id="09a4b-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="09a4b-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="09a4b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09a4b-144">NOTES</span></span>

## <span data-ttu-id="09a4b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09a4b-145">RELATED LINKS</span></span>
