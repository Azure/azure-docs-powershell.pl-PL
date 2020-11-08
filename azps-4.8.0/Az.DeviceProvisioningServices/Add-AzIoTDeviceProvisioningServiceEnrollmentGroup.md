---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062774"
---
# <span data-ttu-id="547c5-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="547c5-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="547c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="547c5-102">SYNOPSIS</span></span>
<span data-ttu-id="547c5-103">Utwórz grupę rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="547c5-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="547c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="547c5-104">SYNTAX</span></span>

### <span data-ttu-id="547c5-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="547c5-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="547c5-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="547c5-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="547c5-108">DESCRIPTION</span></span>
<span data-ttu-id="547c5-109">Utwórz grupę rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="547c5-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="547c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="547c5-110">EXAMPLES</span></span>

### <span data-ttu-id="547c5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="547c5-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="547c5-112">Tworzenie rejestracji przy użyciu typu zaświadczania SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="547c5-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="547c5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="547c5-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="547c5-114">Tworzenie rejestracji z typem zaświadczania — x509</span><span class="sxs-lookup"><span data-stu-id="547c5-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="547c5-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="547c5-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="547c5-116">Tworzenie rejestracji przy użyciu typu zaświadczania o typie SymmetricKey oraz początkowym stanie sznurka.</span><span class="sxs-lookup"><span data-stu-id="547c5-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="547c5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="547c5-117">PARAMETERS</span></span>

### <span data-ttu-id="547c5-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="547c5-118">-AllocationPolicy</span></span>
<span data-ttu-id="547c5-119">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="547c5-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="547c5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="547c5-120">-ApiVersion</span></span>
<span data-ttu-id="547c5-121">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="547c5-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="547c5-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="547c5-122">-AttestationType</span></span>
<span data-ttu-id="547c5-123">Mechanizm zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="547c5-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="547c5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547c5-124">-DefaultProfile</span></span>
<span data-ttu-id="547c5-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="547c5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="547c5-126">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="547c5-126">-Desired</span></span>
<span data-ttu-id="547c5-127">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="547c5-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="547c5-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="547c5-128">-DpsName</span></span>
<span data-ttu-id="547c5-129">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="547c5-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="547c5-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="547c5-130">-DpsObject</span></span>
<span data-ttu-id="547c5-131">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="547c5-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="547c5-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="547c5-132">-EdgeEnabled</span></span>
<span data-ttu-id="547c5-133">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="547c5-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="547c5-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="547c5-134">-IotHub</span></span>
<span data-ttu-id="547c5-135">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="547c5-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="547c5-136">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="547c5-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="547c5-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="547c5-137">-IotHubHostName</span></span>
<span data-ttu-id="547c5-138">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="547c5-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="547c5-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="547c5-139">-Name</span></span>
<span data-ttu-id="547c5-140">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="547c5-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="547c5-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="547c5-141">-PrimaryCAName</span></span>
<span data-ttu-id="547c5-142">Nazwa głównego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="547c5-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="547c5-143">Jeśli zaświadczenie z certyfikatem głównego urzędu certyfikacji jest wymagane, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="547c5-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="547c5-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="547c5-144">-PrimaryCertificate</span></span>
<span data-ttu-id="547c5-145">Ścieżka do pliku zawierającego podstawowy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="547c5-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="547c5-146">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="547c5-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="547c5-147">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="547c5-147">-PrimaryKey</span></span>
<span data-ttu-id="547c5-148">Podstawowy symetryczny kluczowy dostęp współdzielony, przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="547c5-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="547c5-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="547c5-149">-ProvisioningStatus</span></span>
<span data-ttu-id="547c5-150">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="547c5-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="547c5-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="547c5-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="547c5-152">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="547c5-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="547c5-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547c5-153">-ResourceGroupName</span></span>
<span data-ttu-id="547c5-154">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="547c5-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="547c5-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="547c5-155">-ResourceId</span></span>
<span data-ttu-id="547c5-156">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="547c5-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="547c5-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="547c5-157">-RootCertificate</span></span>
<span data-ttu-id="547c5-158">Umożliwia tworzenie X509attestation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="547c5-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="547c5-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="547c5-159">-SecondaryCAName</span></span>
<span data-ttu-id="547c5-160">Nazwa certyfikatu pomocniczego głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="547c5-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="547c5-161">Jeśli zaświadczenie z certyfikatem głównego urzędu certyfikacji jest wymagane, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="547c5-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="547c5-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="547c5-162">-SecondaryCertificate</span></span>
<span data-ttu-id="547c5-163">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="547c5-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="547c5-164">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="547c5-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="547c5-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="547c5-165">-SecondaryKey</span></span>
<span data-ttu-id="547c5-166">Pomocniczy, symetryczny klucz dostępu współdzielony zapisany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="547c5-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="547c5-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="547c5-167">-Tag</span></span>
<span data-ttu-id="547c5-168">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="547c5-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="547c5-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="547c5-169">-WebhookUrl</span></span>
<span data-ttu-id="547c5-170">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="547c5-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="547c5-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="547c5-171">-Confirm</span></span>
<span data-ttu-id="547c5-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="547c5-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="547c5-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547c5-173">-WhatIf</span></span>
<span data-ttu-id="547c5-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="547c5-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="547c5-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="547c5-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="547c5-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547c5-176">CommonParameters</span></span>
<span data-ttu-id="547c5-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547c5-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547c5-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547c5-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547c5-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="547c5-179">INPUTS</span></span>

### <span data-ttu-id="547c5-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="547c5-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="547c5-181">System. String</span><span class="sxs-lookup"><span data-stu-id="547c5-181">System.String</span></span>

## <span data-ttu-id="547c5-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="547c5-182">OUTPUTS</span></span>

### <span data-ttu-id="547c5-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="547c5-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="547c5-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="547c5-184">NOTES</span></span>

## <span data-ttu-id="547c5-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="547c5-185">RELATED LINKS</span></span>
