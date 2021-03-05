---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 2490896fa66a3d06a8887e386c2bf6db6ff2f829
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993987"
---
# <span data-ttu-id="bf420-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="bf420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf420-102">SYNOPSIS</span></span>
<span data-ttu-id="bf420-103">Pobiera profil SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf420-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="bf420-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf420-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf420-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf420-105">DESCRIPTION</span></span>
<span data-ttu-id="bf420-106">Polecenie **cmdlet Get-AzApplicationGatewaySslProfile** pobiera profil SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf420-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="bf420-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf420-107">EXAMPLES</span></span>

### <span data-ttu-id="bf420-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf420-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="bf420-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w $AppGw zmienną. Drugie polecenie pobiera profil SSL SslProfile01 for $AppGw i zapisuje go w $profile pliku.</span><span class="sxs-lookup"><span data-stu-id="bf420-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="bf420-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf420-110">PARAMETERS</span></span>

### <span data-ttu-id="bf420-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf420-111">-ApplicationGateway</span></span>
<span data-ttu-id="bf420-112">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf420-112">The applicationGateway</span></span>

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

### <span data-ttu-id="bf420-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-113">-DefaultProfile</span></span>
<span data-ttu-id="bf420-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf420-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf420-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bf420-115">-Name</span></span>
<span data-ttu-id="bf420-116">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="bf420-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="bf420-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf420-117">CommonParameters</span></span>
<span data-ttu-id="bf420-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf420-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf420-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf420-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf420-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf420-120">INPUTS</span></span>

### <span data-ttu-id="bf420-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf420-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf420-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf420-122">OUTPUTS</span></span>

### <span data-ttu-id="bf420-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="bf420-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf420-124">NOTES</span></span>

## <span data-ttu-id="bf420-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf420-125">RELATED LINKS</span></span>

[<span data-ttu-id="bf420-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="bf420-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="bf420-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="bf420-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bf420-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)