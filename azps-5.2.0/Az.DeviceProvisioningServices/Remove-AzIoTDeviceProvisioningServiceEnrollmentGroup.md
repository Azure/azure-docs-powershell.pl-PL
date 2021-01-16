---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328697"
---
# <span data-ttu-id="95b33-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="95b33-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="95b33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95b33-102">SYNOPSIS</span></span>
<span data-ttu-id="95b33-103">Usuwanie grupy rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="95b33-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="95b33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95b33-104">SYNTAX</span></span>

### <span data-ttu-id="95b33-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="95b33-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95b33-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="95b33-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95b33-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="95b33-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b33-108">Opis</span><span class="sxs-lookup"><span data-stu-id="95b33-108">DESCRIPTION</span></span>
<span data-ttu-id="95b33-109">Usuwanie grupy rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="95b33-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="95b33-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95b33-110">EXAMPLES</span></span>

### <span data-ttu-id="95b33-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95b33-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="95b33-112">Usuwanie określonej grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="95b33-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="95b33-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="95b33-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="95b33-114">Usuwanie wszystkich grup rejestracji.</span><span class="sxs-lookup"><span data-stu-id="95b33-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="95b33-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95b33-115">PARAMETERS</span></span>

### <span data-ttu-id="95b33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b33-116">-DefaultProfile</span></span>
<span data-ttu-id="95b33-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95b33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95b33-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="95b33-118">-DpsName</span></span>
<span data-ttu-id="95b33-119">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="95b33-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="95b33-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="95b33-120">-DpsObject</span></span>
<span data-ttu-id="95b33-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="95b33-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="95b33-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95b33-122">-Name</span></span>
<span data-ttu-id="95b33-123">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="95b33-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="95b33-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95b33-124">-PassThru</span></span>
<span data-ttu-id="95b33-125">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="95b33-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="95b33-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="95b33-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="95b33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95b33-127">-ResourceGroupName</span></span>
<span data-ttu-id="95b33-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="95b33-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="95b33-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95b33-129">-ResourceId</span></span>
<span data-ttu-id="95b33-130">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="95b33-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="95b33-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95b33-131">-Confirm</span></span>
<span data-ttu-id="95b33-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b33-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95b33-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b33-133">-WhatIf</span></span>
<span data-ttu-id="95b33-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b33-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95b33-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95b33-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95b33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b33-136">CommonParameters</span></span>
<span data-ttu-id="95b33-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b33-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b33-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b33-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95b33-139">INPUTS</span></span>

### <span data-ttu-id="95b33-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="95b33-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="95b33-141">System. String</span><span class="sxs-lookup"><span data-stu-id="95b33-141">System.String</span></span>

## <span data-ttu-id="95b33-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95b33-142">OUTPUTS</span></span>

### <span data-ttu-id="95b33-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95b33-143">System.Boolean</span></span>

## <span data-ttu-id="95b33-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95b33-144">NOTES</span></span>

## <span data-ttu-id="95b33-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95b33-145">RELATED LINKS</span></span>
