---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231947"
---
# <span data-ttu-id="d6eb5-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d6eb5-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="d6eb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d6eb5-103">Usuwanie grupy rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="d6eb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6eb5-104">SYNTAX</span></span>

### <span data-ttu-id="d6eb5-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6eb5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6eb5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6eb5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6eb5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6eb5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6eb5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d6eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="d6eb5-109">Usuwanie grupy rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d6eb5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6eb5-110">EXAMPLES</span></span>

### <span data-ttu-id="d6eb5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6eb5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="d6eb5-112">Usuwanie określonej grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="d6eb5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d6eb5-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="d6eb5-114">Usuwanie wszystkich grup rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="d6eb5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6eb5-115">PARAMETERS</span></span>

### <span data-ttu-id="d6eb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6eb5-116">-DefaultProfile</span></span>
<span data-ttu-id="d6eb5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6eb5-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d6eb5-118">-DpsName</span></span>
<span data-ttu-id="d6eb5-119">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d6eb5-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d6eb5-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d6eb5-120">-DpsObject</span></span>
<span data-ttu-id="d6eb5-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d6eb5-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d6eb5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6eb5-122">-Name</span></span>
<span data-ttu-id="d6eb5-123">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="d6eb5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6eb5-124">-PassThru</span></span>
<span data-ttu-id="d6eb5-125">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="d6eb5-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6eb5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6eb5-127">-ResourceGroupName</span></span>
<span data-ttu-id="d6eb5-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d6eb5-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d6eb5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6eb5-129">-ResourceId</span></span>
<span data-ttu-id="d6eb5-130">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d6eb5-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d6eb5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6eb5-131">-Confirm</span></span>
<span data-ttu-id="d6eb5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6eb5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6eb5-133">-WhatIf</span></span>
<span data-ttu-id="d6eb5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6eb5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6eb5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6eb5-136">CommonParameters</span></span>
<span data-ttu-id="d6eb5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6eb5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6eb5-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6eb5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6eb5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6eb5-139">INPUTS</span></span>

### <span data-ttu-id="d6eb5-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d6eb5-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d6eb5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6eb5-141">System.String</span></span>

## <span data-ttu-id="d6eb5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6eb5-142">OUTPUTS</span></span>

### <span data-ttu-id="d6eb5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6eb5-143">System.Boolean</span></span>

## <span data-ttu-id="d6eb5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6eb5-144">NOTES</span></span>

## <span data-ttu-id="d6eb5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6eb5-145">RELATED LINKS</span></span>
