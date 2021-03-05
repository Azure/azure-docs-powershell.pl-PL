---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: 95b7ad2ea93f1e1b22eafe3fbaae811dc33f24d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968129"
---
# <span data-ttu-id="ef71a-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="ef71a-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="ef71a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef71a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef71a-103">Aktualizuje kopię zapasową plików ANF (Azure NetApp Files) na dostarczane opcjonalne modyfikatory.</span><span class="sxs-lookup"><span data-stu-id="ef71a-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="ef71a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef71a-104">SYNTAX</span></span>

### <span data-ttu-id="ef71a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ef71a-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef71a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef71a-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef71a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef71a-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef71a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef71a-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef71a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef71a-109">DESCRIPTION</span></span>
<span data-ttu-id="ef71a-110">Polecenie **cmdlet Update-AzNetAppFilesBackup** modyfikuje kopię zapasową ANF.</span><span class="sxs-lookup"><span data-stu-id="ef71a-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="ef71a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef71a-111">EXAMPLES</span></span>

### <span data-ttu-id="ef71a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef71a-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="ef71a-113">To polecenie wykonuje aktualizację danej kopii zapasowej, modyfikując nazwę użytkownika do podanej nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ef71a-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="ef71a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef71a-114">PARAMETERS</span></span>

### <span data-ttu-id="ef71a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef71a-115">-AccountName</span></span>
<span data-ttu-id="ef71a-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="ef71a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ef71a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef71a-117">-DefaultProfile</span></span>
<span data-ttu-id="ef71a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef71a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef71a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef71a-119">-InputObject</span></span>
<span data-ttu-id="ef71a-120">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="ef71a-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="ef71a-121">— Label</span><span class="sxs-lookup"><span data-stu-id="ef71a-121">-Label</span></span>
<span data-ttu-id="ef71a-122">Etykieta kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="ef71a-122">Label for backup</span></span>

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

### <span data-ttu-id="ef71a-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ef71a-123">-Location</span></span>
<span data-ttu-id="ef71a-124">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="ef71a-124">The location of the resource</span></span>

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

### <span data-ttu-id="ef71a-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ef71a-125">-Name</span></span>
<span data-ttu-id="ef71a-126">Nazwa zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="ef71a-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="ef71a-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ef71a-127">-PoolName</span></span>
<span data-ttu-id="ef71a-128">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="ef71a-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ef71a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef71a-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef71a-130">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="ef71a-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ef71a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef71a-131">-ResourceId</span></span>
<span data-ttu-id="ef71a-132">Identyfikator zasobu kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="ef71a-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="ef71a-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="ef71a-133">-Tag</span></span>
<span data-ttu-id="ef71a-134">Tabela skrótów reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="ef71a-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ef71a-135">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="ef71a-135">-VolumeName</span></span>
<span data-ttu-id="ef71a-136">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="ef71a-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ef71a-137">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="ef71a-137">-VolumeObject</span></span>
<span data-ttu-id="ef71a-138">Obiekt woluminu zawierający kopię zapasową do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="ef71a-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="ef71a-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef71a-139">-Confirm</span></span>
<span data-ttu-id="ef71a-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ef71a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef71a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef71a-141">-WhatIf</span></span>
<span data-ttu-id="ef71a-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef71a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef71a-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ef71a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef71a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef71a-144">CommonParameters</span></span>
<span data-ttu-id="ef71a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef71a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef71a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef71a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef71a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef71a-147">INPUTS</span></span>

### <span data-ttu-id="ef71a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ef71a-148">System.String</span></span>

### <span data-ttu-id="ef71a-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ef71a-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="ef71a-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="ef71a-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="ef71a-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef71a-151">OUTPUTS</span></span>

### <span data-ttu-id="ef71a-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ef71a-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="ef71a-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef71a-153">NOTES</span></span>

## <span data-ttu-id="ef71a-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef71a-154">RELATED LINKS</span></span>
