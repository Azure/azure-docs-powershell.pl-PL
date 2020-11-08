---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064144"
---
# <span data-ttu-id="5e2cf-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="5e2cf-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="5e2cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2cf-103">Tworzenie ustawienia synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="5e2cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e2cf-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e2cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="5e2cf-106">**Nowe-AzDataShareSynchronizationSetting** tworzy ustawienia synchronizacji dla funkcji Udostępnij w udziale dla interwału cykliczności codziennego lub godzinowego w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="5e2cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e2cf-107">EXAMPLES</span></span>

### <span data-ttu-id="5e2cf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e2cf-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="5e2cf-109">To polecenie powoduje utworzenie ustawienia synchronizacji dla interwału cykli dziennego w 9:00 dla udziału AdsShare w WikiAds kont udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="5e2cf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e2cf-110">PARAMETERS</span></span>

### <span data-ttu-id="5e2cf-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e2cf-111">-AccountName</span></span>
<span data-ttu-id="5e2cf-112">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="5e2cf-112">Azure data share account name</span></span>

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

### <span data-ttu-id="5e2cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2cf-113">-DefaultProfile</span></span>
<span data-ttu-id="5e2cf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e2cf-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e2cf-115">-Name</span></span>
<span data-ttu-id="5e2cf-116">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="5e2cf-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="5e2cf-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="5e2cf-117">-RecurrenceInterval</span></span>
<span data-ttu-id="5e2cf-118">Interwał cyklu dla ustawienia synchronizacji (dzień lub godzina)</span><span class="sxs-lookup"><span data-stu-id="5e2cf-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="5e2cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e2cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e2cf-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="5e2cf-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="5e2cf-121">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="5e2cf-121">-ShareName</span></span>
<span data-ttu-id="5e2cf-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e2cf-122">Azure data share name</span></span>

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

### <span data-ttu-id="5e2cf-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="5e2cf-123">-SynchronizationTime</span></span>
<span data-ttu-id="5e2cf-124">Godzina rozpoczęcia zaplanowanego ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="5e2cf-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="5e2cf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e2cf-125">-Confirm</span></span>
<span data-ttu-id="5e2cf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e2cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e2cf-127">-WhatIf</span></span>
<span data-ttu-id="5e2cf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e2cf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e2cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2cf-130">CommonParameters</span></span>
<span data-ttu-id="5e2cf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e2cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2cf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e2cf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2cf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e2cf-133">INPUTS</span></span>

### <span data-ttu-id="5e2cf-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5e2cf-134">None</span></span>

## <span data-ttu-id="5e2cf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e2cf-135">OUTPUTS</span></span>

### <span data-ttu-id="5e2cf-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="5e2cf-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="5e2cf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e2cf-137">NOTES</span></span>

## <span data-ttu-id="5e2cf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e2cf-138">RELATED LINKS</span></span>
