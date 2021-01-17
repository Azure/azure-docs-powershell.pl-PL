---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489881"
---
# <span data-ttu-id="5d1d5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="5d1d5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="5d1d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d1d5-103">Usuń certyfikat usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="5d1d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d1d5-104">SYNTAX</span></span>

### <span data-ttu-id="5d1d5-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d1d5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d1d5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5d1d5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d1d5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5d1d5-108">DESCRIPTION</span></span>
<span data-ttu-id="5d1d5-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="5d1d5-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="5d1d5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d1d5-110">EXAMPLES</span></span>

### <span data-ttu-id="5d1d5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d1d5-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="5d1d5-112">Usuń "webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5d1d5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d1d5-113">PARAMETERS</span></span>

### <span data-ttu-id="5d1d5-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5d1d5-114">-CertificateName</span></span>
<span data-ttu-id="5d1d5-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="5d1d5-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d1d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d1d5-116">-DefaultProfile</span></span>
<span data-ttu-id="5d1d5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d1d5-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="5d1d5-118">-Etag</span></span>
<span data-ttu-id="5d1d5-119">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="5d1d5-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d1d5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d1d5-120">-InputObject</span></span>
<span data-ttu-id="5d1d5-121">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5d1d5-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1d5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d1d5-122">-Name</span></span>
<span data-ttu-id="5d1d5-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5d1d5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5d1d5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d1d5-124">-PassThru</span></span>
<span data-ttu-id="5d1d5-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5d1d5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5d1d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d1d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d1d5-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d1d5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5d1d5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d1d5-128">-ResourceId</span></span>
<span data-ttu-id="5d1d5-129">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5d1d5-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="5d1d5-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d1d5-130">-Confirm</span></span>
<span data-ttu-id="5d1d5-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d1d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d1d5-132">-WhatIf</span></span>
<span data-ttu-id="5d1d5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d1d5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d1d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d1d5-135">CommonParameters</span></span>
<span data-ttu-id="5d1d5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d1d5-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d1d5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d1d5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d1d5-138">INPUTS</span></span>

### <span data-ttu-id="5d1d5-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="5d1d5-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="5d1d5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5d1d5-140">System.String</span></span>

## <span data-ttu-id="5d1d5-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d1d5-141">OUTPUTS</span></span>

### <span data-ttu-id="5d1d5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d1d5-142">System.Boolean</span></span>

## <span data-ttu-id="5d1d5-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d1d5-143">NOTES</span></span>

## <span data-ttu-id="5d1d5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d1d5-144">RELATED LINKS</span></span>
