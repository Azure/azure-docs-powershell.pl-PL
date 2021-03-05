---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 14c2a58c40aa29f1b48902be5d82911f70a71cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968122"
---
# <span data-ttu-id="bcf8d-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcf8d-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="bcf8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcf8d-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf8d-103">Aktualizuje zasady kopii zapasowej usługi Azure NetApp Files (ANF) na opcjonalne modyfikatory.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="bcf8d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bcf8d-104">SYNTAX</span></span>

### <span data-ttu-id="bcf8d-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bcf8d-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf8d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf8d-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf8d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf8d-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf8d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf8d-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcf8d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="bcf8d-109">DESCRIPTION</span></span>
<span data-ttu-id="bcf8d-110">Polecenie **cmdlet Update-AzNetAppFilesBackupPolicy** modyfikuje zasady kopii zapasowej ANF.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="bcf8d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bcf8d-111">EXAMPLES</span></span>

### <span data-ttu-id="bcf8d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bcf8d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="bcf8d-113">To polecenie zmienia zasady kopii zapasowej ANF "MyBackupPolicy", aby mieć dany element DailyBackupsToKeep.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="bcf8d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcf8d-114">PARAMETERS</span></span>

### <span data-ttu-id="bcf8d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcf8d-115">-AccountName</span></span>
<span data-ttu-id="bcf8d-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="bcf8d-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="bcf8d-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="bcf8d-117">-AccountObject</span></span>
<span data-ttu-id="bcf8d-118">Obiekt Account zawierający zasady kopii zapasowej do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="bcf8d-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="bcf8d-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bcf8d-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="bcf8d-120">Dzienna liczba kopii zapasowych do utrzymania</span><span class="sxs-lookup"><span data-stu-id="bcf8d-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf8d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf8d-121">-DefaultProfile</span></span>
<span data-ttu-id="bcf8d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf8d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcf8d-123">-InputObject</span></span>
<span data-ttu-id="bcf8d-124">Obiekt BackupPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="bcf8d-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf8d-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bcf8d-125">-Location</span></span>
<span data-ttu-id="bcf8d-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="bcf8d-126">The location of the resource</span></span>

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

### <span data-ttu-id="bcf8d-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bcf8d-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="bcf8d-128">Miesięczne kopie zapasowe są liczone do utrzymania</span><span class="sxs-lookup"><span data-stu-id="bcf8d-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf8d-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bcf8d-129">-Name</span></span>
<span data-ttu-id="bcf8d-130">Nazwa zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="bcf8d-130">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf8d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf8d-131">-ResourceGroupName</span></span>
<span data-ttu-id="bcf8d-132">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="bcf8d-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="bcf8d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf8d-133">-ResourceId</span></span>
<span data-ttu-id="bcf8d-134">Identyfikator zasobu zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="bcf8d-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="bcf8d-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="bcf8d-135">-Tag</span></span>
<span data-ttu-id="bcf8d-136">Tablica z hasztagami reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="bcf8d-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="bcf8d-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bcf8d-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="bcf8d-138">Cotygodniowe kopie zapasowe są liczone do utrzymania</span><span class="sxs-lookup"><span data-stu-id="bcf8d-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf8d-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bcf8d-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="bcf8d-140">Liczba kopii zapasowych do przechowywania</span><span class="sxs-lookup"><span data-stu-id="bcf8d-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf8d-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcf8d-141">-Confirm</span></span>
<span data-ttu-id="bcf8d-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf8d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf8d-143">-WhatIf</span></span>
<span data-ttu-id="bcf8d-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf8d-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf8d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf8d-146">CommonParameters</span></span>
<span data-ttu-id="bcf8d-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf8d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf8d-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcf8d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf8d-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcf8d-149">INPUTS</span></span>

### <span data-ttu-id="bcf8d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="bcf8d-150">System.String</span></span>

### <span data-ttu-id="bcf8d-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bcf8d-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="bcf8d-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcf8d-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="bcf8d-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcf8d-153">OUTPUTS</span></span>

### <span data-ttu-id="bcf8d-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcf8d-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="bcf8d-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bcf8d-155">NOTES</span></span>

## <span data-ttu-id="bcf8d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcf8d-156">RELATED LINKS</span></span>
