---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188267"
---
# <span data-ttu-id="b8463-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b8463-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="b8463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8463-102">SYNOPSIS</span></span>
<span data-ttu-id="b8463-103">Utwórz urządzenie w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="b8463-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="b8463-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8463-104">SYNTAX</span></span>

### <span data-ttu-id="b8463-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8463-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8463-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8463-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8463-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8463-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8463-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8463-108">DESCRIPTION</span></span>
<span data-ttu-id="b8463-109">Utwórz urządzenie o innym typie autoryzacji w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="b8463-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="b8463-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8463-110">EXAMPLES</span></span>

### <span data-ttu-id="b8463-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8463-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="b8463-112">Utwórz urządzenie IoT z obsługą przeglądarki edge z domyślną autoryzacją (udostępniony klucz prywatny).</span><span class="sxs-lookup"><span data-stu-id="b8463-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="b8463-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b8463-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="b8463-114">Utwórz urządzenie IoT z autoryzacją głównego urzędu certyfikacji z wyłączonym stanem i przyczyną.</span><span class="sxs-lookup"><span data-stu-id="b8463-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="b8463-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b8463-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="b8463-116">Utwórz urządzenie IoT z obsługą krawędzi i dodaj do niego urządzenia podrzędne.</span><span class="sxs-lookup"><span data-stu-id="b8463-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="b8463-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b8463-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="b8463-118">Utwórz urządzenie IoT i ustaw jego urządzenie nadrzędne.</span><span class="sxs-lookup"><span data-stu-id="b8463-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="b8463-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8463-119">PARAMETERS</span></span>

### <span data-ttu-id="b8463-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="b8463-120">-AuthMethod</span></span>
<span data-ttu-id="b8463-121">Typ podmiotu autoryzacji, za pomocą który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="b8463-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8463-122">— Dzieci</span><span class="sxs-lookup"><span data-stu-id="b8463-122">-Children</span></span>
<span data-ttu-id="b8463-123">Lista dodaj urządzenia podrzędne (oddzielone przecinkami) obejmuje tylko urządzenia inne niż edge.</span><span class="sxs-lookup"><span data-stu-id="b8463-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="b8463-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8463-124">-DefaultProfile</span></span>
<span data-ttu-id="b8463-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8463-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8463-126">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="b8463-126">-DeviceId</span></span>
<span data-ttu-id="b8463-127">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="b8463-127">Target Device Id.</span></span>

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

### <span data-ttu-id="b8463-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="b8463-128">-EdgeEnabled</span></span>
<span data-ttu-id="b8463-129">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="b8463-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="b8463-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b8463-130">-Force</span></span>
<span data-ttu-id="b8463-131">Zastępuje urządzenie nadrzędne urządzenia bez krawędzi.</span><span class="sxs-lookup"><span data-stu-id="b8463-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="b8463-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8463-132">-InputObject</span></span>
<span data-ttu-id="b8463-133">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="b8463-133">IotHub object</span></span>

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

### <span data-ttu-id="b8463-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b8463-134">-IotHubName</span></span>
<span data-ttu-id="b8463-135">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="b8463-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b8463-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="b8463-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="b8463-137">Jawny własny podpis usb certyfikatu do użycia jako klucz podstawowy.</span><span class="sxs-lookup"><span data-stu-id="b8463-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8463-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="b8463-138">-ParentDeviceId</span></span>
<span data-ttu-id="b8463-139">Identyfikator urządzenia edge.</span><span class="sxs-lookup"><span data-stu-id="b8463-139">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8463-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8463-140">-ResourceGroupName</span></span>
<span data-ttu-id="b8463-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b8463-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b8463-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8463-142">-ResourceId</span></span>
<span data-ttu-id="b8463-143">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="b8463-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b8463-144">- SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="b8463-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="b8463-145">Jawne samopodpisywane wydrukowanie certyfikatu do użycia na kluczu pomocniczym.</span><span class="sxs-lookup"><span data-stu-id="b8463-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8463-146">— Status</span><span class="sxs-lookup"><span data-stu-id="b8463-146">-Status</span></span>
<span data-ttu-id="b8463-147">Ustawianie stanu urządzenia podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="b8463-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8463-148">- StatusReason</span><span class="sxs-lookup"><span data-stu-id="b8463-148">-StatusReason</span></span>
<span data-ttu-id="b8463-149">Opis stanu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="b8463-149">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8463-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8463-150">-Confirm</span></span>
<span data-ttu-id="b8463-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8463-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8463-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8463-152">-WhatIf</span></span>
<span data-ttu-id="b8463-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8463-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8463-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8463-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8463-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8463-155">CommonParameters</span></span>
<span data-ttu-id="b8463-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8463-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8463-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8463-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8463-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8463-158">INPUTS</span></span>

### <span data-ttu-id="b8463-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b8463-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b8463-160">System.String</span><span class="sxs-lookup"><span data-stu-id="b8463-160">System.String</span></span>

## <span data-ttu-id="b8463-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8463-161">OUTPUTS</span></span>

### <span data-ttu-id="b8463-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="b8463-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="b8463-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8463-163">NOTES</span></span>

## <span data-ttu-id="b8463-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8463-164">RELATED LINKS</span></span>
