---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498850"
---
# <span data-ttu-id="e6765-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e6765-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e6765-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6765-102">SYNOPSIS</span></span>
<span data-ttu-id="e6765-103">Tworzy nowe zasady migawki plików usługi Azure NetApp (ANF) dla konta usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="e6765-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="e6765-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6765-104">SYNTAX</span></span>

### <span data-ttu-id="e6765-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6765-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6765-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6765-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6765-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e6765-107">DESCRIPTION</span></span>
<span data-ttu-id="e6765-108">Polecenie cmdlet **New-AzNetAppFilesActiveDirectory** tworzy nowe zasady migawki dla konta usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="e6765-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="e6765-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6765-109">EXAMPLES</span></span>

### <span data-ttu-id="e6765-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6765-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="e6765-111">To polecenie tworzy nowe zasady migawki ANF dla konta ANF o nazwie Account (Moje konto).</span><span class="sxs-lookup"><span data-stu-id="e6765-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="e6765-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6765-112">PARAMETERS</span></span>

### <span data-ttu-id="e6765-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e6765-113">-AccountName</span></span>
<span data-ttu-id="e6765-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="e6765-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="e6765-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="e6765-115">-AccountObject</span></span>
<span data-ttu-id="e6765-116">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="e6765-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="e6765-117">-DailySchedule</span></span>
<span data-ttu-id="e6765-118">Tablica Hashtable, która reprezentuje harmonogram dzienny</span><span class="sxs-lookup"><span data-stu-id="e6765-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6765-119">-DefaultProfile</span></span>
<span data-ttu-id="e6765-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6765-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6765-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e6765-121">-Enabled</span></span>
<span data-ttu-id="e6765-122">Właściwość decydowania o zasadach jest włączona lub nie</span><span class="sxs-lookup"><span data-stu-id="e6765-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="e6765-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="e6765-123">-HourlySchedule</span></span>
<span data-ttu-id="e6765-124">Tablica Hashtable, która reprezentuje harmonogram godzinowy</span><span class="sxs-lookup"><span data-stu-id="e6765-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e6765-125">-Location</span></span>
<span data-ttu-id="e6765-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="e6765-126">The location of the resource</span></span>

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

### <span data-ttu-id="e6765-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="e6765-127">-MonthlySchedule</span></span>
<span data-ttu-id="e6765-128">Tablica Hashtable przedstawiająca Harmonogram miesięczny</span><span class="sxs-lookup"><span data-stu-id="e6765-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6765-129">-Name</span></span>
<span data-ttu-id="e6765-130">Nazwa zasady migawki ANF</span><span class="sxs-lookup"><span data-stu-id="e6765-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6765-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6765-132">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="e6765-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e6765-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6765-133">-Tag</span></span>
<span data-ttu-id="e6765-134">Tablica Hashtable przedstawiająca znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="e6765-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="e6765-135">-WeeklySchedule</span></span>
<span data-ttu-id="e6765-136">Tablica Hashtable przedstawiająca Harmonogram miesięczny</span><span class="sxs-lookup"><span data-stu-id="e6765-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6765-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6765-137">-Confirm</span></span>
<span data-ttu-id="e6765-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6765-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6765-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6765-139">-WhatIf</span></span>
<span data-ttu-id="e6765-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6765-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6765-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6765-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6765-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6765-142">CommonParameters</span></span>
<span data-ttu-id="e6765-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6765-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6765-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6765-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6765-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6765-145">INPUTS</span></span>

### <span data-ttu-id="e6765-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e6765-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e6765-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6765-147">OUTPUTS</span></span>

### <span data-ttu-id="e6765-148">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e6765-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e6765-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6765-149">NOTES</span></span>

## <span data-ttu-id="e6765-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6765-150">RELATED LINKS</span></span>
