---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189866"
---
# <span data-ttu-id="0d767-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="0d767-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="0d767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d767-102">SYNOPSIS</span></span>
<span data-ttu-id="0d767-103">Pobiera kondycję zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0d767-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="0d767-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d767-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d767-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d767-105">DESCRIPTION</span></span>
<span data-ttu-id="0d767-106">Polecenie Get-AzApplicationGatewayBackendHealth pobiera kondycję zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0d767-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="0d767-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d767-107">EXAMPLES</span></span>

### <span data-ttu-id="0d767-108">Przykład 1. Kondycja zaplecza bez rozwiniętych zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d767-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="0d767-109">To polecenie pobiera kondycję zaplecza bramy aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $BackendHealth zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d767-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="0d767-110">Przykład 2. Kondycja bazy danych z rozwiniętymi zasobami.</span><span class="sxs-lookup"><span data-stu-id="0d767-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="0d767-111">To polecenie ma kondycję zaplecza (wraz z rozwiniętymi zasobami) bramy aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $BackendHealth zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d767-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="0d767-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d767-112">PARAMETERS</span></span>

### <span data-ttu-id="0d767-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0d767-113">-AsJob</span></span>
<span data-ttu-id="0d767-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0d767-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d767-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d767-115">-DefaultProfile</span></span>
<span data-ttu-id="0d767-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d767-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d767-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0d767-117">-ExpandResource</span></span>
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

### <span data-ttu-id="0d767-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0d767-118">-Name</span></span>
<span data-ttu-id="0d767-119">Określa nazwę bramy aplikacji, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d767-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0d767-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d767-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d767-121">Określa nazwę grupy zasobów zawierającej bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0d767-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="0d767-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d767-122">CommonParameters</span></span>
<span data-ttu-id="0d767-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d767-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d767-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d767-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d767-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d767-125">INPUTS</span></span>

### <span data-ttu-id="0d767-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0d767-126">System.String</span></span>

## <span data-ttu-id="0d767-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d767-127">OUTPUTS</span></span>

### <span data-ttu-id="0d767-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="0d767-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="0d767-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d767-129">NOTES</span></span>
<span data-ttu-id="0d767-130">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="0d767-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0d767-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d767-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d767-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d767-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

