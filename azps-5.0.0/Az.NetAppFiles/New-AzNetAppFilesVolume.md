---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232859"
---
# <span data-ttu-id="56e0e-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="56e0e-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="56e0e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="56e0e-103">Tworzy nowy wolumin usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="56e0e-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="56e0e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56e0e-104">SYNTAX</span></span>

### <span data-ttu-id="56e0e-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56e0e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e0e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e0e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56e0e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56e0e-107">DESCRIPTION</span></span>
<span data-ttu-id="56e0e-108">Polecenie cmdlet **New-AzNetAppFilesVolume** tworzy wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="56e0e-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="56e0e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56e0e-109">EXAMPLES</span></span>

### <span data-ttu-id="56e0e-110">Przykład 1. Tworzenie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="56e0e-111">To polecenie tworzy nowy wolumin ANF "MyAnfVolume" w puli "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="56e0e-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="56e0e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56e0e-112">PARAMETERS</span></span>

### <span data-ttu-id="56e0e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56e0e-113">-AccountName</span></span>
<span data-ttu-id="56e0e-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="56e0e-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="56e0e-115">-CreationToken</span></span>
<span data-ttu-id="56e0e-116">Unikatowa ścieżka pliku dla woluminu</span><span class="sxs-lookup"><span data-stu-id="56e0e-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="56e0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e0e-117">-DefaultProfile</span></span>
<span data-ttu-id="56e0e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56e0e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e0e-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="56e0e-119">-ExportPolicy</span></span>
<span data-ttu-id="56e0e-120">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="56e0e-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="56e0e-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="56e0e-121">-Location</span></span>
<span data-ttu-id="56e0e-122">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="56e0e-122">The location of the resource</span></span>

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

### <span data-ttu-id="56e0e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56e0e-123">-Name</span></span>
<span data-ttu-id="56e0e-124">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="56e0e-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="56e0e-125">-PoolName</span></span>
<span data-ttu-id="56e0e-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="56e0e-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="56e0e-127">-PoolObject</span></span>
<span data-ttu-id="56e0e-128">Pula dla nowego obiektu woluminu</span><span class="sxs-lookup"><span data-stu-id="56e0e-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="56e0e-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="56e0e-129">-ProtocolType</span></span>
<span data-ttu-id="56e0e-130">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="56e0e-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="56e0e-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="56e0e-131">-ReplicationObject</span></span>
<span data-ttu-id="56e0e-132">Tablica Hashtable przedstawiająca obiekt replikacji</span><span class="sxs-lookup"><span data-stu-id="56e0e-132">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="56e0e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e0e-133">-ResourceGroupName</span></span>
<span data-ttu-id="56e0e-134">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="56e0e-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="56e0e-135">-ServiceLevel</span></span>
<span data-ttu-id="56e0e-136">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="56e0e-137">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="56e0e-137">-SnapshotId</span></span>
<span data-ttu-id="56e0e-138">Utwórz wolumin na podstawie migawki.</span><span class="sxs-lookup"><span data-stu-id="56e0e-138">Create volume from a snapshot.</span></span> <span data-ttu-id="56e0e-139">Identyfikator UUID (wersja 4) lub identyfikator zasobu służący do identyfikowania migawki</span><span class="sxs-lookup"><span data-stu-id="56e0e-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="56e0e-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="56e0e-140">-SubnetId</span></span>
<span data-ttu-id="56e0e-141">Identyfikator URI zasobu platformy Azure dla delegowanej podsieci</span><span class="sxs-lookup"><span data-stu-id="56e0e-141">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="56e0e-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="56e0e-142">-Tag</span></span>
<span data-ttu-id="56e0e-143">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="56e0e-143">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="56e0e-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="56e0e-144">-UsageThreshold</span></span>
<span data-ttu-id="56e0e-145">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="56e0e-145">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="56e0e-146">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="56e0e-146">-VolumeType</span></span>
<span data-ttu-id="56e0e-147">Typ woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="56e0e-147">The type of the ANF volume</span></span>

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

### <span data-ttu-id="56e0e-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56e0e-148">-Confirm</span></span>
<span data-ttu-id="56e0e-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e0e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e0e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e0e-150">-WhatIf</span></span>
<span data-ttu-id="56e0e-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e0e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e0e-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56e0e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e0e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e0e-153">CommonParameters</span></span>
<span data-ttu-id="56e0e-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e0e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e0e-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56e0e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e0e-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56e0e-156">INPUTS</span></span>

### <span data-ttu-id="56e0e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="56e0e-157">System.String</span></span>

### <span data-ttu-id="56e0e-158">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="56e0e-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="56e0e-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56e0e-159">OUTPUTS</span></span>

### <span data-ttu-id="56e0e-160">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="56e0e-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="56e0e-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56e0e-161">NOTES</span></span>

## <span data-ttu-id="56e0e-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56e0e-162">RELATED LINKS</span></span>
