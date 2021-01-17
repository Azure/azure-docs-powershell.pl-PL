---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326429"
---
# <span data-ttu-id="21a9c-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="21a9c-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="21a9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="21a9c-103">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="21a9c-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="21a9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21a9c-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a9c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="21a9c-106">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="21a9c-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="21a9c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="21a9c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21a9c-108">Example 1</span></span>
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

<span data-ttu-id="21a9c-109">Utwórz obiekt PSFrontendEndpoint do tworzenia przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="21a9c-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="21a9c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="21a9c-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="21a9c-111">-CertificateSource</span></span>
<span data-ttu-id="21a9c-112">Źródło certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="21a9c-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="21a9c-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="21a9c-113">-CertificateType</span></span>
<span data-ttu-id="21a9c-114">Typ certyfikatu służący do bezpiecznego połączenia z usługą frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="21a9c-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="21a9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a9c-115">-DefaultProfile</span></span>
<span data-ttu-id="21a9c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21a9c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a9c-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="21a9c-117">-HostName</span></span>
<span data-ttu-id="21a9c-118">Nazwa hosta frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="21a9c-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="21a9c-119">Musi być nazwą domeny.</span><span class="sxs-lookup"><span data-stu-id="21a9c-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="21a9c-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="21a9c-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="21a9c-121">Minimalna wersja protokołu TLS wymagana od klientów w celu ustanowienia uzgodnienia SSL z przednim Drzwiem.</span><span class="sxs-lookup"><span data-stu-id="21a9c-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="21a9c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21a9c-122">-Name</span></span>
<span data-ttu-id="21a9c-123">Nazwa punktu końcowego frontonu.</span><span class="sxs-lookup"><span data-stu-id="21a9c-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="21a9c-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="21a9c-124">-ProtocolType</span></span>
<span data-ttu-id="21a9c-125">Protokół rozszerzeń TLS, który jest wykorzystywany do zabezpieczania dostarczania</span><span class="sxs-lookup"><span data-stu-id="21a9c-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="21a9c-126">-Secretname</span><span class="sxs-lookup"><span data-stu-id="21a9c-126">-SecretName</span></span>
<span data-ttu-id="21a9c-127">Nazwa tajnego magazynu kluczy reprezentującego pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="21a9c-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="21a9c-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="21a9c-128">-SecretVersion</span></span>
<span data-ttu-id="21a9c-129">Wersja tajnego magazynu kluczy reprezentującego pełną PFX certyfikatu</span><span class="sxs-lookup"><span data-stu-id="21a9c-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="21a9c-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="21a9c-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="21a9c-131">Czy zezwolić na koligację sesji na tym hoście.</span><span class="sxs-lookup"><span data-stu-id="21a9c-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="21a9c-132">Wartość domyślna jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="21a9c-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="21a9c-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="21a9c-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="21a9c-134">Czas wygaśnięcia (TTL) używany w sekundach dla koligacji sesji (jeśli ma zastosowanie).</span><span class="sxs-lookup"><span data-stu-id="21a9c-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="21a9c-135">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="21a9c-135">Default value is 0</span></span>

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

### <span data-ttu-id="21a9c-136">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="21a9c-136">-Vault</span></span>
<span data-ttu-id="21a9c-137">Magazyn kluczy zawierający certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="21a9c-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="21a9c-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="21a9c-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="21a9c-139">Identyfikator zasobu zasad zapory aplikacji sieci Web dla każdego hosta (jeśli ma zastosowanie)</span><span class="sxs-lookup"><span data-stu-id="21a9c-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="21a9c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a9c-140">CommonParameters</span></span>
<span data-ttu-id="21a9c-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a9c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a9c-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21a9c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a9c-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21a9c-143">INPUTS</span></span>

### <span data-ttu-id="21a9c-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21a9c-144">None</span></span>
## <span data-ttu-id="21a9c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21a9c-145">OUTPUTS</span></span>

### <span data-ttu-id="21a9c-146">Microsoft. Azure. Commands. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="21a9c-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="21a9c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21a9c-147">NOTES</span></span>

## <span data-ttu-id="21a9c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21a9c-148">RELATED LINKS</span></span>

<span data-ttu-id="21a9c-149">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="21a9c-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
