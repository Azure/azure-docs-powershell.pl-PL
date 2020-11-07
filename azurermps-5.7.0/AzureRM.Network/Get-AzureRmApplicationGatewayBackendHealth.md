---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 6e6a2bef9ea6bc237db97139bcc7e9e7a0624fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526794"
---
# <span data-ttu-id="bfc03-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="bfc03-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="bfc03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfc03-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc03-103">Pobiera kondycję wewnętrzną bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bfc03-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfc03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfc03-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc03-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfc03-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc03-106">Polecenie cmdlet Get-AzureRmApplicationGatewayBackendHealth pobiera kondycję wewnętrzną zaplecza bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bfc03-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="bfc03-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfc03-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc03-108">--------------------------Przykład 1: Pobiera kondycję bazy danych bez rozwiniętych zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfc03-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="bfc03-109">To polecenie pobiera kondycję zaplecza bramy Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="bfc03-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="bfc03-110">--------------------------Przykład 1: uzyskuje kondycję zaplecza z rozwiniętymi zasobami.</span><span class="sxs-lookup"><span data-stu-id="bfc03-110">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="bfc03-111">To polecenie pobiera kondycję bazy danych (z rozwiniętymi zasobami) bramy Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="bfc03-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="bfc03-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfc03-112">PARAMETERS</span></span>

### <span data-ttu-id="bfc03-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfc03-113">-AsJob</span></span>
<span data-ttu-id="bfc03-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bfc03-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc03-115">-DefaultProfile</span></span>
<span data-ttu-id="bfc03-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc03-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc03-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="bfc03-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc03-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfc03-118">-Name</span></span>
<span data-ttu-id="bfc03-119">Określa nazwę bramy aplikacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc03-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc03-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc03-120">-ResourceGroupName</span></span>
<span data-ttu-id="bfc03-121">Określa nazwę grupy zasobów zawierającej bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bfc03-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc03-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc03-122">CommonParameters</span></span>
<span data-ttu-id="bfc03-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc03-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc03-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc03-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc03-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfc03-125">INPUTS</span></span>

### <span data-ttu-id="bfc03-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc03-126">System.String</span></span>

## <span data-ttu-id="bfc03-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfc03-127">OUTPUTS</span></span>

### <span data-ttu-id="bfc03-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="bfc03-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="bfc03-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfc03-129">NOTES</span></span>
<span data-ttu-id="bfc03-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="bfc03-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bfc03-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfc03-131">RELATED LINKS</span></span>

[<span data-ttu-id="bfc03-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfc03-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)
