---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326214"
---
# <span data-ttu-id="85c20-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="85c20-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="85c20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85c20-102">SYNOPSIS</span></span>
<span data-ttu-id="85c20-103">Usuwa ustawienia HTTP zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85c20-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="85c20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85c20-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85c20-105">DESCRIPTION</span></span>
<span data-ttu-id="85c20-106">Polecenie cmdlet Remove-AzApplicationGatewayBackendHttpSetting usuwa ustawienia protokołu HTTP (Hypertext Transfer Protocol) z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85c20-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="85c20-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85c20-107">EXAMPLES</span></span>

### <span data-ttu-id="85c20-108">Przykład 1: usuwanie ustawień wewnętrznych protokołu HTTP z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="85c20-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="85c20-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="85c20-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="85c20-110">Drugie polecenie usuwa ustawienie HTTP zaplecza o nazwie BackEndSetting02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="85c20-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="85c20-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85c20-111">PARAMETERS</span></span>

### <span data-ttu-id="85c20-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85c20-112">-ApplicationGateway</span></span>
<span data-ttu-id="85c20-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="85c20-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="85c20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c20-114">-DefaultProfile</span></span>
<span data-ttu-id="85c20-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85c20-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c20-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85c20-116">-Name</span></span>
<span data-ttu-id="85c20-117">Określa nazwę ustawienia HTTP zaplecza, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c20-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="85c20-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c20-118">CommonParameters</span></span>
<span data-ttu-id="85c20-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c20-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c20-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c20-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c20-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85c20-121">INPUTS</span></span>

### <span data-ttu-id="85c20-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85c20-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85c20-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85c20-123">OUTPUTS</span></span>

### <span data-ttu-id="85c20-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85c20-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85c20-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85c20-125">NOTES</span></span>

## <span data-ttu-id="85c20-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85c20-126">RELATED LINKS</span></span>

[<span data-ttu-id="85c20-127">Dodaj-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="85c20-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="85c20-128">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="85c20-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="85c20-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="85c20-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="85c20-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="85c20-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

