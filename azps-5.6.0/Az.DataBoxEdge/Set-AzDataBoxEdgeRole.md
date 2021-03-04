---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: b712f52dac6a369c92f9cd3525460a1946ed5db5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971297"
---
# <span data-ttu-id="727fa-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="727fa-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="727fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="727fa-102">SYNOPSIS</span></span>
<span data-ttu-id="727fa-103">Aktualizacje roli dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="727fa-103">Updates a Role for a device</span></span>

## <span data-ttu-id="727fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="727fa-104">SYNTAX</span></span>

### <span data-ttu-id="727fa-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="727fa-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="727fa-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="727fa-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="727fa-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="727fa-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="727fa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="727fa-108">DESCRIPTION</span></span>
<span data-ttu-id="727fa-109">Polecenie **cmdlet Set-AzDataBoxEdgeRole** aktualizuje rolę IoT dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="727fa-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="727fa-110">Stare, montowane udziały zostaną zastąpione nowo dostarczonymi udziałami w parametrze ShareName.</span><span class="sxs-lookup"><span data-stu-id="727fa-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="727fa-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="727fa-111">EXAMPLES</span></span>

### <span data-ttu-id="727fa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="727fa-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="727fa-113">Nazwy udostępniania zastąpią stare, montowane udziały nowo dostarczonymi</span><span class="sxs-lookup"><span data-stu-id="727fa-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="727fa-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="727fa-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="727fa-115">Aby odjąć wszystkie udziały</span><span class="sxs-lookup"><span data-stu-id="727fa-115">To unmount all shares</span></span>

## <span data-ttu-id="727fa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="727fa-116">PARAMETERS</span></span>

### <span data-ttu-id="727fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="727fa-117">-DefaultProfile</span></span>
<span data-ttu-id="727fa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="727fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="727fa-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="727fa-119">-DeviceName</span></span>
<span data-ttu-id="727fa-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="727fa-120">Device Name</span></span>

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

### <span data-ttu-id="727fa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="727fa-121">-InputObject</span></span>
<span data-ttu-id="727fa-122">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="727fa-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="727fa-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="727fa-123">-Name</span></span>
<span data-ttu-id="727fa-124">Nazwa roli</span><span class="sxs-lookup"><span data-stu-id="727fa-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="727fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="727fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="727fa-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="727fa-126">Resource Group Name</span></span>

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

### <span data-ttu-id="727fa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="727fa-127">-ResourceId</span></span>
<span data-ttu-id="727fa-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="727fa-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="727fa-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="727fa-129">-ShareName</span></span>
<span data-ttu-id="727fa-130">Udostępnianie roli</span><span class="sxs-lookup"><span data-stu-id="727fa-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727fa-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="727fa-131">-Confirm</span></span>
<span data-ttu-id="727fa-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="727fa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="727fa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="727fa-133">-WhatIf</span></span>
<span data-ttu-id="727fa-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="727fa-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="727fa-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="727fa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="727fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727fa-136">CommonParameters</span></span>
<span data-ttu-id="727fa-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="727fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727fa-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="727fa-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727fa-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="727fa-139">INPUTS</span></span>

### <span data-ttu-id="727fa-140">System.String</span><span class="sxs-lookup"><span data-stu-id="727fa-140">System.String</span></span>

### <span data-ttu-id="727fa-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="727fa-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="727fa-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="727fa-142">OUTPUTS</span></span>

### <span data-ttu-id="727fa-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="727fa-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="727fa-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="727fa-144">NOTES</span></span>

## <span data-ttu-id="727fa-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="727fa-145">RELATED LINKS</span></span>
