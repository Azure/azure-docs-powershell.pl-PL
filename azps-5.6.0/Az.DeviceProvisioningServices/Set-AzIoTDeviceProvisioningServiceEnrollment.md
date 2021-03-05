---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985083"
---
# <span data-ttu-id="33a38-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="33a38-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="33a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a38-102">SYNOPSIS</span></span>
<span data-ttu-id="33a38-103">Aktualizowanie rekordu rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="33a38-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="33a38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33a38-104">SYNTAX</span></span>

### <span data-ttu-id="33a38-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33a38-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a38-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="33a38-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a38-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33a38-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33a38-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="33a38-108">DESCRIPTION</span></span>
<span data-ttu-id="33a38-109">Zaktualizuj rejestrację urządzenia w usłudze inicjowania obsługi administracyjnej urządzenia w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="33a38-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="33a38-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33a38-110">EXAMPLES</span></span>

### <span data-ttu-id="33a38-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33a38-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="33a38-112">Zaktualizuj zasady i koncentratory alokacji dla rekordu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="33a38-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="33a38-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33a38-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="33a38-114">Zaktualizuj początkowy stan rejestracji.</span><span class="sxs-lookup"><span data-stu-id="33a38-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="33a38-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="33a38-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="33a38-116">Aktualizowanie certyfikatów podstawowych i pomocniczych rejestracji klucza symetrycznego</span><span class="sxs-lookup"><span data-stu-id="33a38-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="33a38-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33a38-117">PARAMETERS</span></span>

### <span data-ttu-id="33a38-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="33a38-118">-AllocationPolicy</span></span>
<span data-ttu-id="33a38-119">Typ alokacji dla urządzenia przypisanego do Centrum.</span><span class="sxs-lookup"><span data-stu-id="33a38-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="33a38-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="33a38-120">-ApiVersion</span></span>
<span data-ttu-id="33a38-121">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="33a38-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="33a38-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a38-122">-DefaultProfile</span></span>
<span data-ttu-id="33a38-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33a38-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a38-124">— Żądane</span><span class="sxs-lookup"><span data-stu-id="33a38-124">-Desired</span></span>
<span data-ttu-id="33a38-125">Początkowe żądane właściwości.</span><span class="sxs-lookup"><span data-stu-id="33a38-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="33a38-126">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="33a38-126">-DeviceId</span></span>
<span data-ttu-id="33a38-127">Identyfikator urządzenia centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="33a38-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="33a38-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="33a38-128">-DpsName</span></span>
<span data-ttu-id="33a38-129">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="33a38-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="33a38-130">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="33a38-130">-DpsObject</span></span>
<span data-ttu-id="33a38-131">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="33a38-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="33a38-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="33a38-132">-EdgeEnabled</span></span>
<span data-ttu-id="33a38-133">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="33a38-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="33a38-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="33a38-134">-EndorsementKey</span></span>
<span data-ttu-id="33a38-135">Klucz rekomendacji dla urządzenia TPM.</span><span class="sxs-lookup"><span data-stu-id="33a38-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="33a38-136">- IotHub</span><span class="sxs-lookup"><span data-stu-id="33a38-136">-IotHub</span></span>
<span data-ttu-id="33a38-137">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="33a38-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="33a38-138">W przypadku wielu centrum IoT użyj listy rozdzielonych spacjami.</span><span class="sxs-lookup"><span data-stu-id="33a38-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="33a38-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="33a38-139">-IotHubHostName</span></span>
<span data-ttu-id="33a38-140">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="33a38-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="33a38-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="33a38-141">-PrimaryCAName</span></span>
<span data-ttu-id="33a38-142">Nazwa podstawowego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="33a38-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="33a38-143">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="33a38-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="33a38-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="33a38-144">-PrimaryCertificate</span></span>
<span data-ttu-id="33a38-145">Ścieżka do pliku zawierającego certyfikat podstawowy.</span><span class="sxs-lookup"><span data-stu-id="33a38-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="33a38-146">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="33a38-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="33a38-147">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="33a38-147">-PrimaryKey</span></span>
<span data-ttu-id="33a38-148">Podstawowy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="33a38-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="33a38-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="33a38-149">-ProvisioningStatus</span></span>
<span data-ttu-id="33a38-150">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="33a38-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="33a38-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="33a38-151">-RegistrationId</span></span>
<span data-ttu-id="33a38-152">Identyfikator rejestracji indywidualnej.</span><span class="sxs-lookup"><span data-stu-id="33a38-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="33a38-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="33a38-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="33a38-154">Dane urządzenia do obsługi przy ponownej obsłudze administracyjnej do innego centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="33a38-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="33a38-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a38-155">-ResourceGroupName</span></span>
<span data-ttu-id="33a38-156">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="33a38-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="33a38-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33a38-157">-ResourceId</span></span>
<span data-ttu-id="33a38-158">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="33a38-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="33a38-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="33a38-159">-RootCertificate</span></span>
<span data-ttu-id="33a38-160">Przełącz się, aby zaktualizować usługi X509attastation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="33a38-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="33a38-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="33a38-161">-SecondaryCAName</span></span>
<span data-ttu-id="33a38-162">Nazwa pomocniczego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="33a38-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="33a38-163">Jeśli wymagane jest poświadczenie za pomocą certyfikatu głównego urzędu certyfikacji, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="33a38-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="33a38-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="33a38-164">-SecondaryCertificate</span></span>
<span data-ttu-id="33a38-165">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="33a38-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="33a38-166">Reprezentacja pliku cer certyfikatu X509 lub ścieżki pliku pem o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="33a38-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="33a38-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="33a38-167">-SecondaryKey</span></span>
<span data-ttu-id="33a38-168">Pomocniczy symetryczny klucz dostępu współużytkowany przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="33a38-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="33a38-169">- StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="33a38-169">-StorageRootKey</span></span>
<span data-ttu-id="33a38-170">Klucz główny magazynu DLA urządzenia TPM.</span><span class="sxs-lookup"><span data-stu-id="33a38-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="33a38-171">— Tag</span><span class="sxs-lookup"><span data-stu-id="33a38-171">-Tag</span></span>
<span data-ttu-id="33a38-172">Początkowe tagi tagi tagów.</span><span class="sxs-lookup"><span data-stu-id="33a38-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="33a38-173">- WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="33a38-173">-WebhookUrl</span></span>
<span data-ttu-id="33a38-174">Adres URL webhook używany dla niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="33a38-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="33a38-175">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33a38-175">-Confirm</span></span>
<span data-ttu-id="33a38-176">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33a38-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a38-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a38-177">-WhatIf</span></span>
<span data-ttu-id="33a38-178">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a38-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a38-179">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="33a38-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a38-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a38-180">CommonParameters</span></span>
<span data-ttu-id="33a38-181">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a38-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a38-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a38-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a38-183">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a38-183">INPUTS</span></span>

### <span data-ttu-id="33a38-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="33a38-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="33a38-185">System.String</span><span class="sxs-lookup"><span data-stu-id="33a38-185">System.String</span></span>

## <span data-ttu-id="33a38-186">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a38-186">OUTPUTS</span></span>

### <span data-ttu-id="33a38-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="33a38-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="33a38-188">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33a38-188">NOTES</span></span>

## <span data-ttu-id="33a38-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33a38-189">RELATED LINKS</span></span>
