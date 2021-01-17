---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359900"
---
# <span data-ttu-id="f070a-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f070a-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f070a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f070a-102">SYNOPSIS</span></span>
<span data-ttu-id="f070a-103">Tworzy nowy wolumin usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="f070a-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="f070a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f070a-104">SYNTAX</span></span>

### <span data-ttu-id="f070a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f070a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f070a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f070a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f070a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f070a-107">DESCRIPTION</span></span>
<span data-ttu-id="f070a-108">Polecenie cmdlet **New-AzNetAppFilesVolume** tworzy wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="f070a-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="f070a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f070a-109">EXAMPLES</span></span>

### <span data-ttu-id="f070a-110">Przykład 1. Tworzenie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="f070a-111">To polecenie tworzy nowy wolumin ANF "MyAnfVolume" w puli "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="f070a-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="f070a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f070a-112">PARAMETERS</span></span>

### <span data-ttu-id="f070a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f070a-113">-AccountName</span></span>
<span data-ttu-id="f070a-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f070a-115">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="f070a-115">-Backup</span></span>
<span data-ttu-id="f070a-116">Tablica Hashtable przedstawiająca obiekt kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f070a-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="f070a-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f070a-117">-BackupId</span></span>
<span data-ttu-id="f070a-118">Identyfikator kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f070a-118">Backup ID.</span></span> <span data-ttu-id="f070a-119">Identyfikator UUID (wersja 4) lub identyfikator zasobu służący do identyfikowania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f070a-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="f070a-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="f070a-120">-CreationToken</span></span>
<span data-ttu-id="f070a-121">Unikatowa ścieżka pliku dla woluminu</span><span class="sxs-lookup"><span data-stu-id="f070a-121">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f070a-122">-DefaultProfile</span></span>
<span data-ttu-id="f070a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f070a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f070a-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="f070a-124">-ExportPolicy</span></span>
<span data-ttu-id="f070a-125">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="f070a-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="f070a-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="f070a-126">-KerberosEnabled</span></span>
<span data-ttu-id="f070a-127">Opis, czy dla woluminu jest włączony protokół Kerberos</span><span class="sxs-lookup"><span data-stu-id="f070a-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="f070a-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f070a-128">-Location</span></span>
<span data-ttu-id="f070a-129">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="f070a-129">The location of the resource</span></span>

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

### <span data-ttu-id="f070a-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f070a-130">-Name</span></span>
<span data-ttu-id="f070a-131">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-131">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f070a-132">-PoolName</span></span>
<span data-ttu-id="f070a-133">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f070a-134">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="f070a-134">-PoolObject</span></span>
<span data-ttu-id="f070a-135">Pula dla nowego obiektu woluminu</span><span class="sxs-lookup"><span data-stu-id="f070a-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="f070a-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="f070a-136">-ProtocolType</span></span>
<span data-ttu-id="f070a-137">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="f070a-137">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="f070a-138">-ReplicationObject</span></span>
<span data-ttu-id="f070a-139">Tablica Hashtable przedstawiająca obiekt replikacji</span><span class="sxs-lookup"><span data-stu-id="f070a-139">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f070a-140">-ResourceGroupName</span></span>
<span data-ttu-id="f070a-141">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f070a-142">— Zabezpieczenia</span><span class="sxs-lookup"><span data-stu-id="f070a-142">-SecurityStyle</span></span>
<span data-ttu-id="f070a-143">Styl zabezpieczeń głośności.</span><span class="sxs-lookup"><span data-stu-id="f070a-143">The security style of volume.</span></span> <span data-ttu-id="f070a-144">Możliwe wartości to: NTFS, "UNIX"</span><span class="sxs-lookup"><span data-stu-id="f070a-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="f070a-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f070a-145">-ServiceLevel</span></span>
<span data-ttu-id="f070a-146">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-146">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-147">-Migawka</span><span class="sxs-lookup"><span data-stu-id="f070a-147">-Snapshot</span></span>
<span data-ttu-id="f070a-148">Tablica Hashtable przedstawiająca obiekt Snapshot</span><span class="sxs-lookup"><span data-stu-id="f070a-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="f070a-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="f070a-150">Jeśli ta funkcja jest włączona (prawda), wolumin będzie zawierać katalog Snapshot (tylko do odczytu), który zapewnia dostęp do każdej migawki woluminu (domyślnie prawda).</span><span class="sxs-lookup"><span data-stu-id="f070a-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="f070a-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f070a-151">-SnapshotId</span></span>
<span data-ttu-id="f070a-152">Utwórz wolumin na podstawie migawki.</span><span class="sxs-lookup"><span data-stu-id="f070a-152">Create volume from a snapshot.</span></span> <span data-ttu-id="f070a-153">Identyfikator UUID (wersja 4) lub identyfikator zasobu służący do identyfikowania migawki</span><span class="sxs-lookup"><span data-stu-id="f070a-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="f070a-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f070a-154">-SubnetId</span></span>
<span data-ttu-id="f070a-155">Identyfikator URI zasobu platformy Azure dla delegowanej podsieci</span><span class="sxs-lookup"><span data-stu-id="f070a-155">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="f070a-156">-Tag</span></span>
<span data-ttu-id="f070a-157">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="f070a-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f070a-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="f070a-158">-ThroughputMibps</span></span>
<span data-ttu-id="f070a-159">Maksymalna produktywność w Mibps, którą można osiągnąć w tym woluminie</span><span class="sxs-lookup"><span data-stu-id="f070a-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="f070a-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="f070a-160">-UsageThreshold</span></span>
<span data-ttu-id="f070a-161">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="f070a-161">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f070a-162">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="f070a-162">-VolumeType</span></span>
<span data-ttu-id="f070a-163">Typ woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="f070a-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="f070a-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f070a-164">-Confirm</span></span>
<span data-ttu-id="f070a-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f070a-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f070a-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f070a-166">-WhatIf</span></span>
<span data-ttu-id="f070a-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f070a-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f070a-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f070a-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f070a-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f070a-169">CommonParameters</span></span>
<span data-ttu-id="f070a-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f070a-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f070a-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f070a-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f070a-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f070a-172">INPUTS</span></span>

### <span data-ttu-id="f070a-173">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f070a-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f070a-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f070a-174">OUTPUTS</span></span>

### <span data-ttu-id="f070a-175">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f070a-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f070a-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f070a-176">NOTES</span></span>

## <span data-ttu-id="f070a-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f070a-177">RELATED LINKS</span></span>
