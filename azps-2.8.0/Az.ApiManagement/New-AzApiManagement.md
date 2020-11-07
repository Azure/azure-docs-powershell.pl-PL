---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 489df2abd46f3ec198422991c2627804f6dc140b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707046"
---
# <span data-ttu-id="cd03a-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-101">New-AzApiManagement</span></span>

## <span data-ttu-id="cd03a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd03a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd03a-103">Tworzenie wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="cd03a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd03a-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-AssignIdentity] [-EnableClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd03a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd03a-105">DESCRIPTION</span></span>
<span data-ttu-id="cd03a-106">Polecenie cmdlet **New-AzApiManagement** tworzy wdrożenie zarządzania interfejsem API w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="cd03a-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="cd03a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd03a-107">EXAMPLES</span></span>

### <span data-ttu-id="cd03a-108">Przykład 1: Tworzenie usługi zarządzania interfejsem API dla warstwy dewelopera</span><span class="sxs-lookup"><span data-stu-id="cd03a-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="cd03a-109">To polecenie tworzy usługę zarządzania interfejsem API warstwy dewelopera.</span><span class="sxs-lookup"><span data-stu-id="cd03a-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="cd03a-110">Polecenie określa nazwę organizacji i adres administratora.</span><span class="sxs-lookup"><span data-stu-id="cd03a-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="cd03a-111">Polecenie nie określa parametru *SKU* .</span><span class="sxs-lookup"><span data-stu-id="cd03a-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="cd03a-112">Dlatego polecenie cmdlet używa domyślnej wartości dewelopera.</span><span class="sxs-lookup"><span data-stu-id="cd03a-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="cd03a-113">Przykład 2: Tworzenie usługi warstwy standardowej zawierającej trzy jednostki</span><span class="sxs-lookup"><span data-stu-id="cd03a-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="cd03a-114">To polecenie tworzy standardową usługę zarządzania interfejsem API o trzech jednostkach.</span><span class="sxs-lookup"><span data-stu-id="cd03a-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="cd03a-115">Przykład 3: Tworzenie usługi warstwy zużycia</span><span class="sxs-lookup"><span data-stu-id="cd03a-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -AssignIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="cd03a-116">To polecenie tworzy usługę zarządzania interfejsem API warstwy zużycia z certyfikatem klienta włączonym w zachodniej Europie.</span><span class="sxs-lookup"><span data-stu-id="cd03a-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="cd03a-117">Przykład 4: Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cd03a-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="cd03a-118">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z zewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="cd03a-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="cd03a-119">Przykład 5: Tworzenie usługi zarządzania interfejsem API dla wewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cd03a-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="cd03a-120">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z wewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="cd03a-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="cd03a-121">Przykład 6: Tworzenie usługi zarządzania interfejsem API i włączanie protokołu TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="cd03a-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="cd03a-122">To polecenie tworzy standardową usługę zarządzania interfejsem API i włączy protokół TLS 1,0 na kliencie frontonu, aby ApiManagement bramę i klienta zaplecza między bramą ApiManagement i zapleczem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="cd03a-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="cd03a-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd03a-123">PARAMETERS</span></span>

### <span data-ttu-id="cd03a-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="cd03a-124">-AdditionalRegions</span></span>
<span data-ttu-id="cd03a-125">Dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="cd03a-125">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="cd03a-126">-AdminEmail</span></span>
<span data-ttu-id="cd03a-127">Określa źródłowy adres e-mail dla wszystkich powiadomień wysyłanych przez system zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-128">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd03a-128">-AssignIdentity</span></span>
<span data-ttu-id="cd03a-129">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd03a-129">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="cd03a-130">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="cd03a-130">-Capacity</span></span>
<span data-ttu-id="cd03a-131">Określa pojemność jednostki SKU usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-131">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="cd03a-132">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="cd03a-132">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-133">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd03a-133">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="cd03a-134">Niestandardowe konfiguracje nazw hostów.</span><span class="sxs-lookup"><span data-stu-id="cd03a-134">Custom hostname configurations.</span></span> <span data-ttu-id="cd03a-135">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="cd03a-135">Default value is $null.</span></span> <span data-ttu-id="cd03a-136">Przekazanie $null spowoduje ustawienie domyślnej nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="cd03a-136">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd03a-137">-DefaultProfile</span></span>
<span data-ttu-id="cd03a-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd03a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd03a-139">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cd03a-139">-EnableClientCertificate</span></span>
<span data-ttu-id="cd03a-140">Flaga przeznaczona tylko do użytku w usłudze ApiManagement SKU.</span><span class="sxs-lookup"><span data-stu-id="cd03a-140">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="cd03a-141">Wymusza to, że certyfikat klienta jest prezentowany na każdej prośbie do bramy.</span><span class="sxs-lookup"><span data-stu-id="cd03a-141">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="cd03a-142">Umożliwia także uwierzytelnianie certyfikatu w zasadach w bramie.</span><span class="sxs-lookup"><span data-stu-id="cd03a-142">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="cd03a-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cd03a-143">-Location</span></span>
<span data-ttu-id="cd03a-144">Określa lokalizację, w której ma zostać utworzona usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-144">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="cd03a-145">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="cd03a-145">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd03a-146">-Name</span></span>
<span data-ttu-id="cd03a-147">Określa nazwę wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-147">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-148">— Organizacja</span><span class="sxs-lookup"><span data-stu-id="cd03a-148">-Organization</span></span>
<span data-ttu-id="cd03a-149">Określa nazwę organizacji.</span><span class="sxs-lookup"><span data-stu-id="cd03a-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="cd03a-150">Funkcja zarządzania interfejsem API używa tego adresu w portalu dewelopera w obszarze powiadomienia e-mail.</span><span class="sxs-lookup"><span data-stu-id="cd03a-150">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd03a-151">-ResourceGroupName</span></span>
<span data-ttu-id="cd03a-152">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd03a-153">-Sku</span></span>
<span data-ttu-id="cd03a-154">Określa warstwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="cd03a-155">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="cd03a-155">Valid values are:</span></span> 
- <span data-ttu-id="cd03a-156">Deweloper</span><span class="sxs-lookup"><span data-stu-id="cd03a-156">Developer</span></span> 
- <span data-ttu-id="cd03a-157">Standard</span><span class="sxs-lookup"><span data-stu-id="cd03a-157">Standard</span></span> 
- <span data-ttu-id="cd03a-158">Premium domyślnym jest deweloper.</span><span class="sxs-lookup"><span data-stu-id="cd03a-158">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-159">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="cd03a-159">-SslSetting</span></span>
<span data-ttu-id="cd03a-160">Ustawienie protokołu SSL usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cd03a-160">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="cd03a-161">Wartość domyślna to $null</span><span class="sxs-lookup"><span data-stu-id="cd03a-161">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd03a-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="cd03a-163">Certyfikaty wystawione przez wewnętrzny urząd certyfikacji do zainstalowania w usłudze.</span><span class="sxs-lookup"><span data-stu-id="cd03a-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="cd03a-164">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="cd03a-164">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd03a-165">-Tag</span></span>
<span data-ttu-id="cd03a-166">Słownik znaczników.</span><span class="sxs-lookup"><span data-stu-id="cd03a-166">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-167">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd03a-167">-VirtualNetwork</span></span>
<span data-ttu-id="cd03a-168">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania interfejsem głównym usługi Azure API.</span><span class="sxs-lookup"><span data-stu-id="cd03a-168">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-169">-VpnType</span><span class="sxs-lookup"><span data-stu-id="cd03a-169">-VpnType</span></span>
<span data-ttu-id="cd03a-170">Typ sieci wirtualnej wdrożenia ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cd03a-170">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="cd03a-171">Prawidłowe wartości to</span><span class="sxs-lookup"><span data-stu-id="cd03a-171">Valid Values are</span></span> 
- <span data-ttu-id="cd03a-172">"Brak" (wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="cd03a-172">"None" (Default Value.</span></span> <span data-ttu-id="cd03a-173">ApiManagement nie jest częścią żadnej sieci wirtualnej ")</span><span class="sxs-lookup"><span data-stu-id="cd03a-173">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="cd03a-174">"Zewnętrzne" (ApiManagement wdrożenie to konfiguracja w sieci wirtualnej z internetowym punktem końcowym)</span><span class="sxs-lookup"><span data-stu-id="cd03a-174">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="cd03a-175">"Internal" (ApiManagement Deployment to Setup w sieci wirtualnej z punktem końcowym w intranecie)</span><span class="sxs-lookup"><span data-stu-id="cd03a-175">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd03a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd03a-176">CommonParameters</span></span>
<span data-ttu-id="cd03a-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd03a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd03a-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd03a-178">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd03a-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd03a-179">INPUTS</span></span>

### <span data-ttu-id="cd03a-180">System. String</span><span class="sxs-lookup"><span data-stu-id="cd03a-180">System.String</span></span>

### <span data-ttu-id="cd03a-181">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. MODELES. PsApiManagementSku, Microsoft. Azure. PowerShell. cmdlet. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cd03a-181">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cd03a-182">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cd03a-182">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cd03a-183">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd03a-183">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="cd03a-184">System. Collections. Generic. dictionary ' 2 [[System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = 7cec85d7bea7798e], [System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cd03a-184">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cd03a-185">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="cd03a-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="cd03a-186">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="cd03a-186">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="cd03a-187">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="cd03a-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="cd03a-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd03a-188">OUTPUTS</span></span>

### <span data-ttu-id="cd03a-189">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cd03a-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd03a-190">NOTES</span></span>

## <span data-ttu-id="cd03a-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd03a-191">RELATED LINKS</span></span>

[<span data-ttu-id="cd03a-192">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-192">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="cd03a-193">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-193">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="cd03a-194">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-194">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="cd03a-195">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-195">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="cd03a-196">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd03a-196">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


