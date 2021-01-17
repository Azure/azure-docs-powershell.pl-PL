---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380410"
---
# <span data-ttu-id="d9efe-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d9efe-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d9efe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9efe-102">SYNOPSIS</span></span>
<span data-ttu-id="d9efe-103">Aktualizuje wolumin pliki usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="d9efe-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="d9efe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9efe-104">SYNTAX</span></span>

### <span data-ttu-id="d9efe-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9efe-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9efe-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9efe-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9efe-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9efe-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9efe-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9efe-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9efe-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d9efe-109">DESCRIPTION</span></span>
<span data-ttu-id="d9efe-110">Polecenie cmdlet **Update-AzNetAppFilesVolume** AKTUALIZUJE wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="d9efe-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="d9efe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9efe-111">EXAMPLES</span></span>

### <span data-ttu-id="d9efe-112">Przykład 1: aktualizowanie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="d9efe-113">To polecenie aktualizuje wolumin ANF "MyAnfVolume" przy użyciu nowego rozmiaru UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="d9efe-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="d9efe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9efe-114">PARAMETERS</span></span>

### <span data-ttu-id="d9efe-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d9efe-115">-AccountName</span></span>
<span data-ttu-id="d9efe-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d9efe-117">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="d9efe-117">-Backup</span></span>
<span data-ttu-id="d9efe-118">Tablica Hashtable przedstawiająca obiekt kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="d9efe-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="d9efe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9efe-119">-DefaultProfile</span></span>
<span data-ttu-id="d9efe-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9efe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9efe-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="d9efe-121">-ExportPolicy</span></span>
<span data-ttu-id="d9efe-122">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="d9efe-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="d9efe-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9efe-123">-InputObject</span></span>
<span data-ttu-id="d9efe-124">Obiekt woluminu do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="d9efe-124">The volume object to update</span></span>

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

### <span data-ttu-id="d9efe-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9efe-125">-Location</span></span>
<span data-ttu-id="d9efe-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d9efe-126">The location of the resource</span></span>

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

### <span data-ttu-id="d9efe-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9efe-127">-Name</span></span>
<span data-ttu-id="d9efe-128">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d9efe-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d9efe-129">-PoolName</span></span>
<span data-ttu-id="d9efe-130">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d9efe-131">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="d9efe-131">-PoolObject</span></span>
<span data-ttu-id="d9efe-132">Obiekt Pool zawierający wolumin do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="d9efe-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="d9efe-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9efe-133">-ResourceGroupName</span></span>
<span data-ttu-id="d9efe-134">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d9efe-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9efe-135">-ResourceId</span></span>
<span data-ttu-id="d9efe-136">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="d9efe-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d9efe-137">-ServiceLevel</span></span>
<span data-ttu-id="d9efe-138">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d9efe-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="d9efe-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9efe-139">-Tag</span></span>
<span data-ttu-id="d9efe-140">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="d9efe-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d9efe-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="d9efe-141">-ThroughputMibps</span></span>
<span data-ttu-id="d9efe-142">Maksymalna produktywność w Mibps, którą można osiągnąć w tym woluminie</span><span class="sxs-lookup"><span data-stu-id="d9efe-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="d9efe-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d9efe-143">-UsageThreshold</span></span>
<span data-ttu-id="d9efe-144">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="d9efe-144">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="d9efe-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9efe-145">-Confirm</span></span>
<span data-ttu-id="d9efe-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9efe-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9efe-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9efe-147">-WhatIf</span></span>
<span data-ttu-id="d9efe-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9efe-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9efe-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9efe-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9efe-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9efe-150">CommonParameters</span></span>
<span data-ttu-id="d9efe-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9efe-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9efe-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9efe-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9efe-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9efe-153">INPUTS</span></span>

### <span data-ttu-id="d9efe-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d9efe-154">System.String</span></span>

### <span data-ttu-id="d9efe-155">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d9efe-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="d9efe-156">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d9efe-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d9efe-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9efe-157">OUTPUTS</span></span>

### <span data-ttu-id="d9efe-158">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d9efe-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d9efe-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9efe-159">NOTES</span></span>

## <span data-ttu-id="d9efe-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9efe-160">RELATED LINKS</span></span>
