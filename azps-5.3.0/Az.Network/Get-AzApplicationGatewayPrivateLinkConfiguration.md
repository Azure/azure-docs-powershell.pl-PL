---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499577"
---
# <span data-ttu-id="3372b-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3372b-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="3372b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3372b-102">SYNOPSIS</span></span>
<span data-ttu-id="3372b-103">Pobiera prywatną konfigurację linku do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3372b-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="3372b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3372b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3372b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3372b-105">DESCRIPTION</span></span>
<span data-ttu-id="3372b-106">Polecenie cmdlet **Get-AzApplicationGatewayPrivateLinkConfiguration** pobiera prywatną konfigurację linku do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3372b-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="3372b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3372b-107">EXAMPLES</span></span>

### <span data-ttu-id="3372b-108">Przykład 1: uzyskiwanie określonej konfiguracji linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="3372b-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="3372b-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3372b-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3372b-110">Drugie polecenie pobiera konfigurację linku prywatnego o nazwie privateLinkConfig01 z $AppGw i zapisuje ją w zmiennej $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3372b-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="3372b-111">Przykład 2: uzyskiwanie listy konfiguracji prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="3372b-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="3372b-112">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3372b-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3372b-113">Drugie polecenie pobiera wszystkie konfiguracje linków prywatnych z $AppGw i zapisuje je w zmiennej $PrivateLinkConfigurations.</span><span class="sxs-lookup"><span data-stu-id="3372b-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="3372b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3372b-114">PARAMETERS</span></span>

### <span data-ttu-id="3372b-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3372b-115">-ApplicationGateway</span></span>
<span data-ttu-id="3372b-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3372b-116">The applicationGateway</span></span>

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

### <span data-ttu-id="3372b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3372b-117">-DefaultProfile</span></span>
<span data-ttu-id="3372b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3372b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3372b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3372b-119">-Name</span></span>
<span data-ttu-id="3372b-120">Nazwa konfiguracji usługi Application Gateway privateLink</span><span class="sxs-lookup"><span data-stu-id="3372b-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="3372b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3372b-121">CommonParameters</span></span>
<span data-ttu-id="3372b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3372b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3372b-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3372b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3372b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3372b-124">INPUTS</span></span>

### <span data-ttu-id="3372b-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3372b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3372b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3372b-126">OUTPUTS</span></span>

### <span data-ttu-id="3372b-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3372b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="3372b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3372b-128">NOTES</span></span>

## <span data-ttu-id="3372b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3372b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3372b-130">Nowe — AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3372b-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3372b-131">Dodaj-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3372b-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3372b-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3372b-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3372b-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3372b-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)