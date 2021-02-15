---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189851"
---
# <span data-ttu-id="c9ecd-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c9ecd-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="c9ecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ecd-103">Pobiera ustawienia protokołu HTTP na końcu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="c9ecd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9ecd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ecd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ecd-106">Polecenie Get-AzApplicationGatewayBackendHttpSetting pobiera ustawienia protokołu HTTP na końcu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="c9ecd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9ecd-107">EXAMPLES</span></span>

### <span data-ttu-id="c9ecd-108">Przykład 1. Uzyskiwanie ustawień protokołu HTTP wt. zaw. według nazwy</span><span class="sxs-lookup"><span data-stu-id="c9ecd-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c9ecd-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w $AppGw zmienną. Drugie polecenie pobiera ustawienia protokołu HTTP o nazwie Ustawienia01 for $AppGw i zapisuje ustawienia w $Settings sieci.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="c9ecd-110">Przykład 2. Pobieranie kolekcji ustawień protokołu HTTP</span><span class="sxs-lookup"><span data-stu-id="c9ecd-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="c9ecd-111">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w $AppGw zmienną. Drugie polecenie pobiera zbiór ustawień protokołu HTTP dla protokołu $AppGw i przechowuje ustawienia w $SettingsList sieci.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="c9ecd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-112">PARAMETERS</span></span>

### <span data-ttu-id="c9ecd-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9ecd-113">-ApplicationGateway</span></span>
<span data-ttu-id="c9ecd-114">Określa obiekt bramy aplikacji zawierający ustawienia protokołu HTTP na zawęzie.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ecd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ecd-115">-DefaultProfile</span></span>
<span data-ttu-id="c9ecd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9ecd-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9ecd-117">-Name</span></span>
<span data-ttu-id="c9ecd-118">Określa nazwę ustawień protokołu HTTP zaplecza, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ecd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ecd-119">CommonParameters</span></span>
<span data-ttu-id="c9ecd-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ecd-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9ecd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ecd-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9ecd-122">INPUTS</span></span>

### <span data-ttu-id="c9ecd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9ecd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9ecd-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-124">OUTPUTS</span></span>

### <span data-ttu-id="c9ecd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c9ecd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c9ecd-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9ecd-126">NOTES</span></span>

## <span data-ttu-id="c9ecd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9ecd-127">RELATED LINKS</span></span>

[<span data-ttu-id="c9ecd-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c9ecd-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c9ecd-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c9ecd-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c9ecd-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c9ecd-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c9ecd-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c9ecd-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

