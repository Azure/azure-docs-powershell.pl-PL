---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 9b27875e19837d7e3b69770234bdcd19648c3130
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985160"
---
# <span data-ttu-id="dab5f-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="dab5f-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="dab5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dab5f-102">SYNOPSIS</span></span>
<span data-ttu-id="dab5f-103">Usuń grupę rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="dab5f-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="dab5f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dab5f-104">SYNTAX</span></span>

### <span data-ttu-id="dab5f-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dab5f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dab5f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dab5f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dab5f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dab5f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab5f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dab5f-108">DESCRIPTION</span></span>
<span data-ttu-id="dab5f-109">Usuń grupę rejestracji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="dab5f-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="dab5f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dab5f-110">EXAMPLES</span></span>

### <span data-ttu-id="dab5f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dab5f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="dab5f-112">Usuwanie określonej grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="dab5f-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="dab5f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dab5f-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="dab5f-114">Usuń wszystkie grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="dab5f-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="dab5f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dab5f-115">PARAMETERS</span></span>

### <span data-ttu-id="dab5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab5f-116">-DefaultProfile</span></span>
<span data-ttu-id="dab5f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dab5f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dab5f-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="dab5f-118">-DpsName</span></span>
<span data-ttu-id="dab5f-119">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dab5f-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dab5f-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="dab5f-120">-DpsObject</span></span>
<span data-ttu-id="dab5f-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dab5f-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="dab5f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dab5f-122">-Name</span></span>
<span data-ttu-id="dab5f-123">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="dab5f-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="dab5f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dab5f-124">-PassThru</span></span>
<span data-ttu-id="dab5f-125">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="dab5f-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="dab5f-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dab5f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dab5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="dab5f-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dab5f-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dab5f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dab5f-129">-ResourceId</span></span>
<span data-ttu-id="dab5f-130">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dab5f-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dab5f-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dab5f-131">-Confirm</span></span>
<span data-ttu-id="dab5f-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dab5f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab5f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab5f-133">-WhatIf</span></span>
<span data-ttu-id="dab5f-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dab5f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab5f-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dab5f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab5f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab5f-136">CommonParameters</span></span>
<span data-ttu-id="dab5f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dab5f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab5f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab5f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab5f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dab5f-139">INPUTS</span></span>

### <span data-ttu-id="dab5f-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="dab5f-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="dab5f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="dab5f-141">System.String</span></span>

## <span data-ttu-id="dab5f-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dab5f-142">OUTPUTS</span></span>

### <span data-ttu-id="dab5f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dab5f-143">System.Boolean</span></span>

## <span data-ttu-id="dab5f-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dab5f-144">NOTES</span></span>

## <span data-ttu-id="dab5f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dab5f-145">RELATED LINKS</span></span>
