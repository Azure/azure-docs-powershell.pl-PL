---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324357"
---
# <span data-ttu-id="7e97f-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="7e97f-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="7e97f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e97f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e97f-103">Tworzenie ustawienia synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="7e97f-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="7e97f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e97f-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e97f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e97f-105">DESCRIPTION</span></span>
<span data-ttu-id="7e97f-106">**Nowe-AzDataShareSynchronizationSetting** tworzy ustawienia synchronizacji dla funkcji Udostępnij w udziale dla interwału cykliczności codziennego lub godzinowego w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="7e97f-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="7e97f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e97f-107">EXAMPLES</span></span>

### <span data-ttu-id="7e97f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e97f-108">Example 1</span></span>
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

<span data-ttu-id="7e97f-109">To polecenie powoduje utworzenie ustawienia synchronizacji dla interwału cykli dziennego w 9:00 dla udziału AdsShare w WikiAds kont udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="7e97f-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="7e97f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e97f-110">PARAMETERS</span></span>

### <span data-ttu-id="7e97f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e97f-111">-AccountName</span></span>
<span data-ttu-id="7e97f-112">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="7e97f-112">Azure data share account name</span></span>

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

### <span data-ttu-id="7e97f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e97f-113">-DefaultProfile</span></span>
<span data-ttu-id="7e97f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e97f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e97f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e97f-115">-Name</span></span>
<span data-ttu-id="7e97f-116">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="7e97f-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="7e97f-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="7e97f-117">-RecurrenceInterval</span></span>
<span data-ttu-id="7e97f-118">Interwał cyklu dla ustawienia synchronizacji (dzień lub godzina)</span><span class="sxs-lookup"><span data-stu-id="7e97f-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="7e97f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e97f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e97f-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="7e97f-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="7e97f-121">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="7e97f-121">-ShareName</span></span>
<span data-ttu-id="7e97f-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="7e97f-122">Azure data share name</span></span>

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

### <span data-ttu-id="7e97f-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="7e97f-123">-SynchronizationTime</span></span>
<span data-ttu-id="7e97f-124">Godzina rozpoczęcia zaplanowanego ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="7e97f-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="7e97f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e97f-125">-Confirm</span></span>
<span data-ttu-id="7e97f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e97f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e97f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e97f-127">-WhatIf</span></span>
<span data-ttu-id="7e97f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e97f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e97f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e97f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e97f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e97f-130">CommonParameters</span></span>
<span data-ttu-id="7e97f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e97f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e97f-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e97f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e97f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e97f-133">INPUTS</span></span>

### <span data-ttu-id="7e97f-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7e97f-134">None</span></span>

## <span data-ttu-id="7e97f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e97f-135">OUTPUTS</span></span>

### <span data-ttu-id="7e97f-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="7e97f-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="7e97f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e97f-137">NOTES</span></span>

## <span data-ttu-id="7e97f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e97f-138">RELATED LINKS</span></span>
