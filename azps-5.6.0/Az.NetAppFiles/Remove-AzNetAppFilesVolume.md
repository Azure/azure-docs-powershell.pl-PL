---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f53ca76da23620a37020a14877059aae4f4c9808
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968266"
---
# <span data-ttu-id="d04a8-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d04a8-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d04a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d04a8-103">Usuwa wolumin usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="d04a8-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="d04a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d04a8-104">SYNTAX</span></span>

### <span data-ttu-id="d04a8-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d04a8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d04a8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d04a8-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d04a8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d04a8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d04a8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d04a8-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d04a8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d04a8-109">DESCRIPTION</span></span>
<span data-ttu-id="d04a8-110">Polecenie **cmdlet Remove-AzNetAppFilesVolume** usuwa wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="d04a8-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="d04a8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d04a8-111">EXAMPLES</span></span>

### <span data-ttu-id="d04a8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d04a8-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="d04a8-113">To polecenie usuwa wolumin ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="d04a8-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="d04a8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d04a8-114">PARAMETERS</span></span>

### <span data-ttu-id="d04a8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d04a8-115">-AccountName</span></span>
<span data-ttu-id="d04a8-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="d04a8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d04a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04a8-117">-DefaultProfile</span></span>
<span data-ttu-id="d04a8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d04a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04a8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d04a8-119">-InputObject</span></span>
<span data-ttu-id="d04a8-120">Obiekt głośności do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d04a8-120">The volume object to remove</span></span>

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

### <span data-ttu-id="d04a8-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d04a8-121">-Name</span></span>
<span data-ttu-id="d04a8-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d04a8-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d04a8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d04a8-123">-PassThru</span></span>
<span data-ttu-id="d04a8-124">Zwracanie, czy określona głośność została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="d04a8-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="d04a8-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d04a8-125">-PoolName</span></span>
<span data-ttu-id="d04a8-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="d04a8-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d04a8-127">- PoolObject</span><span class="sxs-lookup"><span data-stu-id="d04a8-127">-PoolObject</span></span>
<span data-ttu-id="d04a8-128">Obiekt puli zawierający wolumin do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d04a8-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="d04a8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04a8-129">-ResourceGroupName</span></span>
<span data-ttu-id="d04a8-130">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d04a8-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="d04a8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d04a8-131">-ResourceId</span></span>
<span data-ttu-id="d04a8-132">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d04a8-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="d04a8-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d04a8-133">-Confirm</span></span>
<span data-ttu-id="d04a8-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d04a8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d04a8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d04a8-135">-WhatIf</span></span>
<span data-ttu-id="d04a8-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d04a8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d04a8-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d04a8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d04a8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04a8-138">CommonParameters</span></span>
<span data-ttu-id="d04a8-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04a8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04a8-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d04a8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04a8-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d04a8-141">INPUTS</span></span>

### <span data-ttu-id="d04a8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d04a8-142">System.String</span></span>

### <span data-ttu-id="d04a8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d04a8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="d04a8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d04a8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d04a8-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d04a8-145">OUTPUTS</span></span>

### <span data-ttu-id="d04a8-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d04a8-146">System.Boolean</span></span>

## <span data-ttu-id="d04a8-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d04a8-147">NOTES</span></span>

## <span data-ttu-id="d04a8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d04a8-148">RELATED LINKS</span></span>
