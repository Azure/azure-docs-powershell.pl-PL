---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203155"
---
# <span data-ttu-id="9c9bd-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="9c9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9bd-103">Pobiera profil SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9c9bd-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="9c9bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c9bd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c9bd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c9bd-105">DESCRIPTION</span></span>
<span data-ttu-id="9c9bd-106">Polecenie **cmdlet Get-AzApplicationGatewaySslProfile** pobiera profil SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9c9bd-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="9c9bd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c9bd-107">EXAMPLES</span></span>

### <span data-ttu-id="9c9bd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c9bd-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="9c9bd-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w $AppGw zmienną. Drugie polecenie pobiera profil SSL SslProfile01 for $AppGw i zapisuje go w $profile pliku.</span><span class="sxs-lookup"><span data-stu-id="9c9bd-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="9c9bd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c9bd-110">PARAMETERS</span></span>

### <span data-ttu-id="9c9bd-111">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c9bd-111">-ApplicationGateway</span></span>
<span data-ttu-id="9c9bd-112">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c9bd-112">The applicationGateway</span></span>

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

### <span data-ttu-id="9c9bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-113">-DefaultProfile</span></span>
<span data-ttu-id="9c9bd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c9bd-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9c9bd-115">-Name</span></span>
<span data-ttu-id="9c9bd-116">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="9c9bd-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="9c9bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9bd-117">CommonParameters</span></span>
<span data-ttu-id="9c9bd-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c9bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9bd-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c9bd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9bd-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c9bd-120">INPUTS</span></span>

### <span data-ttu-id="9c9bd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c9bd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c9bd-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c9bd-122">OUTPUTS</span></span>

### <span data-ttu-id="9c9bd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="9c9bd-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c9bd-124">NOTES</span></span>

## <span data-ttu-id="9c9bd-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c9bd-125">RELATED LINKS</span></span>

[<span data-ttu-id="9c9bd-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="9c9bd-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="9c9bd-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="9c9bd-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9c9bd-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)