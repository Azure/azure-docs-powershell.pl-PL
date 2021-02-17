---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196410"
---
# <span data-ttu-id="cdd22-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="cdd22-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="cdd22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd22-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd22-103">Utwórz rekord rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="cdd22-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="cdd22-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdd22-104">SYNTAX</span></span>

### <span data-ttu-id="cdd22-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdd22-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd22-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdd22-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd22-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cdd22-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd22-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdd22-108">DESCRIPTION</span></span>
<span data-ttu-id="cdd22-109">Utwórz rejestrację urządzenia w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd22-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="cdd22-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdd22-110">EXAMPLES</span></span>

### <span data-ttu-id="cdd22-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdd22-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="cdd22-112">Tworzenie rejestracji za pomocą poświadczenia typu SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="cdd22-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="cdd22-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdd22-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="cdd22-114">Utwórz rejestrację za pomocą atestacji TPM.</span><span class="sxs-lookup"><span data-stu-id="cdd22-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="cdd22-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cdd22-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="cdd22-116">Tworzenie rejestracji za pomocą poświadczenia typu X509</span><span class="sxs-lookup"><span data-stu-id="cdd22-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="cdd22-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="cdd22-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="cdd22-118">Utwórz rejestrację za pomocą poświadczenia typu SymmetricKey i stanu początkowego.</span><span class="sxs-lookup"><span data-stu-id="cdd22-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="cdd22-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdd22-119">PARAMETERS</span></span>

### <span data-ttu-id="cdd22-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="cdd22-120">-AllocationPolicy</span></span>
<span data-ttu-id="cdd22-121">Typ alokacji dla urządzenia przypisanego do Centrum.</span><span class="sxs-lookup"><span data-stu-id="cdd22-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="cdd22-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cdd22-122">-ApiVersion</span></span>
<span data-ttu-id="cdd22-123">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="cdd22-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="cdd22-124">-AttestationType</span></span>
<span data-ttu-id="cdd22-125">Mechanizm poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cdd22-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="cdd22-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd22-126">-DefaultProfile</span></span>
<span data-ttu-id="cdd22-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd22-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd22-128">— Żądane</span><span class="sxs-lookup"><span data-stu-id="cdd22-128">-Desired</span></span>
<span data-ttu-id="cdd22-129">Początkowe żądane właściwości.</span><span class="sxs-lookup"><span data-stu-id="cdd22-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="cdd22-130">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="cdd22-130">-DeviceId</span></span>
<span data-ttu-id="cdd22-131">Identyfikator urządzenia centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="cdd22-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="cdd22-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="cdd22-132">-DpsName</span></span>
<span data-ttu-id="cdd22-133">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="cdd22-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cdd22-134">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="cdd22-134">-DpsObject</span></span>
<span data-ttu-id="cdd22-135">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="cdd22-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cdd22-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="cdd22-136">-EdgeEnabled</span></span>
<span data-ttu-id="cdd22-137">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="cdd22-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="cdd22-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="cdd22-138">-EndorsementKey</span></span>
<span data-ttu-id="cdd22-139">Klucz rekomendacji dla urządzenia TPM.</span><span class="sxs-lookup"><span data-stu-id="cdd22-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="cdd22-140">- IotHub</span><span class="sxs-lookup"><span data-stu-id="cdd22-140">-IotHub</span></span>
<span data-ttu-id="cdd22-141">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="cdd22-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="cdd22-142">W przypadku wielu centrum IoT użyj listy rozdzielonych spacjami.</span><span class="sxs-lookup"><span data-stu-id="cdd22-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="cdd22-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="cdd22-143">-IotHubHostName</span></span>
<span data-ttu-id="cdd22-144">Host name of the target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="cdd22-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="cdd22-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="cdd22-145">-PrimaryCAName</span></span>
<span data-ttu-id="cdd22-146">Nazwa podstawowego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="cdd22-147">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="cdd22-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="cdd22-148">-PrimaryCertificate</span></span>
<span data-ttu-id="cdd22-149">Ścieżka do pliku zawierającego certyfikat podstawowy.</span><span class="sxs-lookup"><span data-stu-id="cdd22-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="cdd22-150">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="cdd22-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="cdd22-151">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="cdd22-151">-PrimaryKey</span></span>
<span data-ttu-id="cdd22-152">Podstawowy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="cdd22-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="cdd22-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="cdd22-153">-ProvisioningStatus</span></span>
<span data-ttu-id="cdd22-154">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="cdd22-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="cdd22-155">-RegistrationId</span></span>
<span data-ttu-id="cdd22-156">Identyfikator rejestracji indywidualnej.</span><span class="sxs-lookup"><span data-stu-id="cdd22-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="cdd22-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="cdd22-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="cdd22-158">Dane urządzenia do obsługi przy ponownej obsłudze administracyjnej do innego centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="cdd22-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="cdd22-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd22-159">-ResourceGroupName</span></span>
<span data-ttu-id="cdd22-160">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cdd22-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cdd22-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd22-161">-ResourceId</span></span>
<span data-ttu-id="cdd22-162">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="cdd22-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cdd22-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="cdd22-163">-RootCertificate</span></span>
<span data-ttu-id="cdd22-164">Umożliwia tworzenie X509attastation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="cdd22-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="cdd22-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="cdd22-165">-SecondaryCAName</span></span>
<span data-ttu-id="cdd22-166">Nazwa pomocniczego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="cdd22-167">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="cdd22-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="cdd22-168">-SecondaryCertificate</span></span>
<span data-ttu-id="cdd22-169">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="cdd22-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="cdd22-170">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="cdd22-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="cdd22-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cdd22-171">-SecondaryKey</span></span>
<span data-ttu-id="cdd22-172">Pomocniczy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="cdd22-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="cdd22-173">- StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="cdd22-173">-StorageRootKey</span></span>
<span data-ttu-id="cdd22-174">Klucz główny magazynu DLA urządzenia TPM.</span><span class="sxs-lookup"><span data-stu-id="cdd22-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="cdd22-175">— Tag</span><span class="sxs-lookup"><span data-stu-id="cdd22-175">-Tag</span></span>
<span data-ttu-id="cdd22-176">Początkowe tagi tagi tagów.</span><span class="sxs-lookup"><span data-stu-id="cdd22-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="cdd22-177">- WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="cdd22-177">-WebhookUrl</span></span>
<span data-ttu-id="cdd22-178">Adres URL webhook używany dla niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="cdd22-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="cdd22-179">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdd22-179">-Confirm</span></span>
<span data-ttu-id="cdd22-180">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cdd22-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd22-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd22-181">-WhatIf</span></span>
<span data-ttu-id="cdd22-182">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd22-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd22-183">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cdd22-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd22-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd22-184">CommonParameters</span></span>
<span data-ttu-id="cdd22-185">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd22-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd22-186">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd22-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd22-187">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdd22-187">INPUTS</span></span>

### <span data-ttu-id="cdd22-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="cdd22-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="cdd22-189">System.String</span><span class="sxs-lookup"><span data-stu-id="cdd22-189">System.String</span></span>

## <span data-ttu-id="cdd22-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdd22-190">OUTPUTS</span></span>

### <span data-ttu-id="cdd22-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="cdd22-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="cdd22-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdd22-192">NOTES</span></span>

## <span data-ttu-id="cdd22-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdd22-193">RELATED LINKS</span></span>
