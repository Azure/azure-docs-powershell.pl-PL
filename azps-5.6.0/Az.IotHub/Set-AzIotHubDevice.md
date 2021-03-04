---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: c164286e71b198ab19dd1928d6ee495014295306
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955866"
---
# <span data-ttu-id="6efe3-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6efe3-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="6efe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6efe3-102">SYNOPSIS</span></span>
<span data-ttu-id="6efe3-103">Zaktualizuj urządzenie Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6efe3-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="6efe3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6efe3-104">SYNTAX</span></span>

### <span data-ttu-id="6efe3-105">ResourceSetForStatus (Default)</span><span class="sxs-lookup"><span data-stu-id="6efe3-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="6efe3-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="6efe3-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6efe3-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="6efe3-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6efe3-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6efe3-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="6efe3-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="6efe3-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe3-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6efe3-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6efe3-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="6efe3-114">DESCRIPTION</span></span>
<span data-ttu-id="6efe3-115">Zaktualizuj urządzenie Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6efe3-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="6efe3-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6efe3-116">EXAMPLES</span></span>

### <span data-ttu-id="6efe3-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6efe3-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="6efe3-118">Włącz funkcje brzegowe dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6efe3-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="6efe3-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6efe3-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="6efe3-120">Wyłącz stan urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6efe3-120">Disable device status.</span></span>

### <span data-ttu-id="6efe3-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6efe3-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="6efe3-122">Aktualizowanie typu autoryzacji urządzenia Centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="6efe3-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="6efe3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6efe3-123">PARAMETERS</span></span>

### <span data-ttu-id="6efe3-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="6efe3-124">-AuthMethod</span></span>
<span data-ttu-id="6efe3-125">Typ podmiotu autoryzacji, za pomocą który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="6efe3-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="6efe3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efe3-126">-DefaultProfile</span></span>
<span data-ttu-id="6efe3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6efe3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6efe3-128">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="6efe3-128">-DeviceId</span></span>
<span data-ttu-id="6efe3-129">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="6efe3-129">Target Device Id.</span></span>

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

### <span data-ttu-id="6efe3-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6efe3-130">-EdgeEnabled</span></span>
<span data-ttu-id="6efe3-131">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="6efe3-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="6efe3-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6efe3-132">-InputObject</span></span>
<span data-ttu-id="6efe3-133">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="6efe3-133">IotHub object</span></span>

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

### <span data-ttu-id="6efe3-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6efe3-134">-IotHubName</span></span>
<span data-ttu-id="6efe3-135">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="6efe3-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6efe3-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6efe3-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="6efe3-137">Jawny własny podpis usb certyfikatu do użycia jako klucz podstawowy.</span><span class="sxs-lookup"><span data-stu-id="6efe3-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="6efe3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6efe3-138">-ResourceGroupName</span></span>
<span data-ttu-id="6efe3-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6efe3-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6efe3-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6efe3-140">-ResourceId</span></span>
<span data-ttu-id="6efe3-141">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="6efe3-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6efe3-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6efe3-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="6efe3-143">Jawny samopodpisywanego certyfikatu thumbprint do użycia w przypadku klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="6efe3-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="6efe3-144">— Status</span><span class="sxs-lookup"><span data-stu-id="6efe3-144">-Status</span></span>
<span data-ttu-id="6efe3-145">Ustawianie stanu urządzenia podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="6efe3-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="6efe3-146">- StatusReason</span><span class="sxs-lookup"><span data-stu-id="6efe3-146">-StatusReason</span></span>
<span data-ttu-id="6efe3-147">Opis stanu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6efe3-147">Description for device status.</span></span>

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

### <span data-ttu-id="6efe3-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6efe3-148">-Confirm</span></span>
<span data-ttu-id="6efe3-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6efe3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6efe3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6efe3-150">-WhatIf</span></span>
<span data-ttu-id="6efe3-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6efe3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6efe3-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6efe3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6efe3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efe3-153">CommonParameters</span></span>
<span data-ttu-id="6efe3-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efe3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efe3-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efe3-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efe3-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6efe3-156">INPUTS</span></span>

### <span data-ttu-id="6efe3-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6efe3-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6efe3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="6efe3-158">System.String</span></span>

## <span data-ttu-id="6efe3-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6efe3-159">OUTPUTS</span></span>

### <span data-ttu-id="6efe3-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="6efe3-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="6efe3-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6efe3-161">NOTES</span></span>

## <span data-ttu-id="6efe3-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6efe3-162">RELATED LINKS</span></span>
