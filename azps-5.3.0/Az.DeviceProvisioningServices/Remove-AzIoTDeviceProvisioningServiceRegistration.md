---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376938"
---
# <span data-ttu-id="846cd-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="846cd-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="846cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="846cd-102">SYNOPSIS</span></span>
<span data-ttu-id="846cd-103">Umożliwia usunięcie rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="846cd-103">Deletes the device registration.</span></span>

## <span data-ttu-id="846cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="846cd-104">SYNTAX</span></span>

### <span data-ttu-id="846cd-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="846cd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="846cd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="846cd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="846cd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="846cd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="846cd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="846cd-108">DESCRIPTION</span></span>
<span data-ttu-id="846cd-109">Usuwanie rejestracji urządzenia w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="846cd-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="846cd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="846cd-110">EXAMPLES</span></span>

### <span data-ttu-id="846cd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="846cd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="846cd-112">Usuwanie rejestracji urządzenia w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="846cd-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="846cd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="846cd-113">PARAMETERS</span></span>

### <span data-ttu-id="846cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846cd-114">-DefaultProfile</span></span>
<span data-ttu-id="846cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="846cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="846cd-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="846cd-116">-DpsName</span></span>
<span data-ttu-id="846cd-117">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="846cd-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="846cd-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="846cd-118">-DpsObject</span></span>
<span data-ttu-id="846cd-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="846cd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="846cd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="846cd-120">-PassThru</span></span>
<span data-ttu-id="846cd-121">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="846cd-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="846cd-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="846cd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="846cd-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="846cd-123">-RegistrationId</span></span>
<span data-ttu-id="846cd-124">Identyfikator rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="846cd-124">ID of device registration.</span></span>

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

### <span data-ttu-id="846cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="846cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="846cd-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="846cd-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="846cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="846cd-127">-ResourceId</span></span>
<span data-ttu-id="846cd-128">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="846cd-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="846cd-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="846cd-129">-Confirm</span></span>
<span data-ttu-id="846cd-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="846cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="846cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846cd-131">-WhatIf</span></span>
<span data-ttu-id="846cd-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="846cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="846cd-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="846cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="846cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846cd-134">CommonParameters</span></span>
<span data-ttu-id="846cd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="846cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846cd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="846cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846cd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="846cd-137">INPUTS</span></span>

### <span data-ttu-id="846cd-138">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="846cd-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="846cd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="846cd-139">System.String</span></span>

## <span data-ttu-id="846cd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="846cd-140">OUTPUTS</span></span>

### <span data-ttu-id="846cd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="846cd-141">System.Boolean</span></span>

## <span data-ttu-id="846cd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="846cd-142">NOTES</span></span>

## <span data-ttu-id="846cd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="846cd-143">RELATED LINKS</span></span>
