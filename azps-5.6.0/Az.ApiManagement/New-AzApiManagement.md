---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 79387b634bc42a4885139db35ad68a9145c02dba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009434"
---
# <span data-ttu-id="9f50a-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-101">New-AzApiManagement</span></span>

## <span data-ttu-id="9f50a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f50a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f50a-103">Tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9f50a-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="9f50a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9f50a-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f50a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9f50a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f50a-106">Polecenie **cmdlet New-AzApiManagement** tworzy wdrożenie zarządzania interfejsami API w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9f50a-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="9f50a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9f50a-107">EXAMPLES</span></span>

### <span data-ttu-id="9f50a-108">Przykład 1. Tworzenie usługi zarządzania interfejsami API warstwy deweloperskiej</span><span class="sxs-lookup"><span data-stu-id="9f50a-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="9f50a-109">To polecenie tworzy usługę zarządzania interfejsami API warstwy dewelopera.</span><span class="sxs-lookup"><span data-stu-id="9f50a-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="9f50a-110">To polecenie określa adres organizacji i administratora.</span><span class="sxs-lookup"><span data-stu-id="9f50a-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="9f50a-111">To polecenie nie określa *parametru SKU.*</span><span class="sxs-lookup"><span data-stu-id="9f50a-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="9f50a-112">Dlatego polecenie cmdlet używa wartości domyślnej Deweloper.</span><span class="sxs-lookup"><span data-stu-id="9f50a-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="9f50a-113">Przykład 2. Tworzenie usługi warstwy standardowej, która ma trzy jednostki</span><span class="sxs-lookup"><span data-stu-id="9f50a-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="9f50a-114">To polecenie tworzy usługę zarządzania interfejsami API warstwy standardowej, która ma trzy jednostki.</span><span class="sxs-lookup"><span data-stu-id="9f50a-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="9f50a-115">Przykład 3. Tworzenie usługi warstwy Zużycia</span><span class="sxs-lookup"><span data-stu-id="9f50a-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

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

<span data-ttu-id="9f50a-116">To polecenie tworzy usługę zarządzania interfejsami API warstwy zużycia z włączonym certyfikatem klienta w Europie Zachodniej.</span><span class="sxs-lookup"><span data-stu-id="9f50a-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="9f50a-117">Przykład 4. Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9f50a-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="9f50a-118">To polecenie tworzy usługę zarządzania interfejsami API premium w podsieci sieci wirtualnej platformy Azure, która ma zewnętrzny punkt końcowy bramy z regionem głównym w Zachód.</span><span class="sxs-lookup"><span data-stu-id="9f50a-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="9f50a-119">Przykład 5. Tworzenie usługi zarządzania interfejsem API dla wewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9f50a-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="9f50a-120">To polecenie tworzy usługę zarządzania interfejsami API premium w podsieci sieci wirtualnej platformy Azure, która ma wewnętrzny punkt końcowy bramy z regionem głównym w Zachód Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="9f50a-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="9f50a-121">Przykład 6. Tworzenie usługi zarządzania interfejsem API i włączanie protokołu TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="9f50a-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
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

<span data-ttu-id="9f50a-122">To polecenie tworzy standardową usługę zarządzania interfejsami API SKU i włącz standard TLS 1.0 w kliencie frontendu do bramy ApiManagement i klienta zaplecza między bramą ApiManagement a zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9f50a-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="9f50a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f50a-123">PARAMETERS</span></span>

### <span data-ttu-id="9f50a-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="9f50a-124">-AdditionalRegions</span></span>
<span data-ttu-id="9f50a-125">Dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9f50a-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="9f50a-126">- AdminEmail</span><span class="sxs-lookup"><span data-stu-id="9f50a-126">-AdminEmail</span></span>
<span data-ttu-id="9f50a-127">Określa adres e-mail dla wszystkich powiadomień, które wysyła system zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="9f50a-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="9f50a-128">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="9f50a-128">-Capacity</span></span>
<span data-ttu-id="9f50a-129">Określa pojemność sku usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9f50a-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="9f50a-130">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="9f50a-130">The default is one (1).</span></span>

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

### <span data-ttu-id="9f50a-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f50a-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="9f50a-132">Niestandardowe konfiguracje nazw hostów.</span><span class="sxs-lookup"><span data-stu-id="9f50a-132">Custom hostname configurations.</span></span> <span data-ttu-id="9f50a-133">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="9f50a-133">Default value is $null.</span></span> <span data-ttu-id="9f50a-134">Przekazanie $null ustawi domyślną nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="9f50a-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="9f50a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f50a-135">-DefaultProfile</span></span>
<span data-ttu-id="9f50a-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f50a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f50a-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9f50a-137">-EnableClientCertificate</span></span>
<span data-ttu-id="9f50a-138">Flaga ma być używana tylko dla usługi ApiManagement SKU zużycia.</span><span class="sxs-lookup"><span data-stu-id="9f50a-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="9f50a-139">Wymusza to prezentowania certyfikatu klienta dla każdego żądania bramy.</span><span class="sxs-lookup"><span data-stu-id="9f50a-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="9f50a-140">Umożliwia to również uwierzytelnienie certyfikatu w zasadach bramy.</span><span class="sxs-lookup"><span data-stu-id="9f50a-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="9f50a-141">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9f50a-141">-Location</span></span>
<span data-ttu-id="9f50a-142">Określa lokalizację tworzenia usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="9f50a-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="9f50a-143">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | gdzie {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object lokalizacji</span><span class="sxs-lookup"><span data-stu-id="9f50a-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="9f50a-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9f50a-144">-Name</span></span>
<span data-ttu-id="9f50a-145">Określa nazwę wdrożenia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9f50a-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="9f50a-146">— Organizacja</span><span class="sxs-lookup"><span data-stu-id="9f50a-146">-Organization</span></span>
<span data-ttu-id="9f50a-147">Określa nazwę organizacji.</span><span class="sxs-lookup"><span data-stu-id="9f50a-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="9f50a-148">Zarządzanie interfejsem API używa tego adresu w portalu dewelopera w powiadomieniach e-mail.</span><span class="sxs-lookup"><span data-stu-id="9f50a-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="9f50a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f50a-149">-ResourceGroupName</span></span>
<span data-ttu-id="9f50a-150">Określa nazwę grupy zasobów, w ramach której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9f50a-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="9f50a-151">- SKU</span><span class="sxs-lookup"><span data-stu-id="9f50a-151">-Sku</span></span>
<span data-ttu-id="9f50a-152">Określa warstwę usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="9f50a-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="9f50a-153">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="9f50a-153">Valid values are:</span></span> 
- <span data-ttu-id="9f50a-154">Deweloper</span><span class="sxs-lookup"><span data-stu-id="9f50a-154">Developer</span></span> 
- <span data-ttu-id="9f50a-155">Standardowe</span><span class="sxs-lookup"><span data-stu-id="9f50a-155">Standard</span></span> 
- <span data-ttu-id="9f50a-156">Premium Domyślnie jest to Deweloper.</span><span class="sxs-lookup"><span data-stu-id="9f50a-156">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="9f50a-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="9f50a-157">-SslSetting</span></span>
<span data-ttu-id="9f50a-158">Ustawienie ssl usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9f50a-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="9f50a-159">Wartość domyślna to $null</span><span class="sxs-lookup"><span data-stu-id="9f50a-159">Default value is $null</span></span>

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

### <span data-ttu-id="9f50a-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9f50a-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="9f50a-161">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9f50a-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9f50a-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f50a-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="9f50a-163">Certyfikaty wystawione przez wewnętrzny urząd certyfikacji do zainstalowania w usłudze.</span><span class="sxs-lookup"><span data-stu-id="9f50a-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="9f50a-164">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="9f50a-164">Default value is $null.</span></span>

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

### <span data-ttu-id="9f50a-165">— Tag</span><span class="sxs-lookup"><span data-stu-id="9f50a-165">-Tag</span></span>
<span data-ttu-id="9f50a-166">Słownik tagów.</span><span class="sxs-lookup"><span data-stu-id="9f50a-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="9f50a-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9f50a-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="9f50a-168">Przypisz tożsamości użytkowników do tego serwera do używania z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9f50a-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f50a-169">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f50a-169">-VirtualNetwork</span></span>
<span data-ttu-id="9f50a-170">Virtual Network Configuration of master Azure API Management deployment region.</span><span class="sxs-lookup"><span data-stu-id="9f50a-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="9f50a-171">- VpnType</span><span class="sxs-lookup"><span data-stu-id="9f50a-171">-VpnType</span></span>
<span data-ttu-id="9f50a-172">Virtual Network Type of the ApiManagement Deployment.</span><span class="sxs-lookup"><span data-stu-id="9f50a-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="9f50a-173">Prawidłowe wartości to</span><span class="sxs-lookup"><span data-stu-id="9f50a-173">Valid Values are</span></span> 
- <span data-ttu-id="9f50a-174">"Brak" (wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="9f50a-174">"None" (Default Value.</span></span> <span data-ttu-id="9f50a-175">ApiManagement nie jest częścią żadnej sieci wirtualnej")</span><span class="sxs-lookup"><span data-stu-id="9f50a-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="9f50a-176">"Zewnętrzny" (wdrożenie apiManagement jest konfigurowanie wewnątrz sieci wirtualnej mającej punkt końcowy skierowany do Internetu)</span><span class="sxs-lookup"><span data-stu-id="9f50a-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="9f50a-177">"Wewnętrzny" (Wdrożenie zarządzania interfejsem API jest konfigurowanie wewnątrz sieci wirtualnej, która ma punkt końcowy skierowany do intranetu)</span><span class="sxs-lookup"><span data-stu-id="9f50a-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="9f50a-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f50a-178">CommonParameters</span></span>
<span data-ttu-id="9f50a-179">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f50a-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f50a-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f50a-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f50a-181">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f50a-181">INPUTS</span></span>

### <span data-ttu-id="9f50a-182">System.String</span><span class="sxs-lookup"><span data-stu-id="9f50a-182">System.String</span></span>

### <span data-ttu-id="9f50a-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9f50a-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9f50a-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f50a-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9f50a-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f50a-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="9f50a-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f50a-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9f50a-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="9f50a-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="9f50a-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="9f50a-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="9f50a-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="9f50a-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="9f50a-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f50a-190">OUTPUTS</span></span>

### <span data-ttu-id="9f50a-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9f50a-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9f50a-192">NOTES</span></span>

## <span data-ttu-id="9f50a-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f50a-193">RELATED LINKS</span></span>

[<span data-ttu-id="9f50a-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="9f50a-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="9f50a-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="9f50a-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="9f50a-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9f50a-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


