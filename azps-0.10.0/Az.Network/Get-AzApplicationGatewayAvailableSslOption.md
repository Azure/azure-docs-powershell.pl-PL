---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableSslOption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: e0fa27a99a8a2d00819d558b42218b9405a5f039
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890918"
---
# <span data-ttu-id="9615e-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="9615e-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="9615e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9615e-102">SYNOPSIS</span></span>
<span data-ttu-id="9615e-103">Pobiera wszystkie dostępne opcje protokołu SSL dla zasad SSL dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9615e-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="9615e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9615e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9615e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9615e-105">DESCRIPTION</span></span>
<span data-ttu-id="9615e-106">Polecenie cmdlet **Get-AzApplicationGatewayAvailableSslOption** pobiera wszystkie dostępne opcje protokołu SSL dla zasad SSL</span><span class="sxs-lookup"><span data-stu-id="9615e-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="9615e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9615e-107">EXAMPLES</span></span>

### <span data-ttu-id="9615e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9615e-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="9615e-109">To polecenie zwraca wszystkie dostępne opcje protokołu SSL dla zasad SSL.</span><span class="sxs-lookup"><span data-stu-id="9615e-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="9615e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9615e-110">PARAMETERS</span></span>

### <span data-ttu-id="9615e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9615e-111">-DefaultProfile</span></span>
<span data-ttu-id="9615e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9615e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9615e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9615e-113">CommonParameters</span></span>
<span data-ttu-id="9615e-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9615e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9615e-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9615e-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9615e-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9615e-116">INPUTS</span></span>

### <span data-ttu-id="9615e-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9615e-117">None</span></span>

## <span data-ttu-id="9615e-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9615e-118">OUTPUTS</span></span>

### <span data-ttu-id="9615e-119">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="9615e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="9615e-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9615e-120">NOTES</span></span>

## <span data-ttu-id="9615e-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9615e-121">RELATED LINKS</span></span>

