---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 296793309dbcae7317353e41f9f3562a020c9be2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013009"
---
# <span data-ttu-id="aa058-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="aa058-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="aa058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa058-102">SYNOPSIS</span></span>
<span data-ttu-id="aa058-103">Usuń urządzenia inne niż krawędzie jako dzieci z określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="aa058-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="aa058-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa058-104">SYNTAX</span></span>

### <span data-ttu-id="aa058-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa058-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa058-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa058-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa058-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa058-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa058-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa058-108">DESCRIPTION</span></span>
<span data-ttu-id="aa058-109">Usuń wszystkie lub wymienione urządzenia nie edge jako urządzenia brzegowe określone przez dzieci.</span><span class="sxs-lookup"><span data-stu-id="aa058-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="aa058-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa058-110">EXAMPLES</span></span>

### <span data-ttu-id="aa058-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa058-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="aa058-112">Usuń wymienione urządzenia jako dzieci określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="aa058-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="aa058-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="aa058-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="aa058-114">Usuń wszystkie urządzenia nieo edge jako urządzenia brzegowe określone przez dzieci.</span><span class="sxs-lookup"><span data-stu-id="aa058-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="aa058-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa058-115">PARAMETERS</span></span>

### <span data-ttu-id="aa058-116">— Dzieci</span><span class="sxs-lookup"><span data-stu-id="aa058-116">-Children</span></span>
<span data-ttu-id="aa058-117">Lista urządzeń przenośnych (oddzielona przecinkami) obejmuje tylko urządzenia inne niż brzegowe.</span><span class="sxs-lookup"><span data-stu-id="aa058-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa058-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa058-118">-DefaultProfile</span></span>
<span data-ttu-id="aa058-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa058-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa058-120">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="aa058-120">-DeviceId</span></span>
<span data-ttu-id="aa058-121">Identyfikator urządzenia edge.</span><span class="sxs-lookup"><span data-stu-id="aa058-121">Id of edge device.</span></span>

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

### <span data-ttu-id="aa058-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa058-122">-InputObject</span></span>
<span data-ttu-id="aa058-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="aa058-123">IotHub object</span></span>

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

### <span data-ttu-id="aa058-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="aa058-124">-IotHubName</span></span>
<span data-ttu-id="aa058-125">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="aa058-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aa058-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa058-126">-PassThru</span></span>
<span data-ttu-id="aa058-127">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="aa058-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="aa058-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="aa058-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa058-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa058-129">-ResourceGroupName</span></span>
<span data-ttu-id="aa058-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa058-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aa058-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa058-131">-ResourceId</span></span>
<span data-ttu-id="aa058-132">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="aa058-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aa058-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa058-133">-Confirm</span></span>
<span data-ttu-id="aa058-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa058-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa058-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa058-135">-WhatIf</span></span>
<span data-ttu-id="aa058-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa058-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa058-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa058-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa058-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa058-138">CommonParameters</span></span>
<span data-ttu-id="aa058-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa058-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa058-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa058-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa058-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa058-141">INPUTS</span></span>

### <span data-ttu-id="aa058-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="aa058-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aa058-143">System.String</span><span class="sxs-lookup"><span data-stu-id="aa058-143">System.String</span></span>

## <span data-ttu-id="aa058-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa058-144">OUTPUTS</span></span>

### <span data-ttu-id="aa058-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa058-145">System.Boolean</span></span>

## <span data-ttu-id="aa058-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa058-146">NOTES</span></span>

## <span data-ttu-id="aa058-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa058-147">RELATED LINKS</span></span>
