---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: f7342ec33e712407987da28b232670d56bdcab66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705664"
---
# <span data-ttu-id="cd6a9-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="cd6a9-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="cd6a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6a9-103">Tworzy wyzwalacz dla subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="cd6a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd6a9-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd6a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd6a9-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6a9-106">Polecenie cmdlet **New-AzDataShareTrigger** tworzy wyzwalacz dla subskrypcji udostępniania dla określonego interwału cyklu i czasu synchronizacji w ramach konta udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="cd6a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd6a9-107">EXAMPLES</span></span>

### <span data-ttu-id="cd6a9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd6a9-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="cd6a9-109">To polecenie tworzy nowy wyzwalacz AdsTrigger na potrzeby udostępniania subskrypcji AdsShareSubscription za pomocą interwału cykli dziennych 9.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="cd6a9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd6a9-110">PARAMETERS</span></span>

### <span data-ttu-id="cd6a9-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd6a9-111">-AccountName</span></span>
<span data-ttu-id="cd6a9-112">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="cd6a9-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd6a9-113">-AsJob</span></span>
<span data-ttu-id="cd6a9-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="cd6a9-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="cd6a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6a9-115">-DefaultProfile</span></span>
<span data-ttu-id="cd6a9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd6a9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd6a9-117">-Name</span></span>
<span data-ttu-id="cd6a9-118">Nazwa wyzwalacza udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="cd6a9-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a9-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="cd6a9-119">-RecurrenceInterval</span></span>
<span data-ttu-id="cd6a9-120">Interwał cyklu dla wyzwalacza (dzień lub godzina)</span><span class="sxs-lookup"><span data-stu-id="cd6a9-120">The recurrence interval for the trigger (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd6a9-122">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="cd6a9-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a9-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cd6a9-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="cd6a9-124">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="cd6a9-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a9-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="cd6a9-125">-SynchronizationTime</span></span>
<span data-ttu-id="cd6a9-126">Godzina rozpoczęcia zaplanowanej synchronizacji wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="cd6a9-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a9-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd6a9-127">-Confirm</span></span>
<span data-ttu-id="cd6a9-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd6a9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6a9-129">-WhatIf</span></span>
<span data-ttu-id="cd6a9-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd6a9-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd6a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6a9-132">CommonParameters</span></span>
<span data-ttu-id="cd6a9-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd6a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6a9-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6a9-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd6a9-135">INPUTS</span></span>

### <span data-ttu-id="cd6a9-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cd6a9-136">None</span></span>

## <span data-ttu-id="cd6a9-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd6a9-137">OUTPUTS</span></span>

### <span data-ttu-id="cd6a9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="cd6a9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="cd6a9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd6a9-139">NOTES</span></span>

## <span data-ttu-id="cd6a9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd6a9-140">RELATED LINKS</span></span>