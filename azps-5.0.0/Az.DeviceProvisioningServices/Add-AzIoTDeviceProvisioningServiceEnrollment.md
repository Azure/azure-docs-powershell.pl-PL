---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224500"
---
# <span data-ttu-id="29bd3-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="29bd3-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="29bd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="29bd3-103">Utwórz rekord rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="29bd3-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="29bd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29bd3-104">SYNTAX</span></span>

### <span data-ttu-id="29bd3-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29bd3-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="29bd3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29bd3-106">InputObjectSet</span></span>
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

### <span data-ttu-id="29bd3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29bd3-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="29bd3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29bd3-108">DESCRIPTION</span></span>
<span data-ttu-id="29bd3-109">Tworzenie rejestracji urządzenia w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="29bd3-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="29bd3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29bd3-110">EXAMPLES</span></span>

### <span data-ttu-id="29bd3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29bd3-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="29bd3-112">Tworzenie rejestracji przy użyciu typu zaświadczania SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="29bd3-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="29bd3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="29bd3-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="29bd3-114">Tworzenie rejestracji z zaświadczeniem modułu TPM.</span><span class="sxs-lookup"><span data-stu-id="29bd3-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="29bd3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="29bd3-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="29bd3-116">Tworzenie rejestracji z typem zaświadczania — x509</span><span class="sxs-lookup"><span data-stu-id="29bd3-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="29bd3-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="29bd3-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="29bd3-118">Tworzenie rejestracji przy użyciu typu zaświadczania o typie SymmetricKey oraz początkowym stanie sznurka.</span><span class="sxs-lookup"><span data-stu-id="29bd3-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="29bd3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29bd3-119">PARAMETERS</span></span>

### <span data-ttu-id="29bd3-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="29bd3-120">-AllocationPolicy</span></span>
<span data-ttu-id="29bd3-121">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="29bd3-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="29bd3-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="29bd3-122">-ApiVersion</span></span>
<span data-ttu-id="29bd3-123">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="29bd3-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="29bd3-124">-AttestationType</span></span>
<span data-ttu-id="29bd3-125">Mechanizm zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="29bd3-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="29bd3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bd3-126">-DefaultProfile</span></span>
<span data-ttu-id="29bd3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29bd3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29bd3-128">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="29bd3-128">-Desired</span></span>
<span data-ttu-id="29bd3-129">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="29bd3-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="29bd3-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="29bd3-130">-DeviceId</span></span>
<span data-ttu-id="29bd3-131">Identyfikator urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="29bd3-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="29bd3-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="29bd3-132">-DpsName</span></span>
<span data-ttu-id="29bd3-133">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="29bd3-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="29bd3-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="29bd3-134">-DpsObject</span></span>
<span data-ttu-id="29bd3-135">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="29bd3-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="29bd3-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="29bd3-136">-EdgeEnabled</span></span>
<span data-ttu-id="29bd3-137">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="29bd3-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="29bd3-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="29bd3-138">-EndorsementKey</span></span>
<span data-ttu-id="29bd3-139">Klucz poręczenia modułu TPM dla urządzenia modułu TPM.</span><span class="sxs-lookup"><span data-stu-id="29bd3-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="29bd3-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="29bd3-140">-IotHub</span></span>
<span data-ttu-id="29bd3-141">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="29bd3-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="29bd3-142">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="29bd3-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="29bd3-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="29bd3-143">-IotHubHostName</span></span>
<span data-ttu-id="29bd3-144">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="29bd3-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="29bd3-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="29bd3-145">-PrimaryCAName</span></span>
<span data-ttu-id="29bd3-146">Nazwa głównego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="29bd3-147">Jeśli zaświadczenie z certyfikatem głównego urzędu certyfikacji jest wymagane, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="29bd3-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="29bd3-148">-PrimaryCertificate</span></span>
<span data-ttu-id="29bd3-149">Ścieżka do pliku zawierającego podstawowy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="29bd3-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="29bd3-150">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="29bd3-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="29bd3-151">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="29bd3-151">-PrimaryKey</span></span>
<span data-ttu-id="29bd3-152">Podstawowy symetryczny kluczowy dostęp współdzielony, przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="29bd3-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="29bd3-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="29bd3-153">-ProvisioningStatus</span></span>
<span data-ttu-id="29bd3-154">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="29bd3-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="29bd3-155">-RegistrationId</span></span>
<span data-ttu-id="29bd3-156">Indywidualny Identyfikator rejestracji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="29bd3-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="29bd3-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="29bd3-158">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="29bd3-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="29bd3-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bd3-159">-ResourceGroupName</span></span>
<span data-ttu-id="29bd3-160">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="29bd3-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29bd3-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29bd3-161">-ResourceId</span></span>
<span data-ttu-id="29bd3-162">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="29bd3-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="29bd3-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="29bd3-163">-RootCertificate</span></span>
<span data-ttu-id="29bd3-164">Umożliwia tworzenie X509attestation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="29bd3-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="29bd3-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="29bd3-165">-SecondaryCAName</span></span>
<span data-ttu-id="29bd3-166">Nazwa certyfikatu pomocniczego głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="29bd3-167">Jeśli zaświadczenie z certyfikatem głównego urzędu certyfikacji jest wymagane, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="29bd3-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="29bd3-168">-SecondaryCertificate</span></span>
<span data-ttu-id="29bd3-169">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="29bd3-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="29bd3-170">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="29bd3-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="29bd3-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="29bd3-171">-SecondaryKey</span></span>
<span data-ttu-id="29bd3-172">Pomocniczy, symetryczny klucz dostępu współdzielony zapisany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="29bd3-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="29bd3-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="29bd3-173">-StorageRootKey</span></span>
<span data-ttu-id="29bd3-174">Klucz główny magazynowania modułu TPM dla urządzenia modułu TPM.</span><span class="sxs-lookup"><span data-stu-id="29bd3-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="29bd3-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="29bd3-175">-Tag</span></span>
<span data-ttu-id="29bd3-176">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="29bd3-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="29bd3-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="29bd3-177">-WebhookUrl</span></span>
<span data-ttu-id="29bd3-178">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="29bd3-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="29bd3-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29bd3-179">-Confirm</span></span>
<span data-ttu-id="29bd3-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bd3-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bd3-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bd3-181">-WhatIf</span></span>
<span data-ttu-id="29bd3-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bd3-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bd3-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29bd3-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bd3-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bd3-184">CommonParameters</span></span>
<span data-ttu-id="29bd3-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bd3-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bd3-186">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bd3-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bd3-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29bd3-187">INPUTS</span></span>

### <span data-ttu-id="29bd3-188">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="29bd3-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="29bd3-189">System. String</span><span class="sxs-lookup"><span data-stu-id="29bd3-189">System.String</span></span>

## <span data-ttu-id="29bd3-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29bd3-190">OUTPUTS</span></span>

### <span data-ttu-id="29bd3-191">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="29bd3-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="29bd3-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29bd3-192">NOTES</span></span>

## <span data-ttu-id="29bd3-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29bd3-193">RELATED LINKS</span></span>
