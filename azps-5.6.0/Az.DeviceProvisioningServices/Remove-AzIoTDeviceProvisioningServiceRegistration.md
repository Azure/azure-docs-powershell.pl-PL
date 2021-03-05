---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: f72aa2ab648de33baaf50e181afa98e12ac921a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985132"
---
# <span data-ttu-id="02dd7-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="02dd7-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="02dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="02dd7-103">Usuwa rejestrację urządzenia.</span><span class="sxs-lookup"><span data-stu-id="02dd7-103">Deletes the device registration.</span></span>

## <span data-ttu-id="02dd7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02dd7-104">SYNTAX</span></span>

### <span data-ttu-id="02dd7-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02dd7-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02dd7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="02dd7-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02dd7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="02dd7-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02dd7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="02dd7-108">DESCRIPTION</span></span>
<span data-ttu-id="02dd7-109">Usuń rejestrację urządzeń w usłudze inicjowania obsługi urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="02dd7-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="02dd7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="02dd7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02dd7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="02dd7-112">Usuń rejestrację urządzeń w usłudze inicjowania obsługi urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="02dd7-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="02dd7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02dd7-113">PARAMETERS</span></span>

### <span data-ttu-id="02dd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02dd7-114">-DefaultProfile</span></span>
<span data-ttu-id="02dd7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02dd7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02dd7-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="02dd7-116">-DpsName</span></span>
<span data-ttu-id="02dd7-117">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="02dd7-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="02dd7-118">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="02dd7-118">-DpsObject</span></span>
<span data-ttu-id="02dd7-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="02dd7-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02dd7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02dd7-120">-PassThru</span></span>
<span data-ttu-id="02dd7-121">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="02dd7-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="02dd7-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="02dd7-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02dd7-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="02dd7-123">-RegistrationId</span></span>
<span data-ttu-id="02dd7-124">Identyfikator rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="02dd7-124">ID of device registration.</span></span>

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

### <span data-ttu-id="02dd7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02dd7-125">-ResourceGroupName</span></span>
<span data-ttu-id="02dd7-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="02dd7-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="02dd7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02dd7-127">-ResourceId</span></span>
<span data-ttu-id="02dd7-128">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="02dd7-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="02dd7-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02dd7-129">-Confirm</span></span>
<span data-ttu-id="02dd7-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02dd7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02dd7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02dd7-131">-WhatIf</span></span>
<span data-ttu-id="02dd7-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02dd7-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="02dd7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02dd7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02dd7-134">CommonParameters</span></span>
<span data-ttu-id="02dd7-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02dd7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02dd7-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02dd7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02dd7-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02dd7-137">INPUTS</span></span>

### <span data-ttu-id="02dd7-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="02dd7-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="02dd7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="02dd7-139">System.String</span></span>

## <span data-ttu-id="02dd7-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02dd7-140">OUTPUTS</span></span>

### <span data-ttu-id="02dd7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02dd7-141">System.Boolean</span></span>

## <span data-ttu-id="02dd7-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02dd7-142">NOTES</span></span>

## <span data-ttu-id="02dd7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02dd7-143">RELATED LINKS</span></span>
