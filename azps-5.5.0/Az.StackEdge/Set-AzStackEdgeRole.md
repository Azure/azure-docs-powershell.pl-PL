---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190922"
---
# <span data-ttu-id="e93dc-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e93dc-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="e93dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e93dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e93dc-103">Aktualizacje roli dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="e93dc-103">Updates a Role for a device</span></span>

## <span data-ttu-id="e93dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e93dc-104">SYNTAX</span></span>

### <span data-ttu-id="e93dc-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e93dc-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93dc-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e93dc-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93dc-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e93dc-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93dc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e93dc-108">DESCRIPTION</span></span>
<span data-ttu-id="e93dc-109">Polecenie **cmdlet Set-AzStackEdgeRole** aktualizuje rolę IoT dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="e93dc-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="e93dc-110">Stare, montowane udziały zostaną zastąpione nowo dostarczonymi udziałami w parametrze ShareName.</span><span class="sxs-lookup"><span data-stu-id="e93dc-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="e93dc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e93dc-111">EXAMPLES</span></span>

### <span data-ttu-id="e93dc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e93dc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="e93dc-113">Nazwy udostępniania zastąpią stare, montowane udziały nowo dostarczonymi</span><span class="sxs-lookup"><span data-stu-id="e93dc-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="e93dc-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e93dc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="e93dc-115">Aby odjąć wszystkie udziały</span><span class="sxs-lookup"><span data-stu-id="e93dc-115">To unmount all shares</span></span>

## <span data-ttu-id="e93dc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e93dc-116">PARAMETERS</span></span>

### <span data-ttu-id="e93dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93dc-117">-DefaultProfile</span></span>
<span data-ttu-id="e93dc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e93dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e93dc-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e93dc-119">-DeviceName</span></span>
<span data-ttu-id="e93dc-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="e93dc-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e93dc-121">-InputObject</span></span>
<span data-ttu-id="e93dc-122">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="e93dc-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e93dc-123">-Name</span></span>
<span data-ttu-id="e93dc-124">Nazwa roli</span><span class="sxs-lookup"><span data-stu-id="e93dc-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="e93dc-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e93dc-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e93dc-127">-ResourceId</span></span>
<span data-ttu-id="e93dc-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e93dc-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e93dc-129">-ShareName</span></span>
<span data-ttu-id="e93dc-130">Udostępnianie roli</span><span class="sxs-lookup"><span data-stu-id="e93dc-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e93dc-131">-Confirm</span></span>
<span data-ttu-id="e93dc-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e93dc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93dc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93dc-133">-WhatIf</span></span>
<span data-ttu-id="e93dc-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93dc-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e93dc-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e93dc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93dc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93dc-136">CommonParameters</span></span>
<span data-ttu-id="e93dc-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e93dc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93dc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e93dc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93dc-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e93dc-139">INPUTS</span></span>

### <span data-ttu-id="e93dc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e93dc-140">System.String</span></span>

### <span data-ttu-id="e93dc-141">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e93dc-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="e93dc-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e93dc-142">OUTPUTS</span></span>

### <span data-ttu-id="e93dc-143">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e93dc-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="e93dc-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e93dc-144">NOTES</span></span>

## <span data-ttu-id="e93dc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e93dc-145">RELATED LINKS</span></span>
