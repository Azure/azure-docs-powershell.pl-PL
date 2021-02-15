---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203282"
---
# <span data-ttu-id="a3f4f-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a3f4f-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a3f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f4f-103">Aktualizuje głośność plików ANF (Azure NetApp Files) zgodnie z dostępnymi opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="a3f4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3f4f-104">SYNTAX</span></span>

### <span data-ttu-id="a3f4f-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a3f4f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3f4f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3f4f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3f4f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3f4f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3f4f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3f4f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f4f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3f4f-109">DESCRIPTION</span></span>
<span data-ttu-id="a3f4f-110">Polecenie **cmdlet Update-AzNetAppFilesVolume** aktualizuje wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="a3f4f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3f4f-111">EXAMPLES</span></span>

### <span data-ttu-id="a3f4f-112">Przykład 1. Aktualizowanie głośności ANF</span><span class="sxs-lookup"><span data-stu-id="a3f4f-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="a3f4f-113">To polecenie aktualizuje wolumin ANF "MyAnfVolume" o nowy rozmiar UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="a3f4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3f4f-114">PARAMETERS</span></span>

### <span data-ttu-id="a3f4f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3f4f-115">-AccountName</span></span>
<span data-ttu-id="a3f4f-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="a3f4f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a3f4f-117">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="a3f4f-117">-Backup</span></span>
<span data-ttu-id="a3f4f-118">Tablica skrótów reprezentująca obiekt kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="a3f4f-118">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f4f-119">-DefaultProfile</span></span>
<span data-ttu-id="a3f4f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f4f-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="a3f4f-121">-ExportPolicy</span></span>
<span data-ttu-id="a3f4f-122">Tablica z hasztagami reprezentująca zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="a3f4f-122">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3f4f-123">-InputObject</span></span>
<span data-ttu-id="a3f4f-124">Obiekt głośności do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a3f4f-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a3f4f-125">-Location</span></span>
<span data-ttu-id="a3f4f-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="a3f4f-126">The location of the resource</span></span>

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

### <span data-ttu-id="a3f4f-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3f4f-127">-Name</span></span>
<span data-ttu-id="a3f4f-128">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="a3f4f-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a3f4f-129">-PoolName</span></span>
<span data-ttu-id="a3f4f-130">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="a3f4f-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a3f4f-131">- PoolObject</span><span class="sxs-lookup"><span data-stu-id="a3f4f-131">-PoolObject</span></span>
<span data-ttu-id="a3f4f-132">Obiekt puli zawierający wielkość do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a3f4f-132">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f4f-133">-ResourceGroupName</span></span>
<span data-ttu-id="a3f4f-134">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="a3f4f-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a3f4f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3f4f-135">-ResourceId</span></span>
<span data-ttu-id="a3f4f-136">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="a3f4f-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="a3f4f-137">- ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="a3f4f-137">-ServiceLevel</span></span>
<span data-ttu-id="a3f4f-138">Poziom usługi w ilości anfów</span><span class="sxs-lookup"><span data-stu-id="a3f4f-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="a3f4f-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="a3f4f-139">-Tag</span></span>
<span data-ttu-id="a3f4f-140">Tabela skrótów reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="a3f4f-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a3f4f-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="a3f4f-141">-ThroughputMibps</span></span>
<span data-ttu-id="a3f4f-142">Maksymalna przepływność w mibpsach, która może zostać osiągnięta przy tej ilości</span><span class="sxs-lookup"><span data-stu-id="a3f4f-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="a3f4f-143">-UsageThreshold</span></span>
<span data-ttu-id="a3f4f-144">Maksymalny przydział magazynowania dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="a3f4f-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f4f-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3f4f-145">-Confirm</span></span>
<span data-ttu-id="a3f4f-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3f4f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f4f-147">-WhatIf</span></span>
<span data-ttu-id="a3f4f-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f4f-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3f4f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f4f-150">CommonParameters</span></span>
<span data-ttu-id="a3f4f-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f4f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f4f-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3f4f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f4f-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3f4f-153">INPUTS</span></span>

### <span data-ttu-id="a3f4f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a3f4f-154">System.String</span></span>

### <span data-ttu-id="a3f4f-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a3f4f-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="a3f4f-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a3f4f-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a3f4f-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3f4f-157">OUTPUTS</span></span>

### <span data-ttu-id="a3f4f-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a3f4f-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a3f4f-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3f4f-159">NOTES</span></span>

## <span data-ttu-id="a3f4f-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3f4f-160">RELATED LINKS</span></span>
