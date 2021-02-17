---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196403"
---
# <span data-ttu-id="ae281-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="ae281-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="ae281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae281-102">SYNOPSIS</span></span>
<span data-ttu-id="ae281-103">Utwórz grupę rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="ae281-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="ae281-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae281-104">SYNTAX</span></span>

### <span data-ttu-id="ae281-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ae281-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae281-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ae281-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae281-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ae281-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae281-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae281-108">DESCRIPTION</span></span>
<span data-ttu-id="ae281-109">Utwórz grupę rejestracji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="ae281-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ae281-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae281-110">EXAMPLES</span></span>

### <span data-ttu-id="ae281-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae281-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="ae281-112">Tworzenie rejestracji za pomocą poświadczenia typu SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="ae281-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="ae281-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ae281-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="ae281-114">Tworzenie rejestracji za pomocą poświadczenia typu X509</span><span class="sxs-lookup"><span data-stu-id="ae281-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="ae281-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ae281-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="ae281-116">Utwórz rejestrację za pomocą poświadczenia typu SymmetricKey i stanu początkowego.</span><span class="sxs-lookup"><span data-stu-id="ae281-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="ae281-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae281-117">PARAMETERS</span></span>

### <span data-ttu-id="ae281-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ae281-118">-AllocationPolicy</span></span>
<span data-ttu-id="ae281-119">Typ alokacji dla urządzenia przypisanego do Centrum.</span><span class="sxs-lookup"><span data-stu-id="ae281-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="ae281-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ae281-120">-ApiVersion</span></span>
<span data-ttu-id="ae281-121">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="ae281-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="ae281-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="ae281-122">-AttestationType</span></span>
<span data-ttu-id="ae281-123">Mechanizm poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="ae281-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae281-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae281-124">-DefaultProfile</span></span>
<span data-ttu-id="ae281-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae281-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae281-126">— Żądane</span><span class="sxs-lookup"><span data-stu-id="ae281-126">-Desired</span></span>
<span data-ttu-id="ae281-127">Początkowe żądane właściwości.</span><span class="sxs-lookup"><span data-stu-id="ae281-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="ae281-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="ae281-128">-DpsName</span></span>
<span data-ttu-id="ae281-129">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ae281-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ae281-130">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="ae281-130">-DpsObject</span></span>
<span data-ttu-id="ae281-131">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ae281-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ae281-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ae281-132">-EdgeEnabled</span></span>
<span data-ttu-id="ae281-133">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="ae281-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="ae281-134">- IotHub</span><span class="sxs-lookup"><span data-stu-id="ae281-134">-IotHub</span></span>
<span data-ttu-id="ae281-135">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="ae281-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="ae281-136">W przypadku wielu centrum IoT użyj listy rozdzielonych spacjami.</span><span class="sxs-lookup"><span data-stu-id="ae281-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="ae281-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="ae281-137">-IotHubHostName</span></span>
<span data-ttu-id="ae281-138">Host name of the target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ae281-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="ae281-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae281-139">-Name</span></span>
<span data-ttu-id="ae281-140">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ae281-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="ae281-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="ae281-141">-PrimaryCAName</span></span>
<span data-ttu-id="ae281-142">Nazwa podstawowego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="ae281-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="ae281-143">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="ae281-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="ae281-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="ae281-144">-PrimaryCertificate</span></span>
<span data-ttu-id="ae281-145">Ścieżka do pliku zawierającego certyfikat podstawowy.</span><span class="sxs-lookup"><span data-stu-id="ae281-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="ae281-146">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="ae281-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ae281-147">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="ae281-147">-PrimaryKey</span></span>
<span data-ttu-id="ae281-148">Podstawowy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="ae281-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="ae281-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="ae281-149">-ProvisioningStatus</span></span>
<span data-ttu-id="ae281-150">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ae281-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="ae281-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae281-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="ae281-152">Dane urządzenia do obsługi przy ponownej obsłudze administracyjnej do innego centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="ae281-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="ae281-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae281-153">-ResourceGroupName</span></span>
<span data-ttu-id="ae281-154">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ae281-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ae281-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae281-155">-ResourceId</span></span>
<span data-ttu-id="ae281-156">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ae281-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ae281-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae281-157">-RootCertificate</span></span>
<span data-ttu-id="ae281-158">Umożliwia tworzenie X509attastation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="ae281-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="ae281-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="ae281-159">-SecondaryCAName</span></span>
<span data-ttu-id="ae281-160">Nazwa pomocniczego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="ae281-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="ae281-161">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="ae281-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="ae281-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="ae281-162">-SecondaryCertificate</span></span>
<span data-ttu-id="ae281-163">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="ae281-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="ae281-164">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="ae281-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ae281-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ae281-165">-SecondaryKey</span></span>
<span data-ttu-id="ae281-166">Pomocniczy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="ae281-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="ae281-167">— Tag</span><span class="sxs-lookup"><span data-stu-id="ae281-167">-Tag</span></span>
<span data-ttu-id="ae281-168">Początkowe tagi tagi tagów.</span><span class="sxs-lookup"><span data-stu-id="ae281-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="ae281-169">- WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="ae281-169">-WebhookUrl</span></span>
<span data-ttu-id="ae281-170">Adres URL webhook używany dla niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="ae281-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="ae281-171">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae281-171">-Confirm</span></span>
<span data-ttu-id="ae281-172">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae281-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae281-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae281-173">-WhatIf</span></span>
<span data-ttu-id="ae281-174">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae281-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae281-175">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae281-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae281-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae281-176">CommonParameters</span></span>
<span data-ttu-id="ae281-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae281-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae281-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae281-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae281-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae281-179">INPUTS</span></span>

### <span data-ttu-id="ae281-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ae281-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ae281-181">System.String</span><span class="sxs-lookup"><span data-stu-id="ae281-181">System.String</span></span>

## <span data-ttu-id="ae281-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae281-182">OUTPUTS</span></span>

### <span data-ttu-id="ae281-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="ae281-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="ae281-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae281-184">NOTES</span></span>

## <span data-ttu-id="ae281-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae281-185">RELATED LINKS</span></span>
