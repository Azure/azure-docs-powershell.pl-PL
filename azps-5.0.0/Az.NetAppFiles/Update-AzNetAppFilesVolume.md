---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232853"
---
# <span data-ttu-id="728e2-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="728e2-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="728e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="728e2-102">SYNOPSIS</span></span>
<span data-ttu-id="728e2-103">Aktualizuje wolumin pliki usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="728e2-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="728e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="728e2-104">SYNTAX</span></span>

### <span data-ttu-id="728e2-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="728e2-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728e2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="728e2-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728e2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="728e2-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728e2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="728e2-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728e2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="728e2-109">DESCRIPTION</span></span>
<span data-ttu-id="728e2-110">Polecenie cmdlet **Update-AzNetAppFilesVolume** AKTUALIZUJE wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="728e2-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="728e2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="728e2-111">EXAMPLES</span></span>

### <span data-ttu-id="728e2-112">Przykład 1: aktualizowanie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="728e2-113">To polecenie aktualizuje wolumin ANF "MyAnfVolume" przy użyciu nowego rozmiaru UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="728e2-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="728e2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="728e2-114">PARAMETERS</span></span>

### <span data-ttu-id="728e2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="728e2-115">-AccountName</span></span>
<span data-ttu-id="728e2-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="728e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728e2-117">-DefaultProfile</span></span>
<span data-ttu-id="728e2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="728e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="728e2-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="728e2-119">-ExportPolicy</span></span>
<span data-ttu-id="728e2-120">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="728e2-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="728e2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="728e2-121">-InputObject</span></span>
<span data-ttu-id="728e2-122">Obiekt woluminu do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="728e2-122">The volume object to update</span></span>

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

### <span data-ttu-id="728e2-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="728e2-123">-Location</span></span>
<span data-ttu-id="728e2-124">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="728e2-124">The location of the resource</span></span>

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

### <span data-ttu-id="728e2-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="728e2-125">-Name</span></span>
<span data-ttu-id="728e2-126">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-126">The name of the ANF volume</span></span>

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

### <span data-ttu-id="728e2-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="728e2-127">-PoolName</span></span>
<span data-ttu-id="728e2-128">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="728e2-129">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="728e2-129">-PoolObject</span></span>
<span data-ttu-id="728e2-130">Obiekt Pool zawierający wolumin do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="728e2-130">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="728e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="728e2-132">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="728e2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="728e2-133">-ResourceId</span></span>
<span data-ttu-id="728e2-134">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="728e2-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="728e2-135">-ServiceLevel</span></span>
<span data-ttu-id="728e2-136">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="728e2-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="728e2-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="728e2-137">-Tag</span></span>
<span data-ttu-id="728e2-138">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="728e2-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="728e2-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="728e2-139">-UsageThreshold</span></span>
<span data-ttu-id="728e2-140">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="728e2-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="728e2-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="728e2-141">-Confirm</span></span>
<span data-ttu-id="728e2-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="728e2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728e2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728e2-143">-WhatIf</span></span>
<span data-ttu-id="728e2-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="728e2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728e2-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="728e2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728e2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728e2-146">CommonParameters</span></span>
<span data-ttu-id="728e2-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728e2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728e2-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="728e2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728e2-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="728e2-149">INPUTS</span></span>

### <span data-ttu-id="728e2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="728e2-150">System.String</span></span>

### <span data-ttu-id="728e2-151">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="728e2-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="728e2-152">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="728e2-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="728e2-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="728e2-153">OUTPUTS</span></span>

### <span data-ttu-id="728e2-154">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="728e2-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="728e2-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="728e2-155">NOTES</span></span>

## <span data-ttu-id="728e2-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="728e2-156">RELATED LINKS</span></span>
