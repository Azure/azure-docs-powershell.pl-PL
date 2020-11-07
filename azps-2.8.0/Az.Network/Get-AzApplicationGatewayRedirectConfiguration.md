---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 79a4e76f4c9ece74c25c8f017fab6840aac63a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870263"
---
# <span data-ttu-id="806d6-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="806d6-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="806d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="806d6-102">SYNOPSIS</span></span>
<span data-ttu-id="806d6-103">Pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="806d6-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="806d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="806d6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="806d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="806d6-105">DESCRIPTION</span></span>
<span data-ttu-id="806d6-106">Polecenie cmdlet **Get-AzApplicationGatewayRedirectConfiguration** pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="806d6-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="806d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="806d6-107">EXAMPLES</span></span>

### <span data-ttu-id="806d6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="806d6-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="806d6-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="806d6-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="806d6-110">Drugie polecenie pobiera konfigurację przekierowania o nazwie Redirect01 od bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="806d6-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="806d6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="806d6-111">PARAMETERS</span></span>

### <span data-ttu-id="806d6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="806d6-112">-ApplicationGateway</span></span>
<span data-ttu-id="806d6-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="806d6-113">The applicationGateway</span></span>

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

### <span data-ttu-id="806d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806d6-114">-DefaultProfile</span></span>
<span data-ttu-id="806d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="806d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="806d6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="806d6-116">-Name</span></span>
<span data-ttu-id="806d6-117">Nazwa reguły rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="806d6-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="806d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806d6-118">CommonParameters</span></span>
<span data-ttu-id="806d6-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806d6-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="806d6-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806d6-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="806d6-121">INPUTS</span></span>

### <span data-ttu-id="806d6-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="806d6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="806d6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="806d6-123">OUTPUTS</span></span>

### <span data-ttu-id="806d6-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="806d6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="806d6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="806d6-125">NOTES</span></span>

## <span data-ttu-id="806d6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="806d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="806d6-127">Dodaj-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="806d6-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="806d6-128">Nowe — AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="806d6-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="806d6-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="806d6-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="806d6-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="806d6-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
