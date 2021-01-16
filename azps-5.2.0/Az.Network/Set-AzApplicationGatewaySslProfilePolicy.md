---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 344be8b71bc74f3620ca90dd60b61f9a59026ea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333889"
---
# <span data-ttu-id="2a150-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a150-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="2a150-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a150-102">SYNOPSIS</span></span>
<span data-ttu-id="2a150-103">Modyfikuje zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2a150-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="2a150-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a150-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a150-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a150-105">DESCRIPTION</span></span>
<span data-ttu-id="2a150-106">Polecenie cmdlet **Set-AzApplicationGatewaySslProfilePolicy** modyfikuje zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2a150-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="2a150-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a150-107">EXAMPLES</span></span>

### <span data-ttu-id="2a150-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a150-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="2a150-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2a150-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="2a150-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 dla $AppGw i zapisuje ustawienia w zmiennej $profile.</span><span class="sxs-lookup"><span data-stu-id="2a150-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="2a150-111">Ostatnie polecenie modyfikuje zasady SSL obiektu profilu SSL przechowywanego w $profile.</span><span class="sxs-lookup"><span data-stu-id="2a150-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="2a150-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a150-112">PARAMETERS</span></span>

### <span data-ttu-id="2a150-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="2a150-113">-CipherSuite</span></span>
<span data-ttu-id="2a150-114">Mechanizmy szyfrowania SSL są włączone w określonej kolejności dla bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2a150-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a150-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a150-115">-DefaultProfile</span></span>
<span data-ttu-id="2a150-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a150-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a150-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="2a150-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="2a150-118">Lista protokołów SSL do wyłączenia</span><span class="sxs-lookup"><span data-stu-id="2a150-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a150-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="2a150-119">-MinProtocolVersion</span></span>
<span data-ttu-id="2a150-120">Minimalna wersja protokołu SSL, która ma być obsługiwana w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a150-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a150-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="2a150-121">-PolicyName</span></span>
<span data-ttu-id="2a150-122">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="2a150-122">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a150-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="2a150-123">-PolicyType</span></span>
<span data-ttu-id="2a150-124">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="2a150-124">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a150-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="2a150-125">-SslProfile</span></span>
<span data-ttu-id="2a150-126">Profil SSL bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a150-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a150-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a150-127">-Confirm</span></span>
<span data-ttu-id="2a150-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a150-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a150-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a150-129">-WhatIf</span></span>
<span data-ttu-id="2a150-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a150-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a150-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a150-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a150-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a150-132">CommonParameters</span></span>
<span data-ttu-id="2a150-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a150-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a150-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a150-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a150-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a150-135">INPUTS</span></span>

### <span data-ttu-id="2a150-136">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2a150-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2a150-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a150-137">OUTPUTS</span></span>

### <span data-ttu-id="2a150-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2a150-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2a150-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a150-139">NOTES</span></span>

## <span data-ttu-id="2a150-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a150-140">RELATED LINKS</span></span>

[<span data-ttu-id="2a150-141">Dodaj-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a150-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="2a150-142">Nowe — AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a150-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="2a150-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a150-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="2a150-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a150-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)