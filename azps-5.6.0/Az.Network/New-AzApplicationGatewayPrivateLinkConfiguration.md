---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 7c338f49191071bfa48214e65f79e196a75650eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973681"
---
# <span data-ttu-id="79230-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="79230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79230-102">SYNOPSIS</span></span>
<span data-ttu-id="79230-103">Tworzy konfigurację prywatnego linku dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="79230-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="79230-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79230-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79230-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79230-105">DESCRIPTION</span></span>
<span data-ttu-id="79230-106">Polecenie **cmdlet New-AzApplicationGatewayPrivateLinkConfiguration** tworzy konfigurację PrivateLink dla bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="79230-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="79230-107">Konfiguracja łącza prywatnego musi być skojarzona z konfiguracją frontonu ip, aby włączyć funkcję prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="79230-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="79230-108">Jedna konfiguracja łącza prywatnego może być co najwyżej skojarzona tylko z jedną konfiguracją frontonu ip w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79230-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="79230-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79230-109">EXAMPLES</span></span>

### <span data-ttu-id="79230-110">Przykład 1. Tworzenie konfiguracji linku prywatnego przy użyciu pojedynczej konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="79230-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="79230-111">To polecenie tworzy konfigurację privateLink o nazwie "privateLinkConfig01" i przechowuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="79230-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="79230-112">Przykład 2. Tworzenie konfiguracji linku prywatnego z wieloma konfiguracjami adresów IP</span><span class="sxs-lookup"><span data-stu-id="79230-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="79230-113">To polecenie tworzy konfigurację privateLink o nazwie "privateLinkConfig01" z dwoma konfiguracjami ipConfigurations i przechowuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="79230-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="79230-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79230-114">PARAMETERS</span></span>

### <span data-ttu-id="79230-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79230-115">-DefaultProfile</span></span>
<span data-ttu-id="79230-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79230-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79230-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-117">-IpConfiguration</span></span>
<span data-ttu-id="79230-118">Lista konfiguracji ip</span><span class="sxs-lookup"><span data-stu-id="79230-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="79230-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79230-119">-Name</span></span>
<span data-ttu-id="79230-120">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="79230-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="79230-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79230-121">-Confirm</span></span>
<span data-ttu-id="79230-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79230-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79230-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79230-123">-WhatIf</span></span>
<span data-ttu-id="79230-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79230-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79230-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79230-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79230-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79230-126">CommonParameters</span></span>
<span data-ttu-id="79230-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79230-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79230-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79230-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79230-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79230-129">INPUTS</span></span>

### <span data-ttu-id="79230-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="79230-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="79230-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79230-131">OUTPUTS</span></span>

### <span data-ttu-id="79230-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="79230-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79230-133">NOTES</span></span>

## <span data-ttu-id="79230-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79230-134">RELATED LINKS</span></span>

[<span data-ttu-id="79230-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="79230-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="79230-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="79230-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79230-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
