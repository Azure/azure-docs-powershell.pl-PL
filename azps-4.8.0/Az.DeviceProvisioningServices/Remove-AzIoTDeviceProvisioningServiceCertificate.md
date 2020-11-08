---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223963"
---
# <span data-ttu-id="d78a3-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="d78a3-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="d78a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d78a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d78a3-103">Usuń certyfikat usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d78a3-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="d78a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d78a3-104">SYNTAX</span></span>

### <span data-ttu-id="d78a3-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d78a3-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78a3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d78a3-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78a3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d78a3-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d78a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d78a3-108">DESCRIPTION</span></span>
<span data-ttu-id="d78a3-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="d78a3-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="d78a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d78a3-110">EXAMPLES</span></span>

### <span data-ttu-id="d78a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d78a3-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="d78a3-112">Usuń "webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d78a3-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d78a3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d78a3-113">PARAMETERS</span></span>

### <span data-ttu-id="d78a3-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d78a3-114">-CertificateName</span></span>
<span data-ttu-id="d78a3-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d78a3-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="d78a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78a3-116">-DefaultProfile</span></span>
<span data-ttu-id="d78a3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d78a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d78a3-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="d78a3-118">-Etag</span></span>
<span data-ttu-id="d78a3-119">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d78a3-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="d78a3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d78a3-120">-InputObject</span></span>
<span data-ttu-id="d78a3-121">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d78a3-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="d78a3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d78a3-122">-Name</span></span>
<span data-ttu-id="d78a3-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d78a3-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d78a3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d78a3-124">-PassThru</span></span>
<span data-ttu-id="d78a3-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d78a3-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d78a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="d78a3-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d78a3-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d78a3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d78a3-128">-ResourceId</span></span>
<span data-ttu-id="d78a3-129">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d78a3-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d78a3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d78a3-130">-Confirm</span></span>
<span data-ttu-id="d78a3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d78a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d78a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d78a3-132">-WhatIf</span></span>
<span data-ttu-id="d78a3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d78a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d78a3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d78a3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d78a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78a3-135">CommonParameters</span></span>
<span data-ttu-id="d78a3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78a3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d78a3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78a3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d78a3-138">INPUTS</span></span>

### <span data-ttu-id="d78a3-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d78a3-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="d78a3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d78a3-140">System.String</span></span>

## <span data-ttu-id="d78a3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d78a3-141">OUTPUTS</span></span>

### <span data-ttu-id="d78a3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d78a3-142">System.Boolean</span></span>

## <span data-ttu-id="d78a3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d78a3-143">NOTES</span></span>

## <span data-ttu-id="d78a3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d78a3-144">RELATED LINKS</span></span>
