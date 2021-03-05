---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985076"
---
# <span data-ttu-id="1963f-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="1963f-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="1963f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1963f-102">SYNOPSIS</span></span>
<span data-ttu-id="1963f-103">Zaktualizuj grupę rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="1963f-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="1963f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1963f-104">SYNTAX</span></span>

### <span data-ttu-id="1963f-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1963f-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1963f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1963f-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1963f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1963f-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1963f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1963f-108">DESCRIPTION</span></span>
<span data-ttu-id="1963f-109">Zaktualizuj grupę rejestracji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="1963f-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1963f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1963f-110">EXAMPLES</span></span>

### <span data-ttu-id="1963f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1963f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="1963f-112">Zaktualizuj zasady i koncentratory alokacji dla grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1963f-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="1963f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1963f-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="1963f-114">Zaktualizuj początkowy stan rejestracji grupy.</span><span class="sxs-lookup"><span data-stu-id="1963f-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="1963f-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1963f-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="1963f-116">Aktualizowanie kluczy podstawowych i pomocniczych grupy rejestracji symetrycznej</span><span class="sxs-lookup"><span data-stu-id="1963f-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="1963f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1963f-117">PARAMETERS</span></span>

### <span data-ttu-id="1963f-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="1963f-118">-AllocationPolicy</span></span>
<span data-ttu-id="1963f-119">Typ alokacji dla urządzenia przypisanego do Centrum.</span><span class="sxs-lookup"><span data-stu-id="1963f-119">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1963f-120">-ApiVersion</span></span>
<span data-ttu-id="1963f-121">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="1963f-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="1963f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1963f-122">-DefaultProfile</span></span>
<span data-ttu-id="1963f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1963f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1963f-124">— Żądane</span><span class="sxs-lookup"><span data-stu-id="1963f-124">-Desired</span></span>
<span data-ttu-id="1963f-125">Początkowe żądane właściwości.</span><span class="sxs-lookup"><span data-stu-id="1963f-125">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="1963f-126">-DpsName</span></span>
<span data-ttu-id="1963f-127">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="1963f-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1963f-128">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="1963f-128">-DpsObject</span></span>
<span data-ttu-id="1963f-129">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="1963f-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1963f-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="1963f-130">-EdgeEnabled</span></span>
<span data-ttu-id="1963f-131">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="1963f-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-132">- IotHub</span><span class="sxs-lookup"><span data-stu-id="1963f-132">-IotHub</span></span>
<span data-ttu-id="1963f-133">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1963f-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="1963f-134">W przypadku wielu centrum IoT użyj listy rozdzielonych spacjami.</span><span class="sxs-lookup"><span data-stu-id="1963f-134">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="1963f-135">-IotHubHostName</span></span>
<span data-ttu-id="1963f-136">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1963f-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="1963f-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1963f-137">-Name</span></span>
<span data-ttu-id="1963f-138">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1963f-138">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="1963f-139">-PrimaryCAName</span></span>
<span data-ttu-id="1963f-140">Nazwa podstawowego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="1963f-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="1963f-141">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="1963f-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="1963f-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="1963f-142">-PrimaryCertificate</span></span>
<span data-ttu-id="1963f-143">Ścieżka do pliku zawierającego certyfikat podstawowy.</span><span class="sxs-lookup"><span data-stu-id="1963f-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="1963f-144">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="1963f-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="1963f-145">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="1963f-145">-PrimaryKey</span></span>
<span data-ttu-id="1963f-146">Podstawowy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="1963f-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="1963f-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="1963f-147">-ProvisioningStatus</span></span>
<span data-ttu-id="1963f-148">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1963f-148">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="1963f-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="1963f-150">Dane urządzenia do obsługi przy ponownej obsłudze administracyjnej do innego centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="1963f-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1963f-151">-ResourceGroupName</span></span>
<span data-ttu-id="1963f-152">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1963f-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1963f-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1963f-153">-ResourceId</span></span>
<span data-ttu-id="1963f-154">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="1963f-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1963f-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="1963f-155">-RootCertificate</span></span>
<span data-ttu-id="1963f-156">Umożliwia tworzenie X509attastation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="1963f-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="1963f-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="1963f-157">-SecondaryCAName</span></span>
<span data-ttu-id="1963f-158">Nazwa pomocniczego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="1963f-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="1963f-159">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="1963f-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="1963f-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="1963f-160">-SecondaryCertificate</span></span>
<span data-ttu-id="1963f-161">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="1963f-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="1963f-162">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="1963f-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="1963f-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1963f-163">-SecondaryKey</span></span>
<span data-ttu-id="1963f-164">Pomocniczy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="1963f-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="1963f-165">— Tag</span><span class="sxs-lookup"><span data-stu-id="1963f-165">-Tag</span></span>
<span data-ttu-id="1963f-166">Początkowe tagi tagi tagów.</span><span class="sxs-lookup"><span data-stu-id="1963f-166">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1963f-167">- WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="1963f-167">-WebhookUrl</span></span>
<span data-ttu-id="1963f-168">Adres URL webhook używany dla niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="1963f-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="1963f-169">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1963f-169">-Confirm</span></span>
<span data-ttu-id="1963f-170">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1963f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1963f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1963f-171">-WhatIf</span></span>
<span data-ttu-id="1963f-172">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1963f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1963f-173">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1963f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1963f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1963f-174">CommonParameters</span></span>
<span data-ttu-id="1963f-175">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1963f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1963f-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1963f-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1963f-177">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1963f-177">INPUTS</span></span>

### <span data-ttu-id="1963f-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1963f-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1963f-179">System.String</span><span class="sxs-lookup"><span data-stu-id="1963f-179">System.String</span></span>

## <span data-ttu-id="1963f-180">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1963f-180">OUTPUTS</span></span>

### <span data-ttu-id="1963f-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="1963f-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="1963f-182">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1963f-182">NOTES</span></span>

## <span data-ttu-id="1963f-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1963f-183">RELATED LINKS</span></span>
