---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 4087725afbf845e42c2a00952a818f5eb356d421
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968298"
---
# <span data-ttu-id="1c19f-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="1c19f-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="1c19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c19f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c19f-103">Usuwanie/usuwanie połączenia replikacji w woluminie docelowym i wysyłanie zwolnienia do replikacji źródła</span><span class="sxs-lookup"><span data-stu-id="1c19f-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="1c19f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c19f-104">SYNTAX</span></span>

### <span data-ttu-id="1c19f-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1c19f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c19f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c19f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c19f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c19f-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c19f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c19f-108">DESCRIPTION</span></span>
<span data-ttu-id="1c19f-109">Usuwanie/usuwanie połączenia replikacji w woluminie docelowym i wysyłanie zwolnienia do replikacji źródła</span><span class="sxs-lookup"><span data-stu-id="1c19f-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="1c19f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c19f-110">EXAMPLES</span></span>

### <span data-ttu-id="1c19f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c19f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="1c19f-112">To polecenie usuwa połączenie replikacji ANF dla woluminu "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="1c19f-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="1c19f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c19f-113">PARAMETERS</span></span>

### <span data-ttu-id="1c19f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c19f-114">-AccountName</span></span>
<span data-ttu-id="1c19f-115">Nazwa konta ANF dla woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1c19f-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="1c19f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c19f-116">-DefaultProfile</span></span>
<span data-ttu-id="1c19f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c19f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c19f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c19f-118">-InputObject</span></span>
<span data-ttu-id="1c19f-119">Głośność miejsca docelowego ANF z replikacją do usunięcia</span><span class="sxs-lookup"><span data-stu-id="1c19f-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="1c19f-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1c19f-120">-Name</span></span>
<span data-ttu-id="1c19f-121">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1c19f-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1c19f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c19f-122">-PassThru</span></span>
<span data-ttu-id="1c19f-123">Zwracanie, czy określona replikacja ANF została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="1c19f-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="1c19f-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1c19f-124">-PoolName</span></span>
<span data-ttu-id="1c19f-125">Nazwa puli anfów dla woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1c19f-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="1c19f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c19f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c19f-127">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1c19f-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1c19f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c19f-128">-ResourceId</span></span>
<span data-ttu-id="1c19f-129">Identyfikator zasobu woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1c19f-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1c19f-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c19f-130">-Confirm</span></span>
<span data-ttu-id="1c19f-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1c19f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c19f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c19f-132">-WhatIf</span></span>
<span data-ttu-id="1c19f-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c19f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c19f-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1c19f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c19f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c19f-135">CommonParameters</span></span>
<span data-ttu-id="1c19f-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c19f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c19f-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c19f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c19f-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c19f-138">INPUTS</span></span>

### <span data-ttu-id="1c19f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1c19f-139">System.String</span></span>

### <span data-ttu-id="1c19f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1c19f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1c19f-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c19f-141">OUTPUTS</span></span>

### <span data-ttu-id="1c19f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c19f-142">System.Boolean</span></span>

## <span data-ttu-id="1c19f-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c19f-143">NOTES</span></span>

## <span data-ttu-id="1c19f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c19f-144">RELATED LINKS</span></span>
