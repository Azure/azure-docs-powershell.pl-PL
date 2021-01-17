---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335278"
---
# <span data-ttu-id="b9c91-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b9c91-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b9c91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9c91-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c91-103">Umożliwia zaktualizowanie zasad migawki plików usługi Azure NetApp (ANF) do dodanych opcjonalnych modyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="b9c91-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="b9c91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9c91-104">SYNTAX</span></span>

### <span data-ttu-id="b9c91-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9c91-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c91-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c91-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c91-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c91-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c91-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c91-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c91-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b9c91-109">DESCRIPTION</span></span>
<span data-ttu-id="b9c91-110">Polecenie cmdlet **Update-AzNetAppFilesSnapshotPolicy** modyfikuje zasady migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="b9c91-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="b9c91-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9c91-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c91-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9c91-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="b9c91-113">To polecenie powoduje zmianę zasad tworzenia kopii zapasowej ANF "MySnapshotPolicy", aby uzyskać dane HourlySchedule.</span><span class="sxs-lookup"><span data-stu-id="b9c91-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="b9c91-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9c91-114">PARAMETERS</span></span>

### <span data-ttu-id="b9c91-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9c91-115">-AccountName</span></span>
<span data-ttu-id="b9c91-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="b9c91-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b9c91-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="b9c91-117">-AccountObject</span></span>
<span data-ttu-id="b9c91-118">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="b9c91-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="b9c91-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="b9c91-119">-DailySchedule</span></span>
<span data-ttu-id="b9c91-120">Tablica Hashtable, która reprezentuje harmonogram dzienny</span><span class="sxs-lookup"><span data-stu-id="b9c91-120">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="b9c91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c91-121">-DefaultProfile</span></span>
<span data-ttu-id="b9c91-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c91-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c91-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b9c91-123">-Enabled</span></span>
<span data-ttu-id="b9c91-124">Właściwość decydowania o zasadach jest włączona lub nie</span><span class="sxs-lookup"><span data-stu-id="b9c91-124">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="b9c91-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="b9c91-125">-HourlySchedule</span></span>
<span data-ttu-id="b9c91-126">Tablica Hashtable, która reprezentuje harmonogram godzinowy</span><span class="sxs-lookup"><span data-stu-id="b9c91-126">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="b9c91-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9c91-127">-InputObject</span></span>
<span data-ttu-id="b9c91-128">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="b9c91-128">The snapshot object to remove</span></span>

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

### <span data-ttu-id="b9c91-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b9c91-129">-Location</span></span>
<span data-ttu-id="b9c91-130">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="b9c91-130">The location of the resource</span></span>

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

### <span data-ttu-id="b9c91-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="b9c91-131">-MonthlySchedule</span></span>
<span data-ttu-id="b9c91-132">Tablica Hashtable przedstawiająca Harmonogram miesięczny</span><span class="sxs-lookup"><span data-stu-id="b9c91-132">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="b9c91-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9c91-133">-Name</span></span>
<span data-ttu-id="b9c91-134">Nazwa zasady migawki ANF</span><span class="sxs-lookup"><span data-stu-id="b9c91-134">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="b9c91-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c91-135">-ResourceGroupName</span></span>
<span data-ttu-id="b9c91-136">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="b9c91-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b9c91-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c91-137">-ResourceId</span></span>
<span data-ttu-id="b9c91-138">Identyfikator zasobu w zasadach migawki ANF</span><span class="sxs-lookup"><span data-stu-id="b9c91-138">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="b9c91-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9c91-139">-Tag</span></span>
<span data-ttu-id="b9c91-140">Tablica Hashtable przedstawiająca znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="b9c91-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="b9c91-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="b9c91-141">-WeeklySchedule</span></span>
<span data-ttu-id="b9c91-142">Tablica Hashtable przedstawiająca Harmonogram miesięczny</span><span class="sxs-lookup"><span data-stu-id="b9c91-142">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="b9c91-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9c91-143">-Confirm</span></span>
<span data-ttu-id="b9c91-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c91-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c91-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c91-145">-WhatIf</span></span>
<span data-ttu-id="b9c91-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c91-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c91-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9c91-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c91-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c91-148">CommonParameters</span></span>
<span data-ttu-id="b9c91-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c91-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c91-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9c91-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c91-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9c91-151">INPUTS</span></span>

### <span data-ttu-id="b9c91-152">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c91-152">System.String</span></span>

### <span data-ttu-id="b9c91-153">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b9c91-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b9c91-154">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b9c91-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b9c91-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9c91-155">OUTPUTS</span></span>

### <span data-ttu-id="b9c91-156">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b9c91-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b9c91-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9c91-157">NOTES</span></span>

## <span data-ttu-id="b9c91-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9c91-158">RELATED LINKS</span></span>
