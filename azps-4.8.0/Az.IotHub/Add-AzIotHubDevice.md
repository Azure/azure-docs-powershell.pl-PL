---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220942"
---
# <span data-ttu-id="f5702-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5702-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="f5702-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5702-102">SYNOPSIS</span></span>
<span data-ttu-id="f5702-103">Utwórz urządzenie w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f5702-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="f5702-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5702-104">SYNTAX</span></span>

### <span data-ttu-id="f5702-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5702-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5702-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5702-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5702-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5702-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5702-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f5702-108">DESCRIPTION</span></span>
<span data-ttu-id="f5702-109">Utwórz urządzenie z innym typem autoryzacji w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f5702-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="f5702-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5702-110">EXAMPLES</span></span>

### <span data-ttu-id="f5702-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5702-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="f5702-112">Utwórz krawędź z włączonym urządzeniem IoT z opcją domyślna autoryzacja (udostępniony klucz prywatny).</span><span class="sxs-lookup"><span data-stu-id="f5702-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="f5702-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f5702-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="f5702-114">Utwórz urządzenie IoT z autoryzacją głównego urzędu certyfikacji z wyłączonym stanem i powodem.</span><span class="sxs-lookup"><span data-stu-id="f5702-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="f5702-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f5702-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="f5702-116">Utwórz krawędź z włączonym urządzeniem IoT i Dodaj do niego urządzenia podrzędne.</span><span class="sxs-lookup"><span data-stu-id="f5702-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="f5702-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f5702-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="f5702-118">Utwórz urządzenie IoT i ustaw jego urządzenie nadrzędne.</span><span class="sxs-lookup"><span data-stu-id="f5702-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="f5702-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5702-119">PARAMETERS</span></span>

### <span data-ttu-id="f5702-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="f5702-120">-AuthMethod</span></span>
<span data-ttu-id="f5702-121">Typ autoryzacji, z którym ma zostać utworzony obiekt.</span><span class="sxs-lookup"><span data-stu-id="f5702-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="f5702-122">-Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="f5702-122">-Children</span></span>
<span data-ttu-id="f5702-123">Lista Dodaj urządzenia podrzędne (oddzielone przecinkami) obejmuje tylko urządzenia niebędące krawędziami.</span><span class="sxs-lookup"><span data-stu-id="f5702-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="f5702-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5702-124">-DefaultProfile</span></span>
<span data-ttu-id="f5702-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5702-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5702-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f5702-126">-DeviceId</span></span>
<span data-ttu-id="f5702-127">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="f5702-127">Target Device Id.</span></span>

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

### <span data-ttu-id="f5702-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="f5702-128">-EdgeEnabled</span></span>
<span data-ttu-id="f5702-129">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="f5702-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="f5702-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f5702-130">-Force</span></span>
<span data-ttu-id="f5702-131">Zastępuje nadrzędne urządzenie, które nie jest na urządzeniu nadrzędnym.</span><span class="sxs-lookup"><span data-stu-id="f5702-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="f5702-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5702-132">-InputObject</span></span>
<span data-ttu-id="f5702-133">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="f5702-133">IotHub object</span></span>

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

### <span data-ttu-id="f5702-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f5702-134">-IotHubName</span></span>
<span data-ttu-id="f5702-135">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="f5702-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f5702-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="f5702-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="f5702-137">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza podstawowego.</span><span class="sxs-lookup"><span data-stu-id="f5702-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="f5702-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="f5702-138">-ParentDeviceId</span></span>
<span data-ttu-id="f5702-139">Identyfikator urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="f5702-139">Id of edge device.</span></span>

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

### <span data-ttu-id="f5702-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5702-140">-ResourceGroupName</span></span>
<span data-ttu-id="f5702-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f5702-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f5702-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5702-142">-ResourceId</span></span>
<span data-ttu-id="f5702-143">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="f5702-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f5702-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="f5702-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="f5702-145">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="f5702-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="f5702-146">-Status</span><span class="sxs-lookup"><span data-stu-id="f5702-146">-Status</span></span>
<span data-ttu-id="f5702-147">Ustaw stan urządzenia podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="f5702-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="f5702-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="f5702-148">-StatusReason</span></span>
<span data-ttu-id="f5702-149">Opis statusu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="f5702-149">Description for device status.</span></span>

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

### <span data-ttu-id="f5702-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5702-150">-Confirm</span></span>
<span data-ttu-id="f5702-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5702-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5702-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5702-152">-WhatIf</span></span>
<span data-ttu-id="f5702-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5702-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5702-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5702-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5702-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5702-155">CommonParameters</span></span>
<span data-ttu-id="f5702-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5702-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5702-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5702-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5702-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5702-158">INPUTS</span></span>

### <span data-ttu-id="f5702-159">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f5702-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f5702-160">System. String</span><span class="sxs-lookup"><span data-stu-id="f5702-160">System.String</span></span>

## <span data-ttu-id="f5702-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5702-161">OUTPUTS</span></span>

### <span data-ttu-id="f5702-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="f5702-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="f5702-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5702-163">NOTES</span></span>

## <span data-ttu-id="f5702-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5702-164">RELATED LINKS</span></span>
