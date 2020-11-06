---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 612e6b0cb5438dbb37a2e9d1c77da151c852fac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544260"
---
# <span data-ttu-id="d353a-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d353a-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d353a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d353a-102">SYNOPSIS</span></span>
<span data-ttu-id="d353a-103">Usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d353a-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d353a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d353a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d353a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d353a-105">DESCRIPTION</span></span>
<span data-ttu-id="d353a-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d353a-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d353a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d353a-107">EXAMPLES</span></span>

## <span data-ttu-id="d353a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d353a-108">PARAMETERS</span></span>

### <span data-ttu-id="d353a-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d353a-109">-ApplicationGateway</span></span>
<span data-ttu-id="d353a-110">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="d353a-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="d353a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d353a-111">-DefaultProfile</span></span>
<span data-ttu-id="d353a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d353a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d353a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d353a-113">-Name</span></span>
<span data-ttu-id="d353a-114">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet usuwa z serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d353a-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="d353a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d353a-115">CommonParameters</span></span>
<span data-ttu-id="d353a-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d353a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d353a-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d353a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d353a-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d353a-118">INPUTS</span></span>

### <span data-ttu-id="d353a-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d353a-119">PSApplicationGateway</span></span>
<span data-ttu-id="d353a-120">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d353a-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d353a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d353a-121">OUTPUTS</span></span>

### <span data-ttu-id="d353a-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d353a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d353a-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d353a-123">NOTES</span></span>

## <span data-ttu-id="d353a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d353a-124">RELATED LINKS</span></span>

[<span data-ttu-id="d353a-125">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d353a-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d353a-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d353a-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d353a-127">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d353a-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d353a-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d353a-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


