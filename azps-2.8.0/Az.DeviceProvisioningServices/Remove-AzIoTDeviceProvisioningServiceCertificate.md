---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705543"
---
# <span data-ttu-id="ab27f-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="ab27f-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="ab27f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab27f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab27f-103">Usuń certyfikat usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ab27f-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="ab27f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab27f-104">SYNTAX</span></span>

### <span data-ttu-id="ab27f-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab27f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab27f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab27f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab27f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ab27f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab27f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab27f-108">DESCRIPTION</span></span>
<span data-ttu-id="ab27f-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="ab27f-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="ab27f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab27f-110">EXAMPLES</span></span>

### <span data-ttu-id="ab27f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab27f-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="ab27f-112">Usuń "webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ab27f-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ab27f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab27f-113">PARAMETERS</span></span>

### <span data-ttu-id="ab27f-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ab27f-114">-CertificateName</span></span>
<span data-ttu-id="ab27f-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="ab27f-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="ab27f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab27f-116">-DefaultProfile</span></span>
<span data-ttu-id="ab27f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab27f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab27f-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="ab27f-118">-Etag</span></span>
<span data-ttu-id="ab27f-119">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="ab27f-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="ab27f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab27f-120">-InputObject</span></span>
<span data-ttu-id="ab27f-121">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ab27f-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="ab27f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab27f-122">-Name</span></span>
<span data-ttu-id="ab27f-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ab27f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ab27f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab27f-124">-PassThru</span></span>
<span data-ttu-id="ab27f-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ab27f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ab27f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab27f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab27f-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ab27f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ab27f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab27f-128">-ResourceId</span></span>
<span data-ttu-id="ab27f-129">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ab27f-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="ab27f-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab27f-130">-Confirm</span></span>
<span data-ttu-id="ab27f-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab27f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab27f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab27f-132">-WhatIf</span></span>
<span data-ttu-id="ab27f-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab27f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab27f-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab27f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab27f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab27f-135">CommonParameters</span></span>
<span data-ttu-id="ab27f-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab27f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab27f-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab27f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab27f-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab27f-138">INPUTS</span></span>

### <span data-ttu-id="ab27f-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="ab27f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="ab27f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ab27f-140">System.String</span></span>

## <span data-ttu-id="ab27f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab27f-141">OUTPUTS</span></span>

### <span data-ttu-id="ab27f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab27f-142">System.Boolean</span></span>

## <span data-ttu-id="ab27f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab27f-143">NOTES</span></span>

## <span data-ttu-id="ab27f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab27f-144">RELATED LINKS</span></span>
