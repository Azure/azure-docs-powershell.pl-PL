---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543647"
---
# <span data-ttu-id="0ebf4-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebf4-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0ebf4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ebf4-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebf4-103">Usuwa zaufany certyfikat główny z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ebf4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ebf4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ebf4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ebf4-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebf4-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayTrustedRootCertificate** usuwa zaufany certyfikat główny z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="0ebf4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ebf4-107">EXAMPLES</span></span>

### <span data-ttu-id="0ebf4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ebf4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0ebf4-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="0ebf4-110">Drugie polecenie usuwa zaufany certyfikat główny o nazwie myRootCA od bramy aplikacji przechowywanej w $gw.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="0ebf4-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="0ebf4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ebf4-112">PARAMETERS</span></span>

### <span data-ttu-id="0ebf4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ebf4-113">-ApplicationGateway</span></span>
<span data-ttu-id="0ebf4-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ebf4-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebf4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebf4-115">-DefaultProfile</span></span>
<span data-ttu-id="0ebf4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebf4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ebf4-117">-Name</span></span>
<span data-ttu-id="0ebf4-118">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="0ebf4-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="0ebf4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ebf4-119">-Confirm</span></span>
<span data-ttu-id="0ebf4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebf4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebf4-121">-WhatIf</span></span>
<span data-ttu-id="0ebf4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebf4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebf4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebf4-124">CommonParameters</span></span>
<span data-ttu-id="0ebf4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebf4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebf4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebf4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebf4-127">INPUTS</span></span>

### <span data-ttu-id="0ebf4-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ebf4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ebf4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ebf4-129">OUTPUTS</span></span>

### <span data-ttu-id="0ebf4-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ebf4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ebf4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ebf4-131">NOTES</span></span>

## <span data-ttu-id="0ebf4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ebf4-132">RELATED LINKS</span></span>
