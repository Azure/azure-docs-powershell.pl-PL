---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386561"
---
# <span data-ttu-id="9fe1f-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="9fe1f-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="9fe1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fe1f-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe1f-103">Zaktualizuj urządzenie z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="9fe1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fe1f-104">SYNTAX</span></span>

### <span data-ttu-id="9fe1f-105">ResourceSetForStatus (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9fe1f-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9fe1f-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="9fe1f-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fe1f-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9fe1f-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fe1f-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9fe1f-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="9fe1f-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe1f-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fe1f-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe1f-114">Opis</span><span class="sxs-lookup"><span data-stu-id="9fe1f-114">DESCRIPTION</span></span>
<span data-ttu-id="9fe1f-115">Zaktualizuj urządzenie z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="9fe1f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fe1f-116">EXAMPLES</span></span>

### <span data-ttu-id="9fe1f-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9fe1f-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="9fe1f-118">Włączanie funkcji krawędzi na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="9fe1f-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9fe1f-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="9fe1f-120">Wyłącz stan urządzenia.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-120">Disable device status.</span></span>

### <span data-ttu-id="9fe1f-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9fe1f-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="9fe1f-122">Aktualizowanie typu autoryzacji urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="9fe1f-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fe1f-123">PARAMETERS</span></span>

### <span data-ttu-id="9fe1f-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="9fe1f-124">-AuthMethod</span></span>
<span data-ttu-id="9fe1f-125">Typ autoryzacji, z którym ma zostać utworzony obiekt.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe1f-126">-DefaultProfile</span></span>
<span data-ttu-id="9fe1f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe1f-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9fe1f-128">-DeviceId</span></span>
<span data-ttu-id="9fe1f-129">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-129">Target Device Id.</span></span>

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

### <span data-ttu-id="9fe1f-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fe1f-130">-EdgeEnabled</span></span>
<span data-ttu-id="9fe1f-131">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9fe1f-132">-InputObject</span></span>
<span data-ttu-id="9fe1f-133">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="9fe1f-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9fe1f-134">-IotHubName</span></span>
<span data-ttu-id="9fe1f-135">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="9fe1f-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9fe1f-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="9fe1f-137">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza podstawowego.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe1f-138">-ResourceGroupName</span></span>
<span data-ttu-id="9fe1f-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9fe1f-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fe1f-140">-ResourceId</span></span>
<span data-ttu-id="9fe1f-141">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="9fe1f-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9fe1f-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="9fe1f-143">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-144">-Status</span><span class="sxs-lookup"><span data-stu-id="9fe1f-144">-Status</span></span>
<span data-ttu-id="9fe1f-145">Ustaw stan urządzenia podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="9fe1f-146">-StatusReason</span></span>
<span data-ttu-id="9fe1f-147">Opis statusu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe1f-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fe1f-148">-Confirm</span></span>
<span data-ttu-id="9fe1f-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe1f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe1f-150">-WhatIf</span></span>
<span data-ttu-id="9fe1f-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe1f-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe1f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe1f-153">CommonParameters</span></span>
<span data-ttu-id="9fe1f-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe1f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe1f-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe1f-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe1f-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fe1f-156">INPUTS</span></span>

### <span data-ttu-id="9fe1f-157">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9fe1f-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9fe1f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe1f-158">System.String</span></span>

## <span data-ttu-id="9fe1f-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fe1f-159">OUTPUTS</span></span>

### <span data-ttu-id="9fe1f-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="9fe1f-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="9fe1f-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fe1f-161">NOTES</span></span>

## <span data-ttu-id="9fe1f-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fe1f-162">RELATED LINKS</span></span>
