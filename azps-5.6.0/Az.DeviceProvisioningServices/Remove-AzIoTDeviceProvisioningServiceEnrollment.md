---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: edf3845d9c4ac8a836212895fce2e5bbf4e40570
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985167"
---
# <span data-ttu-id="439c6-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="439c6-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="439c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="439c6-102">SYNOPSIS</span></span>
<span data-ttu-id="439c6-103">Usuń rekord rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="439c6-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="439c6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="439c6-104">SYNTAX</span></span>

### <span data-ttu-id="439c6-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="439c6-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="439c6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="439c6-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="439c6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="439c6-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439c6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="439c6-108">DESCRIPTION</span></span>
<span data-ttu-id="439c6-109">Usuń rejestrację urządzenia w usłudze inicjowania obsługi administracyjnej urządzenia w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="439c6-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="439c6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="439c6-110">EXAMPLES</span></span>

### <span data-ttu-id="439c6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="439c6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="439c6-112">Usuwanie określonego rekordu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="439c6-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="439c6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="439c6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="439c6-114">Usuń wszystkie rekordy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="439c6-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="439c6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="439c6-115">PARAMETERS</span></span>

### <span data-ttu-id="439c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439c6-116">-DefaultProfile</span></span>
<span data-ttu-id="439c6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="439c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="439c6-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="439c6-118">-DpsName</span></span>
<span data-ttu-id="439c6-119">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="439c6-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="439c6-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="439c6-120">-DpsObject</span></span>
<span data-ttu-id="439c6-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="439c6-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="439c6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="439c6-122">-PassThru</span></span>
<span data-ttu-id="439c6-123">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="439c6-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="439c6-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="439c6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="439c6-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="439c6-125">-RegistrationId</span></span>
<span data-ttu-id="439c6-126">Identyfikator rejestracji indywidualnej.</span><span class="sxs-lookup"><span data-stu-id="439c6-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="439c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="439c6-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="439c6-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="439c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="439c6-129">-ResourceId</span></span>
<span data-ttu-id="439c6-130">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="439c6-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="439c6-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="439c6-131">-Confirm</span></span>
<span data-ttu-id="439c6-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="439c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="439c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439c6-133">-WhatIf</span></span>
<span data-ttu-id="439c6-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439c6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439c6-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="439c6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="439c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439c6-136">CommonParameters</span></span>
<span data-ttu-id="439c6-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439c6-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439c6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439c6-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="439c6-139">INPUTS</span></span>

### <span data-ttu-id="439c6-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="439c6-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="439c6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="439c6-141">System.String</span></span>

## <span data-ttu-id="439c6-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="439c6-142">OUTPUTS</span></span>

### <span data-ttu-id="439c6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="439c6-143">System.Boolean</span></span>

## <span data-ttu-id="439c6-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="439c6-144">NOTES</span></span>

## <span data-ttu-id="439c6-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="439c6-145">RELATED LINKS</span></span>
