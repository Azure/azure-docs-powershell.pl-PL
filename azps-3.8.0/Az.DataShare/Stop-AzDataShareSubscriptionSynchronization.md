---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 130fce51952078a32bceb31fe3e0770f06dcaffb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053373"
---
# <span data-ttu-id="cddec-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="cddec-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="cddec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cddec-102">SYNOPSIS</span></span>
<span data-ttu-id="cddec-103">Zatrzymuje trwającą synchronizację subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="cddec-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="cddec-104">Abonament udostępniania można określić za pomocą identyfikatora zasobu lub jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="cddec-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="cddec-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cddec-105">SYNTAX</span></span>

### <span data-ttu-id="cddec-106">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cddec-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddec-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cddec-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddec-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cddec-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cddec-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cddec-109">DESCRIPTION</span></span>
<span data-ttu-id="cddec-110">Polecenie cmdlet **stop-AzDataShareSubscriptionSynchronization** zatrzymuje ciągłą synchronizację subskrypcji udziału</span><span class="sxs-lookup"><span data-stu-id="cddec-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="cddec-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cddec-111">EXAMPLES</span></span>

### <span data-ttu-id="cddec-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cddec-112">Example 1</span></span>
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

<span data-ttu-id="cddec-113">Zatrzymuje trwającą synchronizację oznaczoną identyfikatorem-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="cddec-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="cddec-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cddec-114">PARAMETERS</span></span>

### <span data-ttu-id="cddec-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cddec-115">-AccountName</span></span>
<span data-ttu-id="cddec-116">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="cddec-116">Azure data share account name</span></span>

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

### <span data-ttu-id="cddec-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cddec-117">-AsJob</span></span>
<span data-ttu-id="cddec-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="cddec-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="cddec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddec-119">-DefaultProfile</span></span>
<span data-ttu-id="cddec-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cddec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cddec-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cddec-121">-InputObject</span></span>
<span data-ttu-id="cddec-122">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cddec-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="cddec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddec-123">-ResourceGroupName</span></span>
<span data-ttu-id="cddec-124">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="cddec-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cddec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddec-125">-ResourceId</span></span>
<span data-ttu-id="cddec-126">Identyfikator zasobu subskrypcji udziału w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="cddec-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="cddec-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cddec-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="cddec-128">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="cddec-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="cddec-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="cddec-129">-SynchronizationId</span></span>
<span data-ttu-id="cddec-130">Identyfikator synchronizacji, który musi zostać zatrzymany</span><span class="sxs-lookup"><span data-stu-id="cddec-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="cddec-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cddec-131">-Confirm</span></span>
<span data-ttu-id="cddec-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cddec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddec-133">-WhatIf</span></span>
<span data-ttu-id="cddec-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cddec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cddec-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cddec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cddec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddec-136">CommonParameters</span></span>
<span data-ttu-id="cddec-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cddec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddec-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cddec-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddec-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cddec-139">INPUTS</span></span>

### <span data-ttu-id="cddec-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cddec-140">System.String</span></span>

### <span data-ttu-id="cddec-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="cddec-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="cddec-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cddec-142">OUTPUTS</span></span>

### <span data-ttu-id="cddec-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="cddec-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="cddec-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cddec-144">NOTES</span></span>

## <span data-ttu-id="cddec-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cddec-145">RELATED LINKS</span></span>
