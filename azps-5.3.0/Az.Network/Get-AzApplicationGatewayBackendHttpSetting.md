---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499589"
---
# <span data-ttu-id="71d96-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="71d96-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="71d96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71d96-102">SYNOPSIS</span></span>
<span data-ttu-id="71d96-103">Pobiera ustawienia HTTP zaplecza bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="71d96-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="71d96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71d96-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d96-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71d96-105">DESCRIPTION</span></span>
<span data-ttu-id="71d96-106">Polecenie cmdlet Get-AzApplicationGatewayBackendHttpSetting pobiera ustawienia HTTP zaplecza bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="71d96-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="71d96-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71d96-107">EXAMPLES</span></span>

### <span data-ttu-id="71d96-108">Przykład 1: Uzyskaj-Zakończ ustawienia HTTP według nazwy</span><span class="sxs-lookup"><span data-stu-id="71d96-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="71d96-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera ustawienia HTTP o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="71d96-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="71d96-110">Przykład 2: uzyskiwanie zbioru ustawień protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="71d96-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="71d96-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera kolekcję ustawień HTTP dla $AppGw i zapisuje ustawienia w zmiennej $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="71d96-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="71d96-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71d96-112">PARAMETERS</span></span>

### <span data-ttu-id="71d96-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71d96-113">-ApplicationGateway</span></span>
<span data-ttu-id="71d96-114">Określa obiekt bramy aplikacji, który zawiera ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="71d96-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="71d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d96-115">-DefaultProfile</span></span>
<span data-ttu-id="71d96-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71d96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71d96-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71d96-117">-Name</span></span>
<span data-ttu-id="71d96-118">Określa nazwy ustawień protokołu HTTP zaplecza, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71d96-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="71d96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d96-119">CommonParameters</span></span>
<span data-ttu-id="71d96-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d96-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71d96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d96-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71d96-122">INPUTS</span></span>

### <span data-ttu-id="71d96-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71d96-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="71d96-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71d96-124">OUTPUTS</span></span>

### <span data-ttu-id="71d96-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="71d96-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="71d96-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71d96-126">NOTES</span></span>

## <span data-ttu-id="71d96-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71d96-127">RELATED LINKS</span></span>

[<span data-ttu-id="71d96-128">Dodaj-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="71d96-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="71d96-129">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="71d96-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="71d96-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="71d96-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="71d96-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="71d96-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

