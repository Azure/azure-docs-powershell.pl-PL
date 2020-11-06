---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524409"
---
# <span data-ttu-id="31fb8-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="31fb8-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="31fb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="31fb8-103">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="31fb8-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31fb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31fb8-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31fb8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="31fb8-106">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="31fb8-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="31fb8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="31fb8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31fb8-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


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

<span data-ttu-id="31fb8-109">Tworzenie obiektu PSFrontendEndpoint na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="31fb8-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="31fb8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="31fb8-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="31fb8-111">-CertificateSource</span></span>
<span data-ttu-id="31fb8-112">Źródło certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="31fb8-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="31fb8-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="31fb8-113">-CertificateType</span></span>
<span data-ttu-id="31fb8-114">Typ certyfikatu służący do bezpiecznego połączenia z usługą frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="31fb8-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="31fb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31fb8-115">-DefaultProfile</span></span>
<span data-ttu-id="31fb8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31fb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fb8-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="31fb8-117">-HostName</span></span>
<span data-ttu-id="31fb8-118">Nazwa hosta frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="31fb8-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="31fb8-119">Musi być nazwą domeny.</span><span class="sxs-lookup"><span data-stu-id="31fb8-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="31fb8-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31fb8-120">-Name</span></span>
<span data-ttu-id="31fb8-121">Nazwa punktu końcowego frontonu.</span><span class="sxs-lookup"><span data-stu-id="31fb8-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="31fb8-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="31fb8-122">-ProtocolType</span></span>
<span data-ttu-id="31fb8-123">Protokół rozszerzeń TLS, który jest wykorzystywany do zabezpieczania dostarczania</span><span class="sxs-lookup"><span data-stu-id="31fb8-123">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="31fb8-124">-Secretname</span><span class="sxs-lookup"><span data-stu-id="31fb8-124">-SecretName</span></span>
<span data-ttu-id="31fb8-125">Nazwa tajnego magazynu kluczy reprezentującego pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="31fb8-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="31fb8-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="31fb8-126">-SecretVersion</span></span>
<span data-ttu-id="31fb8-127">Wersja tajnego magazynu kluczy reprezentującego pełną PFX certyfikatu</span><span class="sxs-lookup"><span data-stu-id="31fb8-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="31fb8-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="31fb8-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="31fb8-129">Czy zezwolić na koligację sesji na tym hoście.</span><span class="sxs-lookup"><span data-stu-id="31fb8-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="31fb8-130">Wartość domyślna jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="31fb8-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="31fb8-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="31fb8-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="31fb8-132">Czas wygaśnięcia (TTL) używany w sekundach dla koligacji sesji (jeśli ma zastosowanie).</span><span class="sxs-lookup"><span data-stu-id="31fb8-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="31fb8-133">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="31fb8-133">Default value is 0</span></span>

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

### <span data-ttu-id="31fb8-134">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="31fb8-134">-Vault</span></span>
<span data-ttu-id="31fb8-135">Magazyn kluczy zawierający certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="31fb8-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="31fb8-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="31fb8-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="31fb8-137">Identyfikator zasobu zasad zapory aplikacji sieci Web dla każdego hosta (jeśli ma zastosowanie)</span><span class="sxs-lookup"><span data-stu-id="31fb8-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="31fb8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31fb8-138">CommonParameters</span></span>
<span data-ttu-id="31fb8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31fb8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31fb8-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31fb8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31fb8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31fb8-141">INPUTS</span></span>

### <span data-ttu-id="31fb8-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="31fb8-142">None</span></span>

## <span data-ttu-id="31fb8-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31fb8-143">OUTPUTS</span></span>

### <span data-ttu-id="31fb8-144">Microsoft. Azure. Commands. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="31fb8-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="31fb8-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31fb8-145">NOTES</span></span>

## <span data-ttu-id="31fb8-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31fb8-146">RELATED LINKS</span></span>

<span data-ttu-id="31fb8-147">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="31fb8-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
