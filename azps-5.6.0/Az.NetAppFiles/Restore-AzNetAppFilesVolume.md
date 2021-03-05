---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 8c07b375214ef78f281bdfab2b31a94e0504b30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968241"
---
# <span data-ttu-id="c6071-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c6071-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c6071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6071-102">SYNOPSIS</span></span>
<span data-ttu-id="c6071-103">Przywracanie/przywracanie głośności do jednej z jego migawek</span><span class="sxs-lookup"><span data-stu-id="c6071-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="c6071-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6071-104">SYNTAX</span></span>

### <span data-ttu-id="c6071-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c6071-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6071-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6071-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6071-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6071-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6071-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6071-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6071-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6071-109">DESCRIPTION</span></span>
<span data-ttu-id="c6071-110">Przywracanie/przywracanie głośności migawki określonej w paramterze MigawkaD</span><span class="sxs-lookup"><span data-stu-id="c6071-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="c6071-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6071-111">EXAMPLES</span></span>

### <span data-ttu-id="c6071-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6071-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="c6071-113">To polecenie pozwala przywrócić/przywrócić głośność na stronie MyVolume do jednej z migawek za pomocą migawki 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="c6071-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="c6071-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6071-114">PARAMETERS</span></span>

### <span data-ttu-id="c6071-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6071-115">-AccountName</span></span>
<span data-ttu-id="c6071-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="c6071-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c6071-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6071-117">-DefaultProfile</span></span>
<span data-ttu-id="c6071-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6071-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6071-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6071-119">-InputObject</span></span>
<span data-ttu-id="c6071-120">Obiekt głośności do usunięcia</span><span class="sxs-lookup"><span data-stu-id="c6071-120">The volume object to remove</span></span>

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

### <span data-ttu-id="c6071-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c6071-121">-Name</span></span>
<span data-ttu-id="c6071-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="c6071-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="c6071-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6071-123">-PassThru</span></span>
<span data-ttu-id="c6071-124">Zwracanie, czy określona głośność została pomyślnie przywrócona/przywrócona</span><span class="sxs-lookup"><span data-stu-id="c6071-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="c6071-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c6071-125">-PoolName</span></span>
<span data-ttu-id="c6071-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="c6071-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c6071-127">- PoolObject</span><span class="sxs-lookup"><span data-stu-id="c6071-127">-PoolObject</span></span>
<span data-ttu-id="c6071-128">Obiekt puli zawierający wolumin do usunięcia</span><span class="sxs-lookup"><span data-stu-id="c6071-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="c6071-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6071-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6071-130">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="c6071-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="c6071-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6071-131">-ResourceId</span></span>
<span data-ttu-id="c6071-132">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="c6071-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="c6071-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="c6071-133">-SnapshotId</span></span>
<span data-ttu-id="c6071-134">MigawkaId migawki.</span><span class="sxs-lookup"><span data-stu-id="c6071-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="c6071-135">UUID w wersji 4 używanej do identyfikowania migawki</span><span class="sxs-lookup"><span data-stu-id="c6071-135">UUID v4 used to identify the Snapshot</span></span>

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

### <span data-ttu-id="c6071-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6071-136">-Confirm</span></span>
<span data-ttu-id="c6071-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6071-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6071-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6071-138">-WhatIf</span></span>
<span data-ttu-id="c6071-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6071-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6071-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c6071-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6071-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6071-141">CommonParameters</span></span>
<span data-ttu-id="c6071-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6071-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6071-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6071-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6071-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6071-144">INPUTS</span></span>

### <span data-ttu-id="c6071-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c6071-145">System.String</span></span>

### <span data-ttu-id="c6071-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c6071-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="c6071-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c6071-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c6071-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6071-148">OUTPUTS</span></span>

### <span data-ttu-id="c6071-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6071-149">System.Boolean</span></span>

## <span data-ttu-id="c6071-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6071-150">NOTES</span></span>

## <span data-ttu-id="c6071-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6071-151">RELATED LINKS</span></span>
