---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 340adf5b3114750212ad1e2458159f48a9dae91f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968282"
---
# <span data-ttu-id="a6855-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6855-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a6855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6855-102">SYNOPSIS</span></span>
<span data-ttu-id="a6855-103">Usuwa migawkę plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="a6855-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="a6855-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6855-104">SYNTAX</span></span>

### <span data-ttu-id="a6855-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a6855-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6855-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6855-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6855-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6855-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6855-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6855-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6855-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6855-109">DESCRIPTION</span></span>
<span data-ttu-id="a6855-110">Polecenie **cmdlet Remove-AzNetAppFilesSnapshot** usuwa migawkę ANF.</span><span class="sxs-lookup"><span data-stu-id="a6855-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="a6855-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6855-111">EXAMPLES</span></span>

### <span data-ttu-id="a6855-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6855-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="a6855-113">To polecenie usuwa migawkę ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="a6855-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="a6855-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6855-114">PARAMETERS</span></span>

### <span data-ttu-id="a6855-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6855-115">-AccountName</span></span>
<span data-ttu-id="a6855-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="a6855-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a6855-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6855-117">-DefaultProfile</span></span>
<span data-ttu-id="a6855-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6855-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6855-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6855-119">-InputObject</span></span>
<span data-ttu-id="a6855-120">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a6855-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6855-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6855-121">-Name</span></span>
<span data-ttu-id="a6855-122">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="a6855-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6855-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6855-123">-PassThru</span></span>
<span data-ttu-id="a6855-124">Zwracanie, czy określona głośność została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="a6855-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="a6855-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a6855-125">-PoolName</span></span>
<span data-ttu-id="a6855-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="a6855-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a6855-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6855-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6855-128">Grupa zasobów migawki ANF</span><span class="sxs-lookup"><span data-stu-id="a6855-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="a6855-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6855-129">-ResourceId</span></span>
<span data-ttu-id="a6855-130">Identyfikator zasobu migawki ANF</span><span class="sxs-lookup"><span data-stu-id="a6855-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="a6855-131">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="a6855-131">-VolumeName</span></span>
<span data-ttu-id="a6855-132">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="a6855-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a6855-133">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="a6855-133">-VolumeObject</span></span>
<span data-ttu-id="a6855-134">Obiekt głośności zawierający migawkę do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a6855-134">The volume object containing the snapshot to remove</span></span>

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

### <span data-ttu-id="a6855-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6855-135">-Confirm</span></span>
<span data-ttu-id="a6855-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6855-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6855-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6855-137">-WhatIf</span></span>
<span data-ttu-id="a6855-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6855-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6855-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a6855-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6855-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6855-140">CommonParameters</span></span>
<span data-ttu-id="a6855-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6855-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6855-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6855-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6855-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6855-143">INPUTS</span></span>

### <span data-ttu-id="a6855-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a6855-144">System.String</span></span>

### <span data-ttu-id="a6855-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a6855-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="a6855-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6855-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a6855-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6855-147">OUTPUTS</span></span>

### <span data-ttu-id="a6855-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6855-148">System.Boolean</span></span>

## <span data-ttu-id="a6855-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6855-149">NOTES</span></span>

## <span data-ttu-id="a6855-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6855-150">RELATED LINKS</span></span>
