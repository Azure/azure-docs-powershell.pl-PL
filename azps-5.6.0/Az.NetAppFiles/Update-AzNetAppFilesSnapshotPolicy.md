---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cf099afe95eec37e070cc2b09d30b7f4b2766b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968081"
---
# <span data-ttu-id="f2495-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f2495-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f2495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2495-102">SYNOPSIS</span></span>
<span data-ttu-id="f2495-103">Aktualizuje zasady migawki plików ANF (Azure NetApp Files) na dostarczane opcjonalne modyfikatory.</span><span class="sxs-lookup"><span data-stu-id="f2495-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="f2495-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2495-104">SYNTAX</span></span>

### <span data-ttu-id="f2495-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f2495-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2495-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2495-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2495-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2495-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2495-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2495-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2495-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2495-109">DESCRIPTION</span></span>
<span data-ttu-id="f2495-110">Polecenie **cmdlet Update-AzNetAppFilesSnapshotPolicy** modyfikuje zasady migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="f2495-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="f2495-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2495-111">EXAMPLES</span></span>

### <span data-ttu-id="f2495-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2495-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="f2495-113">To polecenie zmienia zasady kopii zapasowej ANF "MySnapshotPolicy", aby mieć podany harmonogram godzinowy.</span><span class="sxs-lookup"><span data-stu-id="f2495-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="f2495-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2495-114">PARAMETERS</span></span>

### <span data-ttu-id="f2495-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2495-115">-AccountName</span></span>
<span data-ttu-id="f2495-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="f2495-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f2495-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f2495-117">-AccountObject</span></span>
<span data-ttu-id="f2495-118">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="f2495-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="f2495-119">- Harmonogram dzienny</span><span class="sxs-lookup"><span data-stu-id="f2495-119">-DailySchedule</span></span>
<span data-ttu-id="f2495-120">Tablica z hasztagami reprezentująca dzienny harmonogram</span><span class="sxs-lookup"><span data-stu-id="f2495-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2495-121">-DefaultProfile</span></span>
<span data-ttu-id="f2495-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2495-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2495-123">— włączone</span><span class="sxs-lookup"><span data-stu-id="f2495-123">-Enabled</span></span>
<span data-ttu-id="f2495-124">Właściwość do decydowania o włączeniu zasad jest włączona lub nie</span><span class="sxs-lookup"><span data-stu-id="f2495-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="f2495-125">-HourlySchedule</span></span>
<span data-ttu-id="f2495-126">Tablica z hasztagami reprezentująca harmonogram godzinowy</span><span class="sxs-lookup"><span data-stu-id="f2495-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2495-127">-InputObject</span></span>
<span data-ttu-id="f2495-128">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="f2495-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2495-129">-Location</span></span>
<span data-ttu-id="f2495-130">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="f2495-130">The location of the resource</span></span>

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

### <span data-ttu-id="f2495-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="f2495-131">-MonthlySchedule</span></span>
<span data-ttu-id="f2495-132">Tablica z hasztagami reprezentująca harmonogram montly</span><span class="sxs-lookup"><span data-stu-id="f2495-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2495-133">-Name</span></span>
<span data-ttu-id="f2495-134">Nazwa zasad migawki ANF</span><span class="sxs-lookup"><span data-stu-id="f2495-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2495-135">-ResourceGroupName</span></span>
<span data-ttu-id="f2495-136">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="f2495-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f2495-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2495-137">-ResourceId</span></span>
<span data-ttu-id="f2495-138">Identyfikator zasobu zasad migawki ANF</span><span class="sxs-lookup"><span data-stu-id="f2495-138">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="f2495-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="f2495-139">-Tag</span></span>
<span data-ttu-id="f2495-140">Tablica z hasztagami reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="f2495-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="f2495-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="f2495-141">-WeeklySchedule</span></span>
<span data-ttu-id="f2495-142">Tablica z hasztagami reprezentująca harmonogram montly</span><span class="sxs-lookup"><span data-stu-id="f2495-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2495-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2495-143">-Confirm</span></span>
<span data-ttu-id="f2495-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2495-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2495-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2495-145">-WhatIf</span></span>
<span data-ttu-id="f2495-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2495-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2495-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2495-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2495-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2495-148">CommonParameters</span></span>
<span data-ttu-id="f2495-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2495-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2495-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2495-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2495-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2495-151">INPUTS</span></span>

### <span data-ttu-id="f2495-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f2495-152">System.String</span></span>

### <span data-ttu-id="f2495-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f2495-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f2495-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f2495-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f2495-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2495-155">OUTPUTS</span></span>

### <span data-ttu-id="f2495-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f2495-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f2495-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2495-157">NOTES</span></span>

## <span data-ttu-id="f2495-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2495-158">RELATED LINKS</span></span>
