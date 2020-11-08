---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052764"
---
# <span data-ttu-id="5d95b-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="5d95b-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="5d95b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d95b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d95b-103">Usuwanie urządzeń nienależących do brzegu jako dzieci z określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="5d95b-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="5d95b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d95b-104">SYNTAX</span></span>

### <span data-ttu-id="5d95b-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d95b-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d95b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d95b-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d95b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5d95b-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d95b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5d95b-108">DESCRIPTION</span></span>
<span data-ttu-id="5d95b-109">Usuwanie wszystkich lub wymienionych urządzeń nienależących do brzegu jako urządzeń podrzędnych określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="5d95b-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="5d95b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d95b-110">EXAMPLES</span></span>

### <span data-ttu-id="5d95b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d95b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="5d95b-112">Usuń wymienione urządzenia jako elementy podrzędne określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="5d95b-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="5d95b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5d95b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="5d95b-114">Usuwanie wszystkich urządzeń nienależących do brzegu jako urządzeń podrzędnych określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="5d95b-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="5d95b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d95b-115">PARAMETERS</span></span>

### <span data-ttu-id="5d95b-116">-Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="5d95b-116">-Children</span></span>
<span data-ttu-id="5d95b-117">Lista urządzeń podrzędnych (rozdzielana przecinkami) obejmuje tylko urządzenia niebędące krawędziami.</span><span class="sxs-lookup"><span data-stu-id="5d95b-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="5d95b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d95b-118">-DefaultProfile</span></span>
<span data-ttu-id="5d95b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d95b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d95b-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5d95b-120">-DeviceId</span></span>
<span data-ttu-id="5d95b-121">Identyfikator urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="5d95b-121">Id of edge device.</span></span>

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

### <span data-ttu-id="5d95b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d95b-122">-InputObject</span></span>
<span data-ttu-id="5d95b-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="5d95b-123">IotHub object</span></span>

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

### <span data-ttu-id="5d95b-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5d95b-124">-IotHubName</span></span>
<span data-ttu-id="5d95b-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5d95b-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5d95b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d95b-126">-PassThru</span></span>
<span data-ttu-id="5d95b-127">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="5d95b-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="5d95b-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5d95b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d95b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d95b-129">-ResourceGroupName</span></span>
<span data-ttu-id="5d95b-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d95b-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5d95b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d95b-131">-ResourceId</span></span>
<span data-ttu-id="5d95b-132">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="5d95b-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5d95b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d95b-133">-Confirm</span></span>
<span data-ttu-id="5d95b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d95b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d95b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d95b-135">-WhatIf</span></span>
<span data-ttu-id="5d95b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d95b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d95b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d95b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d95b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d95b-138">CommonParameters</span></span>
<span data-ttu-id="5d95b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d95b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d95b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d95b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d95b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d95b-141">INPUTS</span></span>

### <span data-ttu-id="5d95b-142">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5d95b-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5d95b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5d95b-143">System.String</span></span>

## <span data-ttu-id="5d95b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d95b-144">OUTPUTS</span></span>

### <span data-ttu-id="5d95b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d95b-145">System.Boolean</span></span>

## <span data-ttu-id="5d95b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d95b-146">NOTES</span></span>

## <span data-ttu-id="5d95b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d95b-147">RELATED LINKS</span></span>
