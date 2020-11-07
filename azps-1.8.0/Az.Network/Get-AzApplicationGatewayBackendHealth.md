---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: eb4415f4c61fd97543bd0e50de6a0a3737f435f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709630"
---
# <span data-ttu-id="6b00c-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="6b00c-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="6b00c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b00c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b00c-103">Pobiera kondycję wewnętrzną bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6b00c-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="6b00c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b00c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b00c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b00c-105">DESCRIPTION</span></span>
<span data-ttu-id="6b00c-106">Polecenie cmdlet Get-AzApplicationGatewayBackendHealth pobiera kondycję wewnętrzną zaplecza bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6b00c-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="6b00c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b00c-107">EXAMPLES</span></span>

### <span data-ttu-id="6b00c-108">Przykład 1: Pobiera kondycję bazy danych bez rozwiniętych zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b00c-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="6b00c-109">To polecenie pobiera kondycję zaplecza bramy Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="6b00c-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="6b00c-110">Przykład 2: Pobiera kondycję zaplecza z rozwiniętymi zasobami.</span><span class="sxs-lookup"><span data-stu-id="6b00c-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="6b00c-111">To polecenie pobiera kondycję bazy danych (z rozwiniętymi zasobami) bramy Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="6b00c-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="6b00c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b00c-112">PARAMETERS</span></span>

### <span data-ttu-id="6b00c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b00c-113">-AsJob</span></span>
<span data-ttu-id="6b00c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6b00c-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b00c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b00c-115">-DefaultProfile</span></span>
<span data-ttu-id="6b00c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b00c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b00c-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6b00c-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b00c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b00c-118">-Name</span></span>
<span data-ttu-id="6b00c-119">Określa nazwę bramy aplikacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b00c-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b00c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b00c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b00c-121">Określa nazwę grupy zasobów zawierającej bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6b00c-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b00c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b00c-122">CommonParameters</span></span>
<span data-ttu-id="6b00c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b00c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b00c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b00c-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b00c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b00c-125">INPUTS</span></span>

### <span data-ttu-id="6b00c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6b00c-126">System.String</span></span>

## <span data-ttu-id="6b00c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b00c-127">OUTPUTS</span></span>

### <span data-ttu-id="6b00c-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="6b00c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="6b00c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b00c-129">NOTES</span></span>
<span data-ttu-id="6b00c-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="6b00c-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6b00c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b00c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b00c-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b00c-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)
