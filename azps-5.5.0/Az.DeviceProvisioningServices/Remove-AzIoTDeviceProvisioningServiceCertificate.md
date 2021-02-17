---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185994"
---
# <span data-ttu-id="38e1a-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="38e1a-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="38e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="38e1a-103">Usuń certyfikat usługi inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="38e1a-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="38e1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38e1a-104">SYNTAX</span></span>

### <span data-ttu-id="38e1a-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="38e1a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e1a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38e1a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e1a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38e1a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38e1a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="38e1a-108">DESCRIPTION</span></span>
<span data-ttu-id="38e1a-109">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates zobacz.</span><span class="sxs-lookup"><span data-stu-id="38e1a-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="38e1a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38e1a-110">EXAMPLES</span></span>

### <span data-ttu-id="38e1a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38e1a-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="38e1a-112">Usuń "mycertificate" w usłudze inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="38e1a-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="38e1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38e1a-113">PARAMETERS</span></span>

### <span data-ttu-id="38e1a-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="38e1a-114">-CertificateName</span></span>
<span data-ttu-id="38e1a-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="38e1a-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="38e1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e1a-116">-DefaultProfile</span></span>
<span data-ttu-id="38e1a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38e1a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38e1a-118">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="38e1a-118">-Etag</span></span>
<span data-ttu-id="38e1a-119">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="38e1a-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="38e1a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38e1a-120">-InputObject</span></span>
<span data-ttu-id="38e1a-121">Obiekt certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="38e1a-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="38e1a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38e1a-122">-Name</span></span>
<span data-ttu-id="38e1a-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="38e1a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="38e1a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38e1a-124">-PassThru</span></span>
<span data-ttu-id="38e1a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="38e1a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="38e1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="38e1a-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="38e1a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="38e1a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38e1a-128">-ResourceId</span></span>
<span data-ttu-id="38e1a-129">Identyfikator zasobu certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="38e1a-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="38e1a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38e1a-130">-Confirm</span></span>
<span data-ttu-id="38e1a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38e1a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e1a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e1a-132">-WhatIf</span></span>
<span data-ttu-id="38e1a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38e1a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38e1a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38e1a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38e1a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e1a-135">CommonParameters</span></span>
<span data-ttu-id="38e1a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38e1a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e1a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e1a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e1a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38e1a-138">INPUTS</span></span>

### <span data-ttu-id="38e1a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="38e1a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="38e1a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="38e1a-140">System.String</span></span>

## <span data-ttu-id="38e1a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38e1a-141">OUTPUTS</span></span>

### <span data-ttu-id="38e1a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38e1a-142">System.Boolean</span></span>

## <span data-ttu-id="38e1a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38e1a-143">NOTES</span></span>

## <span data-ttu-id="38e1a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38e1a-144">RELATED LINKS</span></span>
