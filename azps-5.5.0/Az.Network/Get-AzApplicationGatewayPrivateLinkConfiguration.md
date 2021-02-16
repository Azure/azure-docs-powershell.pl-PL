---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203162"
---
# <span data-ttu-id="a3e04-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3e04-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a3e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e04-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e04-103">Pobiera konfigurację prywatnego linku bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a3e04-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="a3e04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3e04-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e04-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3e04-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e04-106">Polecenie **cmdlet Get-AzApplicationGatewayPrivateLinkConfiguration** pobiera konfigurację prywatnego linku bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a3e04-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="a3e04-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3e04-107">EXAMPLES</span></span>

### <span data-ttu-id="a3e04-108">Przykład 1. Uzyskiwanie określonej konfiguracji linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="a3e04-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a3e04-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3e04-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3e04-110">Drugie polecenie pobiera z programu $AppGw konfigurację prywatnego linku o nazwie privateLinkConfig01 i przechowuje ją w $PrivateLinkConfiguration sieci.</span><span class="sxs-lookup"><span data-stu-id="a3e04-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="a3e04-111">Przykład 2. Uzyskiwanie listy konfiguracji linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="a3e04-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="a3e04-112">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3e04-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3e04-113">Drugie polecenie pobiera wszystkie konfiguracje prywatnego linku z $AppGw i zapisuje je w $PrivateLinkConfigurations zmienną.</span><span class="sxs-lookup"><span data-stu-id="a3e04-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="a3e04-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3e04-114">PARAMETERS</span></span>

### <span data-ttu-id="a3e04-115">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3e04-115">-ApplicationGateway</span></span>
<span data-ttu-id="a3e04-116">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3e04-116">The applicationGateway</span></span>

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

### <span data-ttu-id="a3e04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e04-117">-DefaultProfile</span></span>
<span data-ttu-id="a3e04-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3e04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e04-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3e04-119">-Name</span></span>
<span data-ttu-id="a3e04-120">Nazwa konfiguracji privateLink bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a3e04-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="a3e04-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e04-121">CommonParameters</span></span>
<span data-ttu-id="a3e04-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e04-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e04-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3e04-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e04-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3e04-124">INPUTS</span></span>

### <span data-ttu-id="a3e04-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3e04-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3e04-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3e04-126">OUTPUTS</span></span>

### <span data-ttu-id="a3e04-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3e04-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a3e04-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3e04-128">NOTES</span></span>

## <span data-ttu-id="a3e04-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3e04-129">RELATED LINKS</span></span>

[<span data-ttu-id="a3e04-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3e04-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a3e04-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3e04-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a3e04-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3e04-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a3e04-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3e04-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)