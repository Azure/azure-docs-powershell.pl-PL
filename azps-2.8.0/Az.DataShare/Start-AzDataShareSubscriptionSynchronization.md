---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 2f0b5cd19e0f21a416c9fd5f3a32462eea86cc4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705645"
---
# <span data-ttu-id="528af-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="528af-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="528af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="528af-102">SYNOPSIS</span></span>
<span data-ttu-id="528af-103">Inicjuje synchronizację subskrypcji udziału.</span><span class="sxs-lookup"><span data-stu-id="528af-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="528af-104">Abonament udostępniania można określić za pomocą identyfikatora zasobu lub jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="528af-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="528af-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="528af-105">SYNTAX</span></span>

### <span data-ttu-id="528af-106">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="528af-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="528af-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="528af-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="528af-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="528af-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="528af-109">Opis</span><span class="sxs-lookup"><span data-stu-id="528af-109">DESCRIPTION</span></span>
<span data-ttu-id="528af-110">Polecenie cmdlet **Start-AzDataShareSubscriptionSynchronization** inicjuje synchronizację subskrypcji udziału</span><span class="sxs-lookup"><span data-stu-id="528af-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="528af-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="528af-111">EXAMPLES</span></span>

### <span data-ttu-id="528af-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="528af-112">Example 1</span></span>
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

<span data-ttu-id="528af-113">Te polecenia inicjują synchronizację dla sharesubscription o nazwie AdsShareSubscription na koncie WikiAds.</span><span class="sxs-lookup"><span data-stu-id="528af-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="528af-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="528af-114">PARAMETERS</span></span>

### <span data-ttu-id="528af-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="528af-115">-AccountName</span></span>
<span data-ttu-id="528af-116">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="528af-116">Azure data share account name</span></span>

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

### <span data-ttu-id="528af-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="528af-117">-AsJob</span></span>
<span data-ttu-id="528af-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="528af-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="528af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528af-119">-DefaultProfile</span></span>
<span data-ttu-id="528af-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="528af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="528af-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="528af-121">-InputObject</span></span>
<span data-ttu-id="528af-122">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="528af-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="528af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="528af-123">-ResourceGroupName</span></span>
<span data-ttu-id="528af-124">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="528af-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="528af-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="528af-125">-ResourceId</span></span>
<span data-ttu-id="528af-126">Identyfikator zasobu subskrypcji udziału w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="528af-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="528af-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="528af-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="528af-128">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="528af-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="528af-129">-Synchronizationmode</span><span class="sxs-lookup"><span data-stu-id="528af-129">-SynchronizationMode</span></span>
<span data-ttu-id="528af-130">Tryb synchronizacji (FullSync lub przyrostowa)</span><span class="sxs-lookup"><span data-stu-id="528af-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="528af-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="528af-131">-Confirm</span></span>
<span data-ttu-id="528af-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="528af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="528af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="528af-133">-WhatIf</span></span>
<span data-ttu-id="528af-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="528af-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="528af-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="528af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="528af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528af-136">CommonParameters</span></span>
<span data-ttu-id="528af-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="528af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528af-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="528af-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528af-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="528af-139">INPUTS</span></span>

### <span data-ttu-id="528af-140">System. String</span><span class="sxs-lookup"><span data-stu-id="528af-140">System.String</span></span>

### <span data-ttu-id="528af-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="528af-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="528af-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="528af-142">OUTPUTS</span></span>

### <span data-ttu-id="528af-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="528af-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="528af-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="528af-144">NOTES</span></span>

## <span data-ttu-id="528af-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="528af-145">RELATED LINKS</span></span>
