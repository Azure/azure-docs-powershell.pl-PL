---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200306"
---
# <span data-ttu-id="913e6-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="913e6-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="913e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913e6-102">SYNOPSIS</span></span>
<span data-ttu-id="913e6-103">Tworzenie obiektu PSFrontendEndpoint do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="913e6-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="913e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="913e6-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="913e6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="913e6-105">DESCRIPTION</span></span>
<span data-ttu-id="913e6-106">Tworzenie obiektu PSFrontendEndpoint do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="913e6-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="913e6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="913e6-107">EXAMPLES</span></span>

### <span data-ttu-id="913e6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="913e6-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="913e6-109">Tworzenie obiektu PSFrontendEndpoint do tworzenia drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="913e6-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="913e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913e6-110">PARAMETERS</span></span>

### <span data-ttu-id="913e6-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="913e6-111">-CertificateSource</span></span>
<span data-ttu-id="913e6-112">Źródło certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="913e6-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="913e6-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="913e6-113">-CertificateType</span></span>
<span data-ttu-id="913e6-114">Typ certyfikatu używanego do bezpiecznego połączenia z frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="913e6-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="913e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913e6-115">-DefaultProfile</span></span>
<span data-ttu-id="913e6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="913e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913e6-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="913e6-117">-HostName</span></span>
<span data-ttu-id="913e6-118">Nazwa hosta frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="913e6-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="913e6-119">Musi to być nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="913e6-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="913e6-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="913e6-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="913e6-121">Minimalna wersja TLS wymagana przez klientów do nawiązania uścisku SSL z drzwiami przednimi.</span><span class="sxs-lookup"><span data-stu-id="913e6-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="913e6-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="913e6-122">-Name</span></span>
<span data-ttu-id="913e6-123">Nazwa punktu końcowego frontendu.</span><span class="sxs-lookup"><span data-stu-id="913e6-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="913e6-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="913e6-124">-ProtocolType</span></span>
<span data-ttu-id="913e6-125">Protokół rozszerzenia TLS używany do bezpiecznego dostarczania</span><span class="sxs-lookup"><span data-stu-id="913e6-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="913e6-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="913e6-126">-SecretName</span></span>
<span data-ttu-id="913e6-127">Nazwa klucza magazynu kluczy reprezentująca pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="913e6-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="913e6-128">- SecretVersion</span><span class="sxs-lookup"><span data-stu-id="913e6-128">-SecretVersion</span></span>
<span data-ttu-id="913e6-129">Wersja klucza magazynu kluczy reprezentująca pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="913e6-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="913e6-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="913e6-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="913e6-131">Czy chcesz zezwolić na chciwość sesji na tym hoście.</span><span class="sxs-lookup"><span data-stu-id="913e6-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="913e6-132">Wartość domyślna jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="913e6-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913e6-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="913e6-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="913e6-134">TTL to use in seconds for session affinity, if applicable.</span><span class="sxs-lookup"><span data-stu-id="913e6-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="913e6-135">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="913e6-135">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913e6-136">— magazyn</span><span class="sxs-lookup"><span data-stu-id="913e6-136">-Vault</span></span>
<span data-ttu-id="913e6-137">Magazyn kluczy zawierający certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="913e6-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="913e6-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="913e6-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="913e6-139">Identyfikator zasobu zasad Zapory aplikacji sieci Web dla każdego hosta (jeśli ma zastosowanie)</span><span class="sxs-lookup"><span data-stu-id="913e6-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="913e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913e6-140">CommonParameters</span></span>
<span data-ttu-id="913e6-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913e6-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="913e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913e6-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="913e6-143">INPUTS</span></span>

### <span data-ttu-id="913e6-144">Brak</span><span class="sxs-lookup"><span data-stu-id="913e6-144">None</span></span>
## <span data-ttu-id="913e6-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="913e6-145">OUTPUTS</span></span>

### <span data-ttu-id="913e6-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="913e6-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="913e6-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="913e6-147">NOTES</span></span>

## <span data-ttu-id="913e6-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="913e6-148">RELATED LINKS</span></span>

<span data-ttu-id="913e6-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="913e6-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
