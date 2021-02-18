---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240914"
---
# <span data-ttu-id="59847-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="59847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59847-102">SYNOPSIS</span></span>
<span data-ttu-id="59847-103">Tworzy konfigurację prywatnego linku dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="59847-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="59847-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59847-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59847-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="59847-105">DESCRIPTION</span></span>
<span data-ttu-id="59847-106">Polecenie **cmdlet New-AzApplicationGatewayPrivateLinkConfiguration** tworzy konfigurację PrivateLink dla bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="59847-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="59847-107">Konfiguracja łącza prywatnego musi być skojarzona z konfiguracją frontonu ip, aby włączyć funkcję prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="59847-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="59847-108">Jedna konfiguracja łącza prywatnego może być co najwyżej skojarzona tylko z jedną konfiguracją frontonu ip w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="59847-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="59847-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59847-109">EXAMPLES</span></span>

### <span data-ttu-id="59847-110">Przykład 1. Tworzenie konfiguracji linku prywatnego przy użyciu pojedynczej konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="59847-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="59847-111">To polecenie tworzy konfigurację privateLink o nazwie "privateLinkConfig01" i przechowuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="59847-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="59847-112">Przykład 2. Tworzenie konfiguracji linku prywatnego z wieloma konfiguracjami adresów IP</span><span class="sxs-lookup"><span data-stu-id="59847-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="59847-113">To polecenie tworzy konfigurację privateLink o nazwie "privateLinkConfig01" z dwoma konfiguracjami ipConfigurations i przechowuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="59847-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="59847-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59847-114">PARAMETERS</span></span>

### <span data-ttu-id="59847-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59847-115">-DefaultProfile</span></span>
<span data-ttu-id="59847-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59847-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59847-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-117">-IpConfiguration</span></span>
<span data-ttu-id="59847-118">Lista konfiguracji ip</span><span class="sxs-lookup"><span data-stu-id="59847-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="59847-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59847-119">-Name</span></span>
<span data-ttu-id="59847-120">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="59847-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="59847-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59847-121">-Confirm</span></span>
<span data-ttu-id="59847-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59847-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59847-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59847-123">-WhatIf</span></span>
<span data-ttu-id="59847-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59847-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59847-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="59847-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59847-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59847-126">CommonParameters</span></span>
<span data-ttu-id="59847-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59847-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59847-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59847-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59847-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59847-129">INPUTS</span></span>

### <span data-ttu-id="59847-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="59847-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="59847-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59847-131">OUTPUTS</span></span>

### <span data-ttu-id="59847-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="59847-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59847-133">NOTES</span></span>

## <span data-ttu-id="59847-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59847-134">RELATED LINKS</span></span>

[<span data-ttu-id="59847-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="59847-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="59847-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="59847-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59847-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
