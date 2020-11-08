---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222607"
---
# <span data-ttu-id="91a33-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="91a33-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="91a33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91a33-102">SYNOPSIS</span></span>
<span data-ttu-id="91a33-103">Zatrzymuje trwającą synchronizację subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="91a33-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="91a33-104">Abonament udostępniania można określić za pomocą identyfikatora zasobu lub jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="91a33-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="91a33-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91a33-105">SYNTAX</span></span>

### <span data-ttu-id="91a33-106">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="91a33-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91a33-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a33-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91a33-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a33-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91a33-109">Opis</span><span class="sxs-lookup"><span data-stu-id="91a33-109">DESCRIPTION</span></span>
<span data-ttu-id="91a33-110">Polecenie cmdlet **stop-AzDataShareSubscriptionSynchronization** zatrzymuje ciągłą synchronizację subskrypcji udziału</span><span class="sxs-lookup"><span data-stu-id="91a33-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="91a33-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91a33-111">EXAMPLES</span></span>

### <span data-ttu-id="91a33-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91a33-112">Example 1</span></span>
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

<span data-ttu-id="91a33-113">Zatrzymuje trwającą synchronizację oznaczoną identyfikatorem-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="91a33-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="91a33-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91a33-114">PARAMETERS</span></span>

### <span data-ttu-id="91a33-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91a33-115">-AccountName</span></span>
<span data-ttu-id="91a33-116">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="91a33-116">Azure data share account name</span></span>

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

### <span data-ttu-id="91a33-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91a33-117">-AsJob</span></span>
<span data-ttu-id="91a33-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="91a33-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="91a33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a33-119">-DefaultProfile</span></span>
<span data-ttu-id="91a33-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91a33-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91a33-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91a33-121">-InputObject</span></span>
<span data-ttu-id="91a33-122">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="91a33-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="91a33-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a33-123">-ResourceGroupName</span></span>
<span data-ttu-id="91a33-124">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="91a33-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="91a33-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91a33-125">-ResourceId</span></span>
<span data-ttu-id="91a33-126">Identyfikator zasobu subskrypcji udziału w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="91a33-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="91a33-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="91a33-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="91a33-128">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="91a33-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="91a33-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="91a33-129">-SynchronizationId</span></span>
<span data-ttu-id="91a33-130">Identyfikator synchronizacji, który musi zostać zatrzymany</span><span class="sxs-lookup"><span data-stu-id="91a33-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="91a33-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91a33-131">-Confirm</span></span>
<span data-ttu-id="91a33-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91a33-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91a33-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a33-133">-WhatIf</span></span>
<span data-ttu-id="91a33-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91a33-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91a33-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91a33-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91a33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a33-136">CommonParameters</span></span>
<span data-ttu-id="91a33-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a33-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91a33-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a33-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91a33-139">INPUTS</span></span>

### <span data-ttu-id="91a33-140">System. String</span><span class="sxs-lookup"><span data-stu-id="91a33-140">System.String</span></span>

### <span data-ttu-id="91a33-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="91a33-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="91a33-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91a33-142">OUTPUTS</span></span>

### <span data-ttu-id="91a33-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="91a33-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="91a33-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91a33-144">NOTES</span></span>

## <span data-ttu-id="91a33-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91a33-145">RELATED LINKS</span></span>
