---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222170"
---
# <span data-ttu-id="8ac31-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8ac31-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="8ac31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ac31-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac31-103">Aktualizowanie roli urządzenia</span><span class="sxs-lookup"><span data-stu-id="8ac31-103">Updates a Role for a device</span></span>

## <span data-ttu-id="8ac31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ac31-104">SYNTAX</span></span>

### <span data-ttu-id="8ac31-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ac31-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac31-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ac31-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac31-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ac31-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ac31-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ac31-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac31-109">Polecenie cmdlet **Set-AzStackEdgeRole** aktualizuje rolę IoT dla urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="8ac31-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="8ac31-110">Stare udziały zainstalowane zostaną zastąpione nowo udostępnionym parametrem nazwa_udziału.</span><span class="sxs-lookup"><span data-stu-id="8ac31-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="8ac31-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ac31-111">EXAMPLES</span></span>

### <span data-ttu-id="8ac31-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ac31-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="8ac31-113">Nazwa udziału spowoduje zastąpienie starych udziałów instalowanych nowo dostarczonymi</span><span class="sxs-lookup"><span data-stu-id="8ac31-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="8ac31-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8ac31-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="8ac31-115">Aby odinstalować wszystkie udziały</span><span class="sxs-lookup"><span data-stu-id="8ac31-115">To unmount all shares</span></span>

## <span data-ttu-id="8ac31-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ac31-116">PARAMETERS</span></span>

### <span data-ttu-id="8ac31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac31-117">-DefaultProfile</span></span>
<span data-ttu-id="8ac31-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac31-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8ac31-119">-DeviceName</span></span>
<span data-ttu-id="8ac31-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="8ac31-120">Device Name</span></span>

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

### <span data-ttu-id="8ac31-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ac31-121">-InputObject</span></span>
<span data-ttu-id="8ac31-122">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="8ac31-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8ac31-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ac31-123">-Name</span></span>
<span data-ttu-id="8ac31-124">Nazwa roli</span><span class="sxs-lookup"><span data-stu-id="8ac31-124">Name of the Role</span></span>

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

### <span data-ttu-id="8ac31-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac31-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ac31-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8ac31-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8ac31-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac31-127">-ResourceId</span></span>
<span data-ttu-id="8ac31-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8ac31-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8ac31-129">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="8ac31-129">-ShareName</span></span>
<span data-ttu-id="8ac31-130">Udostępnianie w roli</span><span class="sxs-lookup"><span data-stu-id="8ac31-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="8ac31-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ac31-131">-Confirm</span></span>
<span data-ttu-id="8ac31-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac31-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac31-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac31-133">-WhatIf</span></span>
<span data-ttu-id="8ac31-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac31-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ac31-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ac31-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac31-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac31-136">CommonParameters</span></span>
<span data-ttu-id="8ac31-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac31-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac31-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ac31-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac31-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac31-139">INPUTS</span></span>

### <span data-ttu-id="8ac31-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac31-140">System.String</span></span>

### <span data-ttu-id="8ac31-141">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8ac31-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="8ac31-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ac31-142">OUTPUTS</span></span>

### <span data-ttu-id="8ac31-143">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8ac31-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="8ac31-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ac31-144">NOTES</span></span>

## <span data-ttu-id="8ac31-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac31-145">RELATED LINKS</span></span>
