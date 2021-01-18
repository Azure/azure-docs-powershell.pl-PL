---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503436"
---
# <span data-ttu-id="a2816-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a2816-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="a2816-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2816-102">SYNOPSIS</span></span>
<span data-ttu-id="a2816-103">Dodaj urządzenia niebędące krawędziami jako elementy podrzędne do urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="a2816-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="a2816-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2816-104">SYNTAX</span></span>

### <span data-ttu-id="a2816-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2816-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2816-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2816-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2816-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2816-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2816-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2816-108">DESCRIPTION</span></span>
<span data-ttu-id="a2816-109">Dodaj określoną listę rozdzielaną przecinkami niegranicznych identyfikatorów urządzeń jako elementy podrzędne określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="a2816-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="a2816-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2816-110">EXAMPLES</span></span>

### <span data-ttu-id="a2816-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2816-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="a2816-112">Dodaj urządzenia niebędące krawędziami jako elementy podrzędne do urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="a2816-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="a2816-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2816-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="a2816-114">Dodaj urządzenia niebędące krawędziami jako elementy podrzędne do urządzenia brzegowego irrespectively urządzenie, które nie jest krawędzią, jest już elementem podrzędnym innego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="a2816-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="a2816-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2816-115">PARAMETERS</span></span>

### <span data-ttu-id="a2816-116">-Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="a2816-116">-Children</span></span>
<span data-ttu-id="a2816-117">Lista urządzeń podrzędnych (rozdzielana przecinkami) obejmuje tylko urządzenia niebędące krawędziami.</span><span class="sxs-lookup"><span data-stu-id="a2816-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="a2816-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2816-118">-DefaultProfile</span></span>
<span data-ttu-id="a2816-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2816-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2816-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a2816-120">-DeviceId</span></span>
<span data-ttu-id="a2816-121">Identyfikator urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="a2816-121">Id of edge device.</span></span>

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

### <span data-ttu-id="a2816-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a2816-122">-Force</span></span>
<span data-ttu-id="a2816-123">Zastępuje nadrzędne urządzenie, które nie jest na urządzeniu nadrzędnym.</span><span class="sxs-lookup"><span data-stu-id="a2816-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="a2816-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2816-124">-InputObject</span></span>
<span data-ttu-id="a2816-125">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="a2816-125">IotHub object</span></span>

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

### <span data-ttu-id="a2816-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a2816-126">-IotHubName</span></span>
<span data-ttu-id="a2816-127">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="a2816-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a2816-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2816-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2816-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a2816-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a2816-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2816-130">-ResourceId</span></span>
<span data-ttu-id="a2816-131">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="a2816-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a2816-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2816-132">-Confirm</span></span>
<span data-ttu-id="a2816-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2816-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2816-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2816-134">-WhatIf</span></span>
<span data-ttu-id="a2816-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2816-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2816-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2816-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2816-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2816-137">CommonParameters</span></span>
<span data-ttu-id="a2816-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2816-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2816-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2816-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2816-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2816-140">INPUTS</span></span>

### <span data-ttu-id="a2816-141">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a2816-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a2816-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a2816-142">System.String</span></span>

## <span data-ttu-id="a2816-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2816-143">OUTPUTS</span></span>

### <span data-ttu-id="a2816-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a2816-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="a2816-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2816-145">NOTES</span></span>

## <span data-ttu-id="a2816-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2816-146">RELATED LINKS</span></span>
