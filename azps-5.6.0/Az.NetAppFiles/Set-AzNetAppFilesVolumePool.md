---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 2b3cf6588f32fd958073ced8d3347733416037ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968177"
---
# <span data-ttu-id="78944-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="78944-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="78944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78944-102">SYNOPSIS</span></span>
<span data-ttu-id="78944-103">Zmień pulę dla liczby plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="78944-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="78944-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78944-104">SYNTAX</span></span>

### <span data-ttu-id="78944-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="78944-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78944-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78944-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78944-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78944-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78944-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78944-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78944-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="78944-109">DESCRIPTION</span></span>
<span data-ttu-id="78944-110">Polecenie **cmdlet Set-AzNetAppFilesVolumePool** zmienia pulę woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="78944-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="78944-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78944-111">EXAMPLES</span></span>

### <span data-ttu-id="78944-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78944-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="78944-113">To zmieni pulę woluminu MyVolume na pulę o identyfikatorze 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="78944-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="78944-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78944-114">PARAMETERS</span></span>

### <span data-ttu-id="78944-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78944-115">-AccountName</span></span>
<span data-ttu-id="78944-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="78944-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="78944-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78944-117">-DefaultProfile</span></span>
<span data-ttu-id="78944-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78944-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78944-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78944-119">-InputObject</span></span>
<span data-ttu-id="78944-120">Obiekt głośności do przeniesienia</span><span class="sxs-lookup"><span data-stu-id="78944-120">The volume object to move</span></span>

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

### <span data-ttu-id="78944-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78944-121">-Name</span></span>
<span data-ttu-id="78944-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="78944-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="78944-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="78944-123">-NewPoolResourceId</span></span>
<span data-ttu-id="78944-124">ZasóbId puli pojemności, do która ma być przesunana.</span><span class="sxs-lookup"><span data-stu-id="78944-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="78944-125">UUID w wersji 4 używanej do identyfikowania puli</span><span class="sxs-lookup"><span data-stu-id="78944-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="78944-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="78944-126">-PoolName</span></span>
<span data-ttu-id="78944-127">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="78944-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="78944-128">- PoolObject</span><span class="sxs-lookup"><span data-stu-id="78944-128">-PoolObject</span></span>
<span data-ttu-id="78944-129">Obiekt puli zawierający wielkość</span><span class="sxs-lookup"><span data-stu-id="78944-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="78944-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78944-130">-ResourceGroupName</span></span>
<span data-ttu-id="78944-131">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="78944-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="78944-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78944-132">-ResourceId</span></span>
<span data-ttu-id="78944-133">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="78944-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="78944-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78944-134">-Confirm</span></span>
<span data-ttu-id="78944-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78944-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78944-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78944-136">-WhatIf</span></span>
<span data-ttu-id="78944-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78944-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78944-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="78944-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78944-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78944-139">CommonParameters</span></span>
<span data-ttu-id="78944-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78944-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78944-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78944-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78944-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78944-142">INPUTS</span></span>

### <span data-ttu-id="78944-143">System.String</span><span class="sxs-lookup"><span data-stu-id="78944-143">System.String</span></span>

### <span data-ttu-id="78944-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="78944-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="78944-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="78944-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="78944-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78944-146">OUTPUTS</span></span>

### <span data-ttu-id="78944-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78944-147">System.Boolean</span></span>

## <span data-ttu-id="78944-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78944-148">NOTES</span></span>

## <span data-ttu-id="78944-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78944-149">RELATED LINKS</span></span>
