---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e965f2cdbd9909003a07ea6c6addd198110e456f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890354"
---
# <span data-ttu-id="a5212-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5212-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a5212-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5212-102">SYNOPSIS</span></span>
<span data-ttu-id="a5212-103">Usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a5212-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="a5212-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5212-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5212-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5212-105">DESCRIPTION</span></span>
<span data-ttu-id="a5212-106">Polecenie cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a5212-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="a5212-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5212-107">EXAMPLES</span></span>

### <span data-ttu-id="a5212-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5212-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="a5212-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a5212-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a5212-110">Drugie polecenie usuwa konfigurację przekierowania o nazwie Redirect01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a5212-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a5212-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5212-111">PARAMETERS</span></span>

### <span data-ttu-id="a5212-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5212-112">-ApplicationGateway</span></span>
<span data-ttu-id="a5212-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5212-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a5212-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5212-114">-DefaultProfile</span></span>
<span data-ttu-id="a5212-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5212-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5212-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5212-116">-Name</span></span>
<span data-ttu-id="a5212-117">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="a5212-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="a5212-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5212-118">CommonParameters</span></span>
<span data-ttu-id="a5212-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5212-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5212-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5212-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5212-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5212-121">INPUTS</span></span>

### <span data-ttu-id="a5212-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5212-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5212-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5212-123">OUTPUTS</span></span>

### <span data-ttu-id="a5212-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5212-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5212-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5212-125">NOTES</span></span>

## <span data-ttu-id="a5212-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5212-126">RELATED LINKS</span></span>

