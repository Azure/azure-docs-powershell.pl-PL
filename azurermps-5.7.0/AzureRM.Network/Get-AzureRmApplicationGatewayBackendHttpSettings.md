---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: f0fa24fd6a7d8ed9cf1a9806ca0a419da8c3deb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546727"
---
# <span data-ttu-id="dae35-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dae35-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="dae35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dae35-102">SYNOPSIS</span></span>
<span data-ttu-id="dae35-103">Pobiera ustawienia HTTP zaplecza bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="dae35-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dae35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dae35-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dae35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dae35-105">DESCRIPTION</span></span>
<span data-ttu-id="dae35-106">Polecenie cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings pobiera ustawienia HTTP zaplecza bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="dae35-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="dae35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dae35-107">EXAMPLES</span></span>

### <span data-ttu-id="dae35-108">Przykład 1: Uzyskaj-Zakończ ustawienia HTTP według nazwy</span><span class="sxs-lookup"><span data-stu-id="dae35-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="dae35-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera ustawienia HTTP o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="dae35-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="dae35-110">Przykład 2: uzyskiwanie zbioru ustawień protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="dae35-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="dae35-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera kolekcję ustawień HTTP dla $AppGw i zapisuje ustawienia w zmiennej $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="dae35-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="dae35-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dae35-112">PARAMETERS</span></span>

### <span data-ttu-id="dae35-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dae35-113">-ApplicationGateway</span></span>
<span data-ttu-id="dae35-114">Określa obiekt bramy aplikacji, który zawiera ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dae35-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="dae35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae35-115">-DefaultProfile</span></span>
<span data-ttu-id="dae35-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dae35-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae35-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dae35-117">-Name</span></span>
<span data-ttu-id="dae35-118">Określa nazwy ustawień protokołu HTTP zaplecza, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae35-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dae35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae35-119">CommonParameters</span></span>
<span data-ttu-id="dae35-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae35-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae35-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae35-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dae35-122">INPUTS</span></span>

### <span data-ttu-id="dae35-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dae35-123">System.String</span></span>

## <span data-ttu-id="dae35-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dae35-124">OUTPUTS</span></span>

### <span data-ttu-id="dae35-125">Microsoft. Azure. Commands. Network. models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dae35-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="dae35-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dae35-126">NOTES</span></span>

## <span data-ttu-id="dae35-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dae35-127">RELATED LINKS</span></span>

[<span data-ttu-id="dae35-128">Dodaj-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dae35-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="dae35-129">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dae35-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="dae35-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dae35-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="dae35-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dae35-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

