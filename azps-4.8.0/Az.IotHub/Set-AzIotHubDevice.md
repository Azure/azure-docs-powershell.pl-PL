---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064459"
---
# <span data-ttu-id="762e5-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="762e5-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="762e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="762e5-102">SYNOPSIS</span></span>
<span data-ttu-id="762e5-103">Zaktualizuj urządzenie z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="762e5-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="762e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="762e5-104">SYNTAX</span></span>

### <span data-ttu-id="762e5-105">ResourceSetForStatus (domyślny)</span><span class="sxs-lookup"><span data-stu-id="762e5-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="762e5-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="762e5-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="762e5-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="762e5-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="762e5-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="762e5-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="762e5-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="762e5-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762e5-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="762e5-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="762e5-114">Opis</span><span class="sxs-lookup"><span data-stu-id="762e5-114">DESCRIPTION</span></span>
<span data-ttu-id="762e5-115">Zaktualizuj urządzenie z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="762e5-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="762e5-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="762e5-116">EXAMPLES</span></span>

### <span data-ttu-id="762e5-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="762e5-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="762e5-118">Włączanie funkcji krawędzi na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="762e5-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="762e5-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="762e5-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="762e5-120">Wyłącz stan urządzenia.</span><span class="sxs-lookup"><span data-stu-id="762e5-120">Disable device status.</span></span>

### <span data-ttu-id="762e5-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="762e5-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="762e5-122">Aktualizowanie typu autoryzacji urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="762e5-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="762e5-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="762e5-123">PARAMETERS</span></span>

### <span data-ttu-id="762e5-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="762e5-124">-AuthMethod</span></span>
<span data-ttu-id="762e5-125">Typ autoryzacji, z którym ma zostać utworzony obiekt.</span><span class="sxs-lookup"><span data-stu-id="762e5-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="762e5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762e5-126">-DefaultProfile</span></span>
<span data-ttu-id="762e5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="762e5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="762e5-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="762e5-128">-DeviceId</span></span>
<span data-ttu-id="762e5-129">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="762e5-129">Target Device Id.</span></span>

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

### <span data-ttu-id="762e5-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="762e5-130">-EdgeEnabled</span></span>
<span data-ttu-id="762e5-131">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="762e5-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="762e5-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="762e5-132">-InputObject</span></span>
<span data-ttu-id="762e5-133">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="762e5-133">IotHub object</span></span>

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

### <span data-ttu-id="762e5-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="762e5-134">-IotHubName</span></span>
<span data-ttu-id="762e5-135">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="762e5-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="762e5-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="762e5-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="762e5-137">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza podstawowego.</span><span class="sxs-lookup"><span data-stu-id="762e5-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="762e5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762e5-138">-ResourceGroupName</span></span>
<span data-ttu-id="762e5-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="762e5-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="762e5-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="762e5-140">-ResourceId</span></span>
<span data-ttu-id="762e5-141">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="762e5-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="762e5-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="762e5-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="762e5-143">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="762e5-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="762e5-144">-Status</span><span class="sxs-lookup"><span data-stu-id="762e5-144">-Status</span></span>
<span data-ttu-id="762e5-145">Ustaw stan urządzenia podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="762e5-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="762e5-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="762e5-146">-StatusReason</span></span>
<span data-ttu-id="762e5-147">Opis statusu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="762e5-147">Description for device status.</span></span>

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

### <span data-ttu-id="762e5-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="762e5-148">-Confirm</span></span>
<span data-ttu-id="762e5-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762e5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762e5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762e5-150">-WhatIf</span></span>
<span data-ttu-id="762e5-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762e5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="762e5-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="762e5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="762e5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762e5-153">CommonParameters</span></span>
<span data-ttu-id="762e5-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762e5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762e5-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762e5-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762e5-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="762e5-156">INPUTS</span></span>

### <span data-ttu-id="762e5-157">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="762e5-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="762e5-158">System. String</span><span class="sxs-lookup"><span data-stu-id="762e5-158">System.String</span></span>

## <span data-ttu-id="762e5-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="762e5-159">OUTPUTS</span></span>

### <span data-ttu-id="762e5-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="762e5-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="762e5-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="762e5-161">NOTES</span></span>

## <span data-ttu-id="762e5-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="762e5-162">RELATED LINKS</span></span>
