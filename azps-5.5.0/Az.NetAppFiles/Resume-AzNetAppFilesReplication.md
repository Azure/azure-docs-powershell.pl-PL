---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241138"
---
# <span data-ttu-id="1771d-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="1771d-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="1771d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1771d-102">SYNOPSIS</span></span>
<span data-ttu-id="1771d-103">Wznów/zsynchronizuj połączenie z woluminem docelowym.</span><span class="sxs-lookup"><span data-stu-id="1771d-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="1771d-104">Jeśli operacja zostanie uruchomiono w woluminie źródłowym, spowoduje to odwrócenie połączenia i zsynchronizowanie go ze źródłem do miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="1771d-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="1771d-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1771d-105">SYNTAX</span></span>

### <span data-ttu-id="1771d-106">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1771d-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1771d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1771d-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1771d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1771d-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1771d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1771d-109">DESCRIPTION</span></span>
<span data-ttu-id="1771d-110">Wznawianie/ponowne synchronizacja połączenia woluminu docelowego</span><span class="sxs-lookup"><span data-stu-id="1771d-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="1771d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1771d-111">EXAMPLES</span></span>

### <span data-ttu-id="1771d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1771d-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="1771d-113">To polecenie wznawia połączenie replikacji ANF dla woluminu "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="1771d-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="1771d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1771d-114">PARAMETERS</span></span>

### <span data-ttu-id="1771d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1771d-115">-AccountName</span></span>
<span data-ttu-id="1771d-116">Nazwa konta ANF dla woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1771d-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="1771d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1771d-117">-DefaultProfile</span></span>
<span data-ttu-id="1771d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1771d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1771d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1771d-119">-InputObject</span></span>
<span data-ttu-id="1771d-120">Obiekt obrotu miejsca docelowego replikacji ANF do ponownej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="1771d-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="1771d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1771d-121">-Name</span></span>
<span data-ttu-id="1771d-122">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1771d-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1771d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1771d-123">-PassThru</span></span>
<span data-ttu-id="1771d-124">Zwracanie, czy wykonano ponowną synchronizację określonego woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1771d-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="1771d-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1771d-125">-PoolName</span></span>
<span data-ttu-id="1771d-126">Nazwa puli anfów dla woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1771d-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="1771d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1771d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1771d-128">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1771d-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1771d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1771d-129">-ResourceId</span></span>
<span data-ttu-id="1771d-130">Identyfikator zasobu woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1771d-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1771d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1771d-131">-Confirm</span></span>
<span data-ttu-id="1771d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1771d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1771d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1771d-133">-WhatIf</span></span>
<span data-ttu-id="1771d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1771d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1771d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1771d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1771d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1771d-136">CommonParameters</span></span>
<span data-ttu-id="1771d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1771d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1771d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1771d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1771d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1771d-139">INPUTS</span></span>

### <span data-ttu-id="1771d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1771d-140">System.String</span></span>

### <span data-ttu-id="1771d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1771d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1771d-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1771d-142">OUTPUTS</span></span>

### <span data-ttu-id="1771d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1771d-143">System.Boolean</span></span>

## <span data-ttu-id="1771d-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1771d-144">NOTES</span></span>

## <span data-ttu-id="1771d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1771d-145">RELATED LINKS</span></span>
