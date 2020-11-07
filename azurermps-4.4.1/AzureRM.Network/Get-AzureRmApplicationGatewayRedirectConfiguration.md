---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 66da90ea590c4d2359dbe7e703667f9fe7189fba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716677"
---
# <span data-ttu-id="6ac5f-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ac5f-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6ac5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ac5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac5f-103">Pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ac5f-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ac5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ac5f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac5f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ac5f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac5f-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayRedirectConfiguration** pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ac5f-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="6ac5f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ac5f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ac5f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ac5f-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6ac5f-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ac5f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6ac5f-110">Drugie polecenie pobiera konfigurację przekierowania o nazwie Redirect01 od bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ac5f-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="6ac5f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ac5f-111">PARAMETERS</span></span>

### <span data-ttu-id="6ac5f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ac5f-112">-ApplicationGateway</span></span>
<span data-ttu-id="6ac5f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ac5f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6ac5f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ac5f-114">-Name</span></span>
<span data-ttu-id="6ac5f-115">Nazwa reguły rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="6ac5f-115">The name of the request routing rule</span></span>

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

### <span data-ttu-id="6ac5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac5f-116">-DefaultProfile</span></span>
<span data-ttu-id="6ac5f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac5f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ac5f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac5f-118">CommonParameters</span></span>
<span data-ttu-id="6ac5f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac5f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac5f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac5f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac5f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ac5f-121">INPUTS</span></span>

### <span data-ttu-id="6ac5f-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ac5f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ac5f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ac5f-123">OUTPUTS</span></span>

### <span data-ttu-id="6ac5f-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ac5f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="6ac5f-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ac5f-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6ac5f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ac5f-126">NOTES</span></span>

## <span data-ttu-id="6ac5f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ac5f-127">RELATED LINKS</span></span>

