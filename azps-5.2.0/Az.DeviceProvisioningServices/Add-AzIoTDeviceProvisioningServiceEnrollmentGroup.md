---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340978"
---
# <span data-ttu-id="65571-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="65571-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="65571-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65571-102">SYNOPSIS</span></span>
<span data-ttu-id="65571-103">Utwórz grupę rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="65571-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="65571-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65571-104">SYNTAX</span></span>

### <span data-ttu-id="65571-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65571-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65571-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65571-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65571-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="65571-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65571-108">Opis</span><span class="sxs-lookup"><span data-stu-id="65571-108">DESCRIPTION</span></span>
<span data-ttu-id="65571-109">Utwórz grupę rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="65571-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="65571-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65571-110">EXAMPLES</span></span>

### <span data-ttu-id="65571-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65571-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="65571-112">Tworzenie rejestracji przy użyciu typu zaświadczania SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="65571-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="65571-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="65571-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="65571-114">Tworzenie rejestracji z typem zaświadczania — x509</span><span class="sxs-lookup"><span data-stu-id="65571-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="65571-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="65571-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="65571-116">Tworzenie rejestracji przy użyciu typu zaświadczania o typie SymmetricKey oraz początkowym stanie sznurka.</span><span class="sxs-lookup"><span data-stu-id="65571-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="65571-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65571-117">PARAMETERS</span></span>

### <span data-ttu-id="65571-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="65571-118">-AllocationPolicy</span></span>
<span data-ttu-id="65571-119">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="65571-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="65571-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65571-120">-ApiVersion</span></span>
<span data-ttu-id="65571-121">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="65571-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="65571-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="65571-122">-AttestationType</span></span>
<span data-ttu-id="65571-123">Mechanizm zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="65571-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="65571-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65571-124">-DefaultProfile</span></span>
<span data-ttu-id="65571-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65571-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65571-126">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="65571-126">-Desired</span></span>
<span data-ttu-id="65571-127">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="65571-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="65571-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="65571-128">-DpsName</span></span>
<span data-ttu-id="65571-129">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="65571-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="65571-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="65571-130">-DpsObject</span></span>
<span data-ttu-id="65571-131">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="65571-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="65571-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="65571-132">-EdgeEnabled</span></span>
<span data-ttu-id="65571-133">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="65571-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="65571-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="65571-134">-IotHub</span></span>
<span data-ttu-id="65571-135">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="65571-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="65571-136">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="65571-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="65571-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="65571-137">-IotHubHostName</span></span>
<span data-ttu-id="65571-138">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="65571-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="65571-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65571-139">-Name</span></span>
<span data-ttu-id="65571-140">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="65571-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="65571-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="65571-141">-PrimaryCAName</span></span>
<span data-ttu-id="65571-142">Nazwa głównego certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="65571-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="65571-143">Jeśli zaświadczenie z certyfikatem głównego urzędu certyfikacji jest wymagane, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="65571-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="65571-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="65571-144">-PrimaryCertificate</span></span>
<span data-ttu-id="65571-145">Ścieżka do pliku zawierającego podstawowy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="65571-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="65571-146">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="65571-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="65571-147">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="65571-147">-PrimaryKey</span></span>
<span data-ttu-id="65571-148">Podstawowy symetryczny kluczowy dostęp współdzielony, przechowywany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="65571-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="65571-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="65571-149">-ProvisioningStatus</span></span>
<span data-ttu-id="65571-150">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="65571-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="65571-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="65571-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="65571-152">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="65571-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="65571-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65571-153">-ResourceGroupName</span></span>
<span data-ttu-id="65571-154">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="65571-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="65571-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65571-155">-ResourceId</span></span>
<span data-ttu-id="65571-156">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="65571-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="65571-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="65571-157">-RootCertificate</span></span>
<span data-ttu-id="65571-158">Umożliwia tworzenie X509attestation przy użyciu certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="65571-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="65571-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="65571-159">-SecondaryCAName</span></span>
<span data-ttu-id="65571-160">Nazwa certyfikatu pomocniczego głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="65571-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="65571-161">Jeśli zaświadczenie z certyfikatem głównego urzędu certyfikacji jest wymagane, należy podać nazwę głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="65571-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="65571-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="65571-162">-SecondaryCertificate</span></span>
<span data-ttu-id="65571-163">Ścieżka do pliku zawierającego certyfikat pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="65571-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="65571-164">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="65571-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="65571-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="65571-165">-SecondaryKey</span></span>
<span data-ttu-id="65571-166">Pomocniczy, symetryczny klucz dostępu współdzielony zapisany w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="65571-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="65571-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="65571-167">-Tag</span></span>
<span data-ttu-id="65571-168">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="65571-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="65571-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="65571-169">-WebhookUrl</span></span>
<span data-ttu-id="65571-170">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="65571-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="65571-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65571-171">-Confirm</span></span>
<span data-ttu-id="65571-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65571-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65571-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65571-173">-WhatIf</span></span>
<span data-ttu-id="65571-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65571-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65571-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65571-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65571-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65571-176">CommonParameters</span></span>
<span data-ttu-id="65571-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65571-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65571-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65571-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65571-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65571-179">INPUTS</span></span>

### <span data-ttu-id="65571-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="65571-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="65571-181">System. String</span><span class="sxs-lookup"><span data-stu-id="65571-181">System.String</span></span>

## <span data-ttu-id="65571-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65571-182">OUTPUTS</span></span>

### <span data-ttu-id="65571-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="65571-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="65571-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65571-184">NOTES</span></span>

## <span data-ttu-id="65571-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65571-185">RELATED LINKS</span></span>
