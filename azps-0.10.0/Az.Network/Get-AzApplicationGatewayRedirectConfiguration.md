---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: c9443c93745c1f6db9372b8f845f3ac399e51398
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890869"
---
# <span data-ttu-id="bc9fc-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc9fc-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bc9fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9fc-103">Pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc9fc-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="bc9fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc9fc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc9fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc9fc-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9fc-106">Polecenie cmdlet **Get-AzApplicationGatewayRedirectConfiguration** pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc9fc-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="bc9fc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc9fc-107">EXAMPLES</span></span>

### <span data-ttu-id="bc9fc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc9fc-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bc9fc-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bc9fc-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bc9fc-110">Drugie polecenie pobiera konfigurację przekierowania o nazwie Redirect01 od bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bc9fc-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="bc9fc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc9fc-111">PARAMETERS</span></span>

### <span data-ttu-id="bc9fc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc9fc-112">-ApplicationGateway</span></span>
<span data-ttu-id="bc9fc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc9fc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bc9fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9fc-114">-DefaultProfile</span></span>
<span data-ttu-id="bc9fc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc9fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc9fc-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc9fc-116">-Name</span></span>
<span data-ttu-id="bc9fc-117">Nazwa reguły rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="bc9fc-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="bc9fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9fc-118">CommonParameters</span></span>
<span data-ttu-id="bc9fc-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc9fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9fc-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc9fc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9fc-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc9fc-121">INPUTS</span></span>

### <span data-ttu-id="bc9fc-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc9fc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bc9fc-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc9fc-123">OUTPUTS</span></span>

### <span data-ttu-id="bc9fc-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc9fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="bc9fc-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc9fc-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bc9fc-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc9fc-126">NOTES</span></span>

## <span data-ttu-id="bc9fc-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc9fc-127">RELATED LINKS</span></span>

