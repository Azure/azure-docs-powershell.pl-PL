---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 6d6253b338bef04c39032bb29b5fb0ba300f4073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868400"
---
# <span data-ttu-id="d242c-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d242c-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="d242c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d242c-102">SYNOPSIS</span></span>
<span data-ttu-id="d242c-103">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="d242c-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d242c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d242c-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d242c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d242c-105">DESCRIPTION</span></span>
<span data-ttu-id="d242c-106">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="d242c-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d242c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d242c-107">EXAMPLES</span></span>

### <span data-ttu-id="d242c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d242c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="d242c-109">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="d242c-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d242c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d242c-110">PARAMETERS</span></span>

### <span data-ttu-id="d242c-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="d242c-111">-CertificateSource</span></span>
<span data-ttu-id="d242c-112">Źródło certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="d242c-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d242c-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="d242c-113">-CertificateType</span></span>
<span data-ttu-id="d242c-114">Typ certyfikatu służący do bezpiecznego połączenia z usługą frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d242c-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d242c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d242c-115">-DefaultProfile</span></span>
<span data-ttu-id="d242c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d242c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d242c-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="d242c-117">-HostName</span></span>
<span data-ttu-id="d242c-118">Nazwa hosta frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d242c-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="d242c-119">Musi być nazwą domeny.</span><span class="sxs-lookup"><span data-stu-id="d242c-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="d242c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d242c-120">-Name</span></span>
<span data-ttu-id="d242c-121">Nazwa punktu końcowego frontonu.</span><span class="sxs-lookup"><span data-stu-id="d242c-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="d242c-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="d242c-122">-ProtocolType</span></span>
<span data-ttu-id="d242c-123">Protokół rozszerzeń TLS, który jest wykorzystywany do zabezpieczania dostarczania</span><span class="sxs-lookup"><span data-stu-id="d242c-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d242c-124">-Secretname</span><span class="sxs-lookup"><span data-stu-id="d242c-124">-SecretName</span></span>
<span data-ttu-id="d242c-125">Nazwa tajnego magazynu kluczy reprezentującego pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="d242c-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d242c-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="d242c-126">-SecretVersion</span></span>
<span data-ttu-id="d242c-127">Wersja tajnego magazynu kluczy reprezentującego pełną PFX certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d242c-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d242c-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="d242c-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="d242c-129">Czy zezwolić na koligację sesji na tym hoście.</span><span class="sxs-lookup"><span data-stu-id="d242c-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="d242c-130">Wartość domyślna jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="d242c-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="d242c-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d242c-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="d242c-132">Czas wygaśnięcia (TTL) używany w sekundach dla koligacji sesji (jeśli ma zastosowanie).</span><span class="sxs-lookup"><span data-stu-id="d242c-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="d242c-133">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="d242c-133">Default value is 0</span></span>

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

### <span data-ttu-id="d242c-134">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="d242c-134">-Vault</span></span>
<span data-ttu-id="d242c-135">Magazyn kluczy zawierający certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="d242c-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="d242c-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="d242c-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="d242c-137">Identyfikator zasobu zasad zapory aplikacji sieci Web dla każdego hosta (jeśli ma zastosowanie)</span><span class="sxs-lookup"><span data-stu-id="d242c-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="d242c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d242c-138">CommonParameters</span></span>
<span data-ttu-id="d242c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d242c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d242c-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d242c-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d242c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d242c-141">INPUTS</span></span>

### <span data-ttu-id="d242c-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d242c-142">None</span></span>

## <span data-ttu-id="d242c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d242c-143">OUTPUTS</span></span>

### <span data-ttu-id="d242c-144">Microsoft. Azure. Commands. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d242c-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="d242c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d242c-145">NOTES</span></span>

## <span data-ttu-id="d242c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d242c-146">RELATED LINKS</span></span>

<span data-ttu-id="d242c-147">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d242c-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
