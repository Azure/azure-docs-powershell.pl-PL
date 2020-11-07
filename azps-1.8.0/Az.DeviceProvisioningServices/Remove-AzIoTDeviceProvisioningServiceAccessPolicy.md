---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 1efd429489be41f619454fd2b772c7cbb1ebc5c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709883"
---
# <span data-ttu-id="7ca8d-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ca8d-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="7ca8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ca8d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca8d-103">Usuwanie zasad dostępu współdzielonego w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7ca8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ca8d-104">SYNTAX</span></span>

### <span data-ttu-id="7ca8d-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ca8d-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ca8d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ca8d-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca8d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7ca8d-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca8d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7ca8d-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca8d-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7ca8d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7ca8d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ca8d-110">EXAMPLES</span></span>

### <span data-ttu-id="7ca8d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ca8d-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="7ca8d-112">Usuwanie zasad dostępu współużytkowanego "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7ca8d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7ca8d-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="7ca8d-114">Usuwanie zasad dostępu współdzielonego "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="7ca8d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ca8d-115">PARAMETERS</span></span>

### <span data-ttu-id="7ca8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca8d-116">-DefaultProfile</span></span>
<span data-ttu-id="7ca8d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca8d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ca8d-118">-InputObject</span></span>
<span data-ttu-id="7ca8d-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="7ca8d-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca8d-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="7ca8d-120">-KeyName</span></span>
<span data-ttu-id="7ca8d-121">Nazwa klucza zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="7ca8d-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="7ca8d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ca8d-122">-Name</span></span>
<span data-ttu-id="7ca8d-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="7ca8d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7ca8d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ca8d-124">-PassThru</span></span>
<span data-ttu-id="7ca8d-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7ca8d-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7ca8d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca8d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ca8d-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7ca8d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7ca8d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca8d-128">-ResourceId</span></span>
<span data-ttu-id="7ca8d-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="7ca8d-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7ca8d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ca8d-130">-Confirm</span></span>
<span data-ttu-id="7ca8d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca8d-132">-WhatIf</span></span>
<span data-ttu-id="7ca8d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca8d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca8d-135">CommonParameters</span></span>
<span data-ttu-id="7ca8d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca8d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca8d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ca8d-138">INPUTS</span></span>

### <span data-ttu-id="7ca8d-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="7ca8d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="7ca8d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca8d-140">System.String</span></span>

## <span data-ttu-id="7ca8d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ca8d-141">OUTPUTS</span></span>

### <span data-ttu-id="7ca8d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ca8d-142">System.Boolean</span></span>

## <span data-ttu-id="7ca8d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ca8d-143">NOTES</span></span>

## <span data-ttu-id="7ca8d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ca8d-144">RELATED LINKS</span></span>
