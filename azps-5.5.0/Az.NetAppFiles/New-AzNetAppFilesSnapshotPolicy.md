---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192074"
---
# <span data-ttu-id="b30a6-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b30a6-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b30a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b30a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b30a6-103">Tworzy nowe zasady migawki plików ANF (Azure NetApp Files) dla konta ANF.</span><span class="sxs-lookup"><span data-stu-id="b30a6-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="b30a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b30a6-104">SYNTAX</span></span>

### <span data-ttu-id="b30a6-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b30a6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b30a6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b30a6-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b30a6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b30a6-107">DESCRIPTION</span></span>
<span data-ttu-id="b30a6-108">Polecenie **cmdlet New-AzNetAppFilesActiveDirectory** tworzy nowe zasady migawki dla konta ANF.</span><span class="sxs-lookup"><span data-stu-id="b30a6-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="b30a6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b30a6-109">EXAMPLES</span></span>

### <span data-ttu-id="b30a6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b30a6-110">Example 1</span></span>
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

<span data-ttu-id="b30a6-111">To polecenie tworzy nowe zasady migawki ANF dla konta ANF o nazwie konto "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="b30a6-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="b30a6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b30a6-112">PARAMETERS</span></span>

### <span data-ttu-id="b30a6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b30a6-113">-AccountName</span></span>
<span data-ttu-id="b30a6-114">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="b30a6-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b30a6-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b30a6-115">-AccountObject</span></span>
<span data-ttu-id="b30a6-116">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="b30a6-116">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="b30a6-117">- Harmonogram dzienny</span><span class="sxs-lookup"><span data-stu-id="b30a6-117">-DailySchedule</span></span>
<span data-ttu-id="b30a6-118">Tablica z hasztagami reprezentująca dzienny harmonogram</span><span class="sxs-lookup"><span data-stu-id="b30a6-118">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="b30a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30a6-119">-DefaultProfile</span></span>
<span data-ttu-id="b30a6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b30a6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30a6-121">— włączone</span><span class="sxs-lookup"><span data-stu-id="b30a6-121">-Enabled</span></span>
<span data-ttu-id="b30a6-122">Właściwość do decydowania o włączeniu zasad jest włączona lub nie</span><span class="sxs-lookup"><span data-stu-id="b30a6-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="b30a6-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="b30a6-123">-HourlySchedule</span></span>
<span data-ttu-id="b30a6-124">Tablica z hasztagami reprezentująca harmonogram godzinowy</span><span class="sxs-lookup"><span data-stu-id="b30a6-124">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="b30a6-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b30a6-125">-Location</span></span>
<span data-ttu-id="b30a6-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="b30a6-126">The location of the resource</span></span>

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

### <span data-ttu-id="b30a6-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="b30a6-127">-MonthlySchedule</span></span>
<span data-ttu-id="b30a6-128">Tablica z hasztagami reprezentująca harmonogram montly</span><span class="sxs-lookup"><span data-stu-id="b30a6-128">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="b30a6-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b30a6-129">-Name</span></span>
<span data-ttu-id="b30a6-130">Nazwa zasad migawki ANF</span><span class="sxs-lookup"><span data-stu-id="b30a6-130">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="b30a6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30a6-131">-ResourceGroupName</span></span>
<span data-ttu-id="b30a6-132">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="b30a6-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b30a6-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="b30a6-133">-Tag</span></span>
<span data-ttu-id="b30a6-134">Tablica z hasztagami reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="b30a6-134">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="b30a6-135">- Harmonogram tygodniowy</span><span class="sxs-lookup"><span data-stu-id="b30a6-135">-WeeklySchedule</span></span>
<span data-ttu-id="b30a6-136">Tablica z hasztagami reprezentująca harmonogram montly</span><span class="sxs-lookup"><span data-stu-id="b30a6-136">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="b30a6-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b30a6-137">-Confirm</span></span>
<span data-ttu-id="b30a6-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b30a6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b30a6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b30a6-139">-WhatIf</span></span>
<span data-ttu-id="b30a6-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b30a6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b30a6-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b30a6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b30a6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30a6-142">CommonParameters</span></span>
<span data-ttu-id="b30a6-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30a6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30a6-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b30a6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30a6-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b30a6-145">INPUTS</span></span>

### <span data-ttu-id="b30a6-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b30a6-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b30a6-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b30a6-147">OUTPUTS</span></span>

### <span data-ttu-id="b30a6-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b30a6-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b30a6-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b30a6-149">NOTES</span></span>

## <span data-ttu-id="b30a6-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b30a6-150">RELATED LINKS</span></span>
