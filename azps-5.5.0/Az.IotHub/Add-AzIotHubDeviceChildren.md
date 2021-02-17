---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188259"
---
# <span data-ttu-id="cb07c-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="cb07c-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="cb07c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb07c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb07c-103">Dodaj urządzenia nie edge jako dzieci do urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="cb07c-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="cb07c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb07c-104">SYNTAX</span></span>

### <span data-ttu-id="cb07c-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="cb07c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb07c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb07c-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb07c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb07c-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb07c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb07c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb07c-109">Dodaj określoną listę rozdzieloną przecinkami identyfikatory urządzeń niebędące krawędzią jako dzieci określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="cb07c-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="cb07c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb07c-110">EXAMPLES</span></span>

### <span data-ttu-id="cb07c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb07c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="cb07c-112">Dodaj urządzenia nie edge jako dzieci do urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="cb07c-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="cb07c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cb07c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="cb07c-114">Niezależnie od tego, czy urządzenia nieo edge będą dodawać urządzenia nieo edge jako dzieci, niezależnie od tego, czy urządzenie bez krawędzi jest już urządzeniem podrzędnym innego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="cb07c-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="cb07c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb07c-115">PARAMETERS</span></span>

### <span data-ttu-id="cb07c-116">— Dzieci</span><span class="sxs-lookup"><span data-stu-id="cb07c-116">-Children</span></span>
<span data-ttu-id="cb07c-117">Lista urządzeń przenośnych (oddzielona przecinkami) obejmuje tylko urządzenia inne niż edge.</span><span class="sxs-lookup"><span data-stu-id="cb07c-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb07c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb07c-118">-DefaultProfile</span></span>
<span data-ttu-id="cb07c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb07c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb07c-120">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="cb07c-120">-DeviceId</span></span>
<span data-ttu-id="cb07c-121">Identyfikator urządzenia edge.</span><span class="sxs-lookup"><span data-stu-id="cb07c-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb07c-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cb07c-122">-Force</span></span>
<span data-ttu-id="cb07c-123">Zastępuje urządzenie nadrzędne urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="cb07c-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="cb07c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb07c-124">-InputObject</span></span>
<span data-ttu-id="cb07c-125">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="cb07c-125">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb07c-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cb07c-126">-IotHubName</span></span>
<span data-ttu-id="cb07c-127">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="cb07c-127">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb07c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb07c-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb07c-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cb07c-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb07c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb07c-130">-ResourceId</span></span>
<span data-ttu-id="cb07c-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="cb07c-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb07c-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb07c-132">-Confirm</span></span>
<span data-ttu-id="cb07c-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb07c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb07c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb07c-134">-WhatIf</span></span>
<span data-ttu-id="cb07c-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb07c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb07c-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb07c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb07c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb07c-137">CommonParameters</span></span>
<span data-ttu-id="cb07c-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb07c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb07c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb07c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb07c-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb07c-140">INPUTS</span></span>

### <span data-ttu-id="cb07c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cb07c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cb07c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cb07c-142">System.String</span></span>

## <span data-ttu-id="cb07c-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb07c-143">OUTPUTS</span></span>

### <span data-ttu-id="cb07c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDdyseksja</span><span class="sxs-lookup"><span data-stu-id="cb07c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="cb07c-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb07c-145">NOTES</span></span>

## <span data-ttu-id="cb07c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb07c-146">RELATED LINKS</span></span>
