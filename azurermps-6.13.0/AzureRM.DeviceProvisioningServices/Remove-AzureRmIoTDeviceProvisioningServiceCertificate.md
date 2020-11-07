---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717416"
---
# <span data-ttu-id="441dc-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="441dc-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="441dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="441dc-102">SYNOPSIS</span></span>
<span data-ttu-id="441dc-103">Usuń certyfikat usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="441dc-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="441dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="441dc-104">SYNTAX</span></span>

### <span data-ttu-id="441dc-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="441dc-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="441dc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="441dc-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="441dc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="441dc-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="441dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="441dc-108">DESCRIPTION</span></span>
<span data-ttu-id="441dc-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="441dc-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="441dc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="441dc-110">EXAMPLES</span></span>

### <span data-ttu-id="441dc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="441dc-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="441dc-112">Usuń "webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="441dc-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="441dc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="441dc-113">PARAMETERS</span></span>

### <span data-ttu-id="441dc-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="441dc-114">-CertificateName</span></span>
<span data-ttu-id="441dc-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="441dc-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="441dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441dc-116">-DefaultProfile</span></span>
<span data-ttu-id="441dc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="441dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441dc-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="441dc-118">-Etag</span></span>
<span data-ttu-id="441dc-119">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="441dc-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="441dc-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="441dc-120">-InputObject</span></span>
<span data-ttu-id="441dc-121">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="441dc-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="441dc-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="441dc-122">-Name</span></span>
<span data-ttu-id="441dc-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="441dc-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="441dc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="441dc-124">-PassThru</span></span>
<span data-ttu-id="441dc-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="441dc-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="441dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="441dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="441dc-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="441dc-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="441dc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="441dc-128">-ResourceId</span></span>
<span data-ttu-id="441dc-129">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="441dc-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="441dc-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="441dc-130">-Confirm</span></span>
<span data-ttu-id="441dc-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="441dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="441dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="441dc-132">-WhatIf</span></span>
<span data-ttu-id="441dc-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="441dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="441dc-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="441dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="441dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441dc-135">CommonParameters</span></span>
<span data-ttu-id="441dc-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="441dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441dc-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="441dc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441dc-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="441dc-138">INPUTS</span></span>

### <span data-ttu-id="441dc-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="441dc-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="441dc-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="441dc-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="441dc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="441dc-141">System.String</span></span>

## <span data-ttu-id="441dc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="441dc-142">OUTPUTS</span></span>

### <span data-ttu-id="441dc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="441dc-143">System.Boolean</span></span>

## <span data-ttu-id="441dc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="441dc-144">NOTES</span></span>

## <span data-ttu-id="441dc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="441dc-145">RELATED LINKS</span></span>
