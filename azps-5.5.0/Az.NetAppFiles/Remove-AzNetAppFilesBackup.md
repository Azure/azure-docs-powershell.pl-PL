---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192051"
---
# <span data-ttu-id="85554-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="85554-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="85554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85554-102">SYNOPSIS</span></span>
<span data-ttu-id="85554-103">Usuwa kopię zapasową plików Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="85554-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="85554-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85554-104">SYNTAX</span></span>

### <span data-ttu-id="85554-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="85554-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85554-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85554-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85554-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85554-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85554-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85554-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85554-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="85554-109">DESCRIPTION</span></span>
<span data-ttu-id="85554-110">Polecenie **cmdlet Remove-AzNetAppFilesBackup** usuwa konto ANF.</span><span class="sxs-lookup"><span data-stu-id="85554-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="85554-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85554-111">EXAMPLES</span></span>

### <span data-ttu-id="85554-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85554-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="85554-113">To polecenie usuwa nową kopię zapasową ANF o nazwie "MyBackup" dla woluminu "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="85554-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="85554-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85554-114">PARAMETERS</span></span>

### <span data-ttu-id="85554-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85554-115">-AccountName</span></span>
<span data-ttu-id="85554-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="85554-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85554-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85554-117">-DefaultProfile</span></span>
<span data-ttu-id="85554-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85554-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85554-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85554-119">-InputObject</span></span>
<span data-ttu-id="85554-120">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="85554-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85554-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="85554-121">-Name</span></span>
<span data-ttu-id="85554-122">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="85554-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85554-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85554-123">-PassThru</span></span>
<span data-ttu-id="85554-124">Zwracanie, czy określona kopia zapasowa została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="85554-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="85554-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="85554-125">-PoolName</span></span>
<span data-ttu-id="85554-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="85554-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="85554-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85554-127">-ResourceGroupName</span></span>
<span data-ttu-id="85554-128">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="85554-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="85554-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85554-129">-ResourceId</span></span>
<span data-ttu-id="85554-130">Identyfikator zasobu kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="85554-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="85554-131">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="85554-131">-VolumeName</span></span>
<span data-ttu-id="85554-132">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="85554-132">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85554-133">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="85554-133">-VolumeObject</span></span>
<span data-ttu-id="85554-134">Obiekt woluminu zawierający kopię zapasową do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="85554-134">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85554-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85554-135">-Confirm</span></span>
<span data-ttu-id="85554-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="85554-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85554-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85554-137">-WhatIf</span></span>
<span data-ttu-id="85554-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85554-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85554-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="85554-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85554-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85554-140">CommonParameters</span></span>
<span data-ttu-id="85554-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85554-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85554-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85554-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85554-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85554-143">INPUTS</span></span>

### <span data-ttu-id="85554-144">System.String</span><span class="sxs-lookup"><span data-stu-id="85554-144">System.String</span></span>

### <span data-ttu-id="85554-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="85554-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="85554-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="85554-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="85554-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85554-147">OUTPUTS</span></span>

### <span data-ttu-id="85554-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="85554-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="85554-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85554-149">NOTES</span></span>

## <span data-ttu-id="85554-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85554-150">RELATED LINKS</span></span>
