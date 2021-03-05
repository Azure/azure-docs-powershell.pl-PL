---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996696"
---
# <span data-ttu-id="dc1f3-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="dc1f3-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="dc1f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1f3-103">Tworzy ustawienie synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="dc1f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc1f3-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc1f3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1f3-106">Ustawienie **New-AzDataShareSynchronizationSetting** tworzy ustawienie synchronizacji dla udziału na koncie udziału dla interwału cyklu o określonym czasie dziennym lub cogodzinnym.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="dc1f3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="dc1f3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc1f3-108">Example 1</span></span>
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

<span data-ttu-id="dc1f3-109">To polecenia tworzy ustawienie synchronizacji dla interwału cyklu dziennego o godzinie 9:00 dla udostępniania usługi AdsShare w dzieleniu danych konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="dc1f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="dc1f3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc1f3-111">-AccountName</span></span>
<span data-ttu-id="dc1f3-112">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="dc1f3-112">Azure data share account name</span></span>

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

### <span data-ttu-id="dc1f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1f3-113">-DefaultProfile</span></span>
<span data-ttu-id="dc1f3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc1f3-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dc1f3-115">-Name</span></span>
<span data-ttu-id="dc1f3-116">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="dc1f3-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="dc1f3-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="dc1f3-117">-RecurrenceInterval</span></span>
<span data-ttu-id="dc1f3-118">Interwał cyklu ustawienia synchronizacji (dzień lub godzina)</span><span class="sxs-lookup"><span data-stu-id="dc1f3-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="dc1f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc1f3-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="dc1f3-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="dc1f3-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dc1f3-121">-ShareName</span></span>
<span data-ttu-id="dc1f3-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="dc1f3-122">Azure data share name</span></span>

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

### <span data-ttu-id="dc1f3-123">- SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="dc1f3-123">-SynchronizationTime</span></span>
<span data-ttu-id="dc1f3-124">Godzina rozpoczęcia ustawienia zaplanowanej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="dc1f3-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="dc1f3-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc1f3-125">-Confirm</span></span>
<span data-ttu-id="dc1f3-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc1f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc1f3-127">-WhatIf</span></span>
<span data-ttu-id="dc1f3-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc1f3-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc1f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1f3-130">CommonParameters</span></span>
<span data-ttu-id="dc1f3-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1f3-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc1f3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1f3-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc1f3-133">INPUTS</span></span>

### <span data-ttu-id="dc1f3-134">Brak</span><span class="sxs-lookup"><span data-stu-id="dc1f3-134">None</span></span>

## <span data-ttu-id="dc1f3-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc1f3-135">OUTPUTS</span></span>

### <span data-ttu-id="dc1f3-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="dc1f3-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="dc1f3-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc1f3-137">NOTES</span></span>

## <span data-ttu-id="dc1f3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc1f3-138">RELATED LINKS</span></span>
