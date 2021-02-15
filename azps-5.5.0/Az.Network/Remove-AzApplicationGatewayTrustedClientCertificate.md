---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186986"
---
# <span data-ttu-id="1c9d9-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1c9d9-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1c9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9d9-103">Usuwa obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="1c9d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c9d9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9d9-106">Polecenie **cmdlet Remove-AzApplicationGatewayTrustedClientCertificate** usuwa obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="1c9d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c9d9-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c9d9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="1c9d9-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje je w $gw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="1c9d9-110">Drugie polecenie usuwa łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o nazwie "TrustedClientCertificate01" z bramy aplikacji przechowywanej w $gw.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="1c9d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c9d9-111">PARAMETERS</span></span>

### <span data-ttu-id="1c9d9-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c9d9-112">-ApplicationGateway</span></span>
<span data-ttu-id="1c9d9-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c9d9-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9d9-114">-DefaultProfile</span></span>
<span data-ttu-id="1c9d9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9d9-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1c9d9-116">-Name</span></span>
<span data-ttu-id="1c9d9-117">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="1c9d9-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="1c9d9-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c9d9-118">-Confirm</span></span>
<span data-ttu-id="1c9d9-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9d9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9d9-120">-WhatIf</span></span>
<span data-ttu-id="1c9d9-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9d9-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9d9-123">CommonParameters</span></span>
<span data-ttu-id="1c9d9-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9d9-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c9d9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9d9-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c9d9-126">INPUTS</span></span>

### <span data-ttu-id="1c9d9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c9d9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c9d9-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c9d9-128">OUTPUTS</span></span>

### <span data-ttu-id="1c9d9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c9d9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c9d9-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c9d9-130">NOTES</span></span>

## <span data-ttu-id="1c9d9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c9d9-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c9d9-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1c9d9-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1c9d9-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1c9d9-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1c9d9-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1c9d9-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1c9d9-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1c9d9-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)