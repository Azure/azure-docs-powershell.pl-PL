---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 6dff1e78f83c48a103266c39bd9f3462a20b50a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995317"
---
# <span data-ttu-id="81471-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="81471-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="81471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81471-102">SYNOPSIS</span></span>
<span data-ttu-id="81471-103">Modyfikuje zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="81471-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="81471-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81471-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81471-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="81471-105">DESCRIPTION</span></span>
<span data-ttu-id="81471-106">Polecenie **cmdlet Set-AzApplicationGatewaySslProfilePolicy** modyfikuje zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="81471-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="81471-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81471-107">EXAMPLES</span></span>

### <span data-ttu-id="81471-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81471-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="81471-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="81471-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="81471-110">Drugie polecenie pobiera profil ssl o nazwie SslProfile01 for $AppGw i zapisuje ustawienia w $profile pliku.</span><span class="sxs-lookup"><span data-stu-id="81471-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="81471-111">Ostatnie polecenie modyfikuje zasady ssl obiektu profilu ssl przechowywanego w $profile.</span><span class="sxs-lookup"><span data-stu-id="81471-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="81471-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81471-112">PARAMETERS</span></span>

### <span data-ttu-id="81471-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="81471-113">-CipherSuite</span></span>
<span data-ttu-id="81471-114">Pakiety szyfrowania ssl, które mają być włączone w określonej kolejności dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="81471-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="81471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81471-115">-DefaultProfile</span></span>
<span data-ttu-id="81471-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81471-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81471-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="81471-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="81471-118">Lista protokołów SSL do wyłączenia</span><span class="sxs-lookup"><span data-stu-id="81471-118">List of SSL protocols to be disabled</span></span>

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

### <span data-ttu-id="81471-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="81471-119">-MinProtocolVersion</span></span>
<span data-ttu-id="81471-120">Minimalna wersja protokołu Ssl, która ma być obsługiwana przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="81471-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="81471-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="81471-121">-PolicyName</span></span>
<span data-ttu-id="81471-122">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="81471-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="81471-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="81471-123">-PolicyType</span></span>
<span data-ttu-id="81471-124">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="81471-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="81471-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="81471-125">-SslProfile</span></span>
<span data-ttu-id="81471-126">Profil SSL bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="81471-126">The application gateway SSL profile</span></span>

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

### <span data-ttu-id="81471-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81471-127">-Confirm</span></span>
<span data-ttu-id="81471-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81471-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81471-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81471-129">-WhatIf</span></span>
<span data-ttu-id="81471-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81471-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81471-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="81471-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81471-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81471-132">CommonParameters</span></span>
<span data-ttu-id="81471-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81471-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81471-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81471-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81471-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81471-135">INPUTS</span></span>

### <span data-ttu-id="81471-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="81471-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="81471-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81471-137">OUTPUTS</span></span>

### <span data-ttu-id="81471-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="81471-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="81471-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81471-139">NOTES</span></span>

## <span data-ttu-id="81471-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81471-140">RELATED LINKS</span></span>

[<span data-ttu-id="81471-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="81471-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="81471-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="81471-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="81471-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="81471-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="81471-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="81471-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)