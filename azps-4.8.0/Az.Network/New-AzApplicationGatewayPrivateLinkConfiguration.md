---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223840"
---
# <span data-ttu-id="e4d6a-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="e4d6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d6a-103">Tworzy konfigurację linku prywatnego dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="e4d6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4d6a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d6a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="e4d6a-106">Polecenie cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** tworzy konfigurację PrivateLink dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="e4d6a-107">Aby można było włączyć funkcję linków prywatnych, konfiguracja prywatnego linku musi być skojarzona z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="e4d6a-108">Jedna prywatna konfiguracja linku może atmost być skojarzona tylko z jednej konfiguracji adresu IP frontonu w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="e4d6a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4d6a-109">EXAMPLES</span></span>

### <span data-ttu-id="e4d6a-110">Przykład 1. Tworzenie prywatnej konfiguracji linku przy użyciu jednej konfiguracji IP</span><span class="sxs-lookup"><span data-stu-id="e4d6a-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="e4d6a-111">To polecenie tworzy konfigurację PrivateLink o nazwie "privateLinkConfig01" i zapisuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="e4d6a-112">Przykład 2: Tworzenie prywatnej konfiguracji linku z wieloma konfiguracjami protokołu IP</span><span class="sxs-lookup"><span data-stu-id="e4d6a-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="e4d6a-113">To polecenie tworzy konfigurację PrivateLink o nazwie "privateLinkConfig01" z dwoma elementami Ipconfiguration i zapisuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="e4d6a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4d6a-114">PARAMETERS</span></span>

### <span data-ttu-id="e4d6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d6a-115">-DefaultProfile</span></span>
<span data-ttu-id="e4d6a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d6a-117">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-117">-IpConfiguration</span></span>
<span data-ttu-id="e4d6a-118">Lista elementu ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d6a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4d6a-119">-Name</span></span>
<span data-ttu-id="e4d6a-120">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="e4d6a-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d6a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4d6a-121">-Confirm</span></span>
<span data-ttu-id="e4d6a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d6a-123">-WhatIf</span></span>
<span data-ttu-id="e4d6a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d6a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d6a-126">CommonParameters</span></span>
<span data-ttu-id="e4d6a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d6a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4d6a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d6a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4d6a-129">INPUTS</span></span>

### <span data-ttu-id="e4d6a-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="e4d6a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="e4d6a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4d6a-131">OUTPUTS</span></span>

### <span data-ttu-id="e4d6a-132">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="e4d6a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4d6a-133">NOTES</span></span>

## <span data-ttu-id="e4d6a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4d6a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4d6a-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e4d6a-136">Dodaj-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e4d6a-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e4d6a-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d6a-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
