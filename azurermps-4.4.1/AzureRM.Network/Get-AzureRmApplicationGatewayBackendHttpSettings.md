---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 4fd6f3b3d0cd9d2b639cfe8b0a8c01f09a148edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716682"
---
# <span data-ttu-id="4ea21-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ea21-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4ea21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ea21-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea21-103">Pobiera ustawienia HTTP zaplecza bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="4ea21-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ea21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ea21-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea21-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ea21-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea21-106">Polecenie cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings pobiera ustawienia HTTP zaplecza bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="4ea21-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="4ea21-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ea21-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea21-108">Przykład 1: Uzyskaj-Zakończ ustawienia HTTP według nazwy</span><span class="sxs-lookup"><span data-stu-id="4ea21-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4ea21-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera ustawienia HTTP o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="4ea21-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="4ea21-110">Przykład 2: uzyskiwanie zbioru ustawień protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="4ea21-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="4ea21-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera kolekcję ustawień HTTP dla $AppGw i zapisuje ustawienia w zmiennej $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="4ea21-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="4ea21-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ea21-112">PARAMETERS</span></span>

### <span data-ttu-id="4ea21-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ea21-113">-ApplicationGateway</span></span>
<span data-ttu-id="4ea21-114">Określa obiekt bramy aplikacji, który zawiera ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4ea21-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4ea21-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ea21-115">-Name</span></span>
<span data-ttu-id="4ea21-116">Określa nazwy ustawień protokołu HTTP zaplecza, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea21-116">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4ea21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea21-117">-DefaultProfile</span></span>
<span data-ttu-id="4ea21-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea21-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea21-119">CommonParameters</span></span>
<span data-ttu-id="4ea21-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea21-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea21-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea21-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ea21-122">INPUTS</span></span>

### <span data-ttu-id="4ea21-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea21-123">System.String</span></span>

## <span data-ttu-id="4ea21-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ea21-124">OUTPUTS</span></span>

### <span data-ttu-id="4ea21-125">Microsoft. Azure. Commands. Network. models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ea21-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4ea21-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ea21-126">NOTES</span></span>

## <span data-ttu-id="4ea21-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ea21-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ea21-128">Dodaj-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ea21-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4ea21-129">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ea21-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4ea21-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ea21-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4ea21-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ea21-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

