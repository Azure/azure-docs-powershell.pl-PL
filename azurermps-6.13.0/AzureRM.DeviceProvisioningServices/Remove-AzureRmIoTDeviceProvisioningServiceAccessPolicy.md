---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548684"
---
# <span data-ttu-id="0d1a9-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0d1a9-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="0d1a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1a9-103">Usuwanie zasad dostępu współdzielonego w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d1a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d1a9-104">SYNTAX</span></span>

### <span data-ttu-id="0d1a9-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d1a9-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d1a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d1a9-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d1a9-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d1a9-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1a9-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0d1a9-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0d1a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d1a9-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1a9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d1a9-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="0d1a9-112">Usuwanie zasad dostępu współużytkowanego "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="0d1a9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0d1a9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="0d1a9-114">Usuwanie zasad dostępu współdzielonego "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="0d1a9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d1a9-115">PARAMETERS</span></span>

### <span data-ttu-id="0d1a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1a9-116">-DefaultProfile</span></span>
<span data-ttu-id="0d1a9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1a9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d1a9-118">-InputObject</span></span>
<span data-ttu-id="0d1a9-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0d1a9-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0d1a9-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="0d1a9-120">-KeyName</span></span>
<span data-ttu-id="0d1a9-121">Nazwa klucza zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0d1a9-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="0d1a9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d1a9-122">-Name</span></span>
<span data-ttu-id="0d1a9-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0d1a9-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0d1a9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d1a9-124">-PassThru</span></span>
<span data-ttu-id="0d1a9-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0d1a9-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0d1a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d1a9-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0d1a9-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0d1a9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d1a9-128">-ResourceId</span></span>
<span data-ttu-id="0d1a9-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0d1a9-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0d1a9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d1a9-130">-Confirm</span></span>
<span data-ttu-id="0d1a9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1a9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1a9-132">-WhatIf</span></span>
<span data-ttu-id="0d1a9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d1a9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1a9-135">CommonParameters</span></span>
<span data-ttu-id="0d1a9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1a9-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1a9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1a9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d1a9-138">INPUTS</span></span>

### <span data-ttu-id="0d1a9-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0d1a9-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="0d1a9-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d1a9-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0d1a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1a9-141">System.String</span></span>

## <span data-ttu-id="0d1a9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d1a9-142">OUTPUTS</span></span>

### <span data-ttu-id="0d1a9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d1a9-143">System.Boolean</span></span>

## <span data-ttu-id="0d1a9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d1a9-144">NOTES</span></span>

## <span data-ttu-id="0d1a9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d1a9-145">RELATED LINKS</span></span>
