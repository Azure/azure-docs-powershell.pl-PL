---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499538"
---
# <span data-ttu-id="f3ae6-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f3ae6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ae6-103">Pobiera profil SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="f3ae6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3ae6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3ae6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ae6-106">Polecenie cmdlet **Get-AzApplicationGatewaySslProfile** pobiera profil SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="f3ae6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ae6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3ae6-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="f3ae6-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera profil SSL SslProfile01 dla $AppGw i zapisuje go w zmiennej $profile.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="f3ae6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="f3ae6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3ae6-111">-ApplicationGateway</span></span>
<span data-ttu-id="f3ae6-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3ae6-112">The applicationGateway</span></span>

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

### <span data-ttu-id="f3ae6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-113">-DefaultProfile</span></span>
<span data-ttu-id="f3ae6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ae6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3ae6-115">-Name</span></span>
<span data-ttu-id="f3ae6-116">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="f3ae6-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="f3ae6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ae6-117">CommonParameters</span></span>
<span data-ttu-id="f3ae6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ae6-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3ae6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ae6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3ae6-120">INPUTS</span></span>

### <span data-ttu-id="f3ae6-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3ae6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3ae6-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3ae6-122">OUTPUTS</span></span>

### <span data-ttu-id="f3ae6-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f3ae6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3ae6-124">NOTES</span></span>

## <span data-ttu-id="f3ae6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3ae6-125">RELATED LINKS</span></span>

[<span data-ttu-id="f3ae6-126">Nowe — AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f3ae6-127">Dodaj-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f3ae6-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f3ae6-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae6-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)