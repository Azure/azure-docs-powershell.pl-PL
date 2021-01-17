---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380466"
---
# <span data-ttu-id="4a896-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="4a896-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="4a896-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a896-102">SYNOPSIS</span></span>
<span data-ttu-id="4a896-103">Umożliwia zaktualizowanie kopii zapasowej plików usługi Azure NetApp (ANF) do dodanych opcjonalnych modyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="4a896-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="4a896-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a896-104">SYNTAX</span></span>

### <span data-ttu-id="4a896-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a896-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a896-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a896-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a896-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a896-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a896-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a896-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a896-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4a896-109">DESCRIPTION</span></span>
<span data-ttu-id="4a896-110">Polecenie cmdlet **Update-AzNetAppFilesBackup** modyfikuje kopię zapasową ANF.</span><span class="sxs-lookup"><span data-stu-id="4a896-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="4a896-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a896-111">EXAMPLES</span></span>

### <span data-ttu-id="4a896-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a896-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="4a896-113">To polecenie wykonuje aktualizację w danej kopii zapasowej, modyfikując określoną nazwę użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4a896-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="4a896-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a896-114">PARAMETERS</span></span>

### <span data-ttu-id="4a896-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a896-115">-AccountName</span></span>
<span data-ttu-id="4a896-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="4a896-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="4a896-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a896-117">-DefaultProfile</span></span>
<span data-ttu-id="4a896-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a896-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a896-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a896-119">-InputObject</span></span>
<span data-ttu-id="4a896-120">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="4a896-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="4a896-121">-Label</span><span class="sxs-lookup"><span data-stu-id="4a896-121">-Label</span></span>
<span data-ttu-id="4a896-122">Etykieta kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="4a896-122">Label for backup</span></span>

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

### <span data-ttu-id="4a896-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4a896-123">-Location</span></span>
<span data-ttu-id="4a896-124">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="4a896-124">The location of the resource</span></span>

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

### <span data-ttu-id="4a896-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a896-125">-Name</span></span>
<span data-ttu-id="4a896-126">Nazwa zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="4a896-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="4a896-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4a896-127">-PoolName</span></span>
<span data-ttu-id="4a896-128">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="4a896-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="4a896-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a896-129">-ResourceGroupName</span></span>
<span data-ttu-id="4a896-130">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="4a896-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4a896-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a896-131">-ResourceId</span></span>
<span data-ttu-id="4a896-132">Identyfikator zasobu kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="4a896-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="4a896-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a896-133">-Tag</span></span>
<span data-ttu-id="4a896-134">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="4a896-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="4a896-135">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="4a896-135">-VolumeName</span></span>
<span data-ttu-id="4a896-136">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="4a896-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="4a896-137">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="4a896-137">-VolumeObject</span></span>
<span data-ttu-id="4a896-138">Obiekt woluminu zawierający kopię zapasową do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="4a896-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="4a896-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a896-139">-Confirm</span></span>
<span data-ttu-id="4a896-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a896-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a896-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a896-141">-WhatIf</span></span>
<span data-ttu-id="4a896-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a896-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a896-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a896-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a896-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a896-144">CommonParameters</span></span>
<span data-ttu-id="4a896-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a896-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a896-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a896-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a896-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a896-147">INPUTS</span></span>

### <span data-ttu-id="4a896-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4a896-148">System.String</span></span>

### <span data-ttu-id="4a896-149">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="4a896-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="4a896-150">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="4a896-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="4a896-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a896-151">OUTPUTS</span></span>

### <span data-ttu-id="4a896-152">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4a896-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4a896-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a896-153">NOTES</span></span>

## <span data-ttu-id="4a896-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a896-154">RELATED LINKS</span></span>
