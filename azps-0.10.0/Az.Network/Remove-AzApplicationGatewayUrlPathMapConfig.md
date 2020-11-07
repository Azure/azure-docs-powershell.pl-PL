---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890330"
---
# <span data-ttu-id="40d48-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40d48-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="40d48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40d48-102">SYNOPSIS</span></span>
<span data-ttu-id="40d48-103">Usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="40d48-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="40d48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40d48-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d48-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40d48-105">DESCRIPTION</span></span>
<span data-ttu-id="40d48-106">Polecenie cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="40d48-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="40d48-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40d48-107">EXAMPLES</span></span>

### <span data-ttu-id="40d48-108">1:1</span><span class="sxs-lookup"><span data-stu-id="40d48-108">1:</span></span>
```

```

## <span data-ttu-id="40d48-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40d48-109">PARAMETERS</span></span>

### <span data-ttu-id="40d48-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d48-110">-ApplicationGateway</span></span>
<span data-ttu-id="40d48-111">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="40d48-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="40d48-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d48-112">-DefaultProfile</span></span>
<span data-ttu-id="40d48-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40d48-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d48-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40d48-114">-Name</span></span>
<span data-ttu-id="40d48-115">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet usuwa z serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="40d48-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="40d48-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d48-116">CommonParameters</span></span>
<span data-ttu-id="40d48-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d48-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d48-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d48-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d48-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40d48-119">INPUTS</span></span>

### <span data-ttu-id="40d48-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d48-120">PSApplicationGateway</span></span>
<span data-ttu-id="40d48-121">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="40d48-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="40d48-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40d48-122">OUTPUTS</span></span>

### <span data-ttu-id="40d48-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d48-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="40d48-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40d48-124">NOTES</span></span>

## <span data-ttu-id="40d48-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40d48-125">RELATED LINKS</span></span>

[<span data-ttu-id="40d48-126">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40d48-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40d48-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40d48-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40d48-128">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40d48-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40d48-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40d48-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


