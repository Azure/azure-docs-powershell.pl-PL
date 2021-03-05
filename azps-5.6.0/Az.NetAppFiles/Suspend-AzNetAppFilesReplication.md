---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: 198ec8c67939c3ae01a52f2a9b06982ce8ee8d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968170"
---
# <span data-ttu-id="c0845-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="c0845-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="c0845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0845-102">SYNOPSIS</span></span>
<span data-ttu-id="c0845-103">Zawieszanie/przerwanie połączenia replikacji w woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="c0845-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="c0845-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0845-104">SYNTAX</span></span>

### <span data-ttu-id="c0845-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0845-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0845-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0845-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0845-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0845-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0845-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0845-108">DESCRIPTION</span></span>
<span data-ttu-id="c0845-109">Zawieszanie/przerwanie połączenia replikacji w woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="c0845-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="c0845-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0845-110">EXAMPLES</span></span>

### <span data-ttu-id="c0845-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0845-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="c0845-112">To polecenie zawiesza połączenie replikacji ANF na woluminie "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="c0845-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="c0845-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0845-113">PARAMETERS</span></span>

### <span data-ttu-id="c0845-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0845-114">-AccountName</span></span>
<span data-ttu-id="c0845-115">Nazwa konta ANF dla woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="c0845-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="c0845-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0845-116">-DefaultProfile</span></span>
<span data-ttu-id="c0845-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0845-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0845-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="c0845-118">-ForceBreak</span></span>
<span data-ttu-id="c0845-119">Jeśli replikacja jest w przesyłaniu stanu i chcesz wymusić przerwę replikacji, ustaw wartość True (Prawda)</span><span class="sxs-lookup"><span data-stu-id="c0845-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0845-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0845-120">-InputObject</span></span>
<span data-ttu-id="c0845-121">Obiekt woluminu docelowego ANF z przerwą replikacji</span><span class="sxs-lookup"><span data-stu-id="c0845-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="c0845-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0845-122">-Name</span></span>
<span data-ttu-id="c0845-123">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="c0845-123">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0845-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0845-124">-PassThru</span></span>
<span data-ttu-id="c0845-125">Zwracanie, czy wykonano podział określonej replikacji woluminu</span><span class="sxs-lookup"><span data-stu-id="c0845-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="c0845-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c0845-126">-PoolName</span></span>
<span data-ttu-id="c0845-127">Nazwa puli anfów dla woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="c0845-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="c0845-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0845-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0845-129">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="c0845-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c0845-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0845-130">-ResourceId</span></span>
<span data-ttu-id="c0845-131">Identyfikator zasobu woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="c0845-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c0845-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0845-132">-Confirm</span></span>
<span data-ttu-id="c0845-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0845-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0845-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0845-134">-WhatIf</span></span>
<span data-ttu-id="c0845-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0845-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0845-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0845-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0845-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0845-137">CommonParameters</span></span>
<span data-ttu-id="c0845-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0845-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0845-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0845-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0845-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0845-140">INPUTS</span></span>

### <span data-ttu-id="c0845-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c0845-141">System.String</span></span>

### <span data-ttu-id="c0845-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c0845-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c0845-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0845-143">OUTPUTS</span></span>

### <span data-ttu-id="c0845-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0845-144">System.Boolean</span></span>

## <span data-ttu-id="c0845-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0845-145">NOTES</span></span>

## <span data-ttu-id="c0845-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0845-146">RELATED LINKS</span></span>
