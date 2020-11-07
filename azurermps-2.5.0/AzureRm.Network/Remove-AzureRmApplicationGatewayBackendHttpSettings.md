---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 71ce0dd8d4c5988dfc5cd4226ee76dcec46042ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898270"
---
# <span data-ttu-id="2fe33-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fe33-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2fe33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fe33-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe33-103">Usuwa ustawienia HTTP zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2fe33-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fe33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fe33-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2fe33-105">DESCRIPTION</span></span>
<span data-ttu-id="2fe33-106">Polecenie cmdlet Remove-AzureRmApplicationGatewayBackendHttpSettings usuwa ustawienia protokołu HTTP (Hypertext Transfer Protocol) z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe33-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="2fe33-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fe33-107">EXAMPLES</span></span>

### <span data-ttu-id="2fe33-108">Przykład 1: usuwanie ustawień wewnętrznych protokołu HTTP z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2fe33-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="2fe33-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2fe33-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2fe33-110">Drugie polecenie usuwa ustawienie HTTP zaplecza o nazwie BackEndSetting02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2fe33-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2fe33-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fe33-111">PARAMETERS</span></span>

### <span data-ttu-id="2fe33-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fe33-112">-ApplicationGateway</span></span>
<span data-ttu-id="2fe33-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2fe33-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="2fe33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe33-114">-DefaultProfile</span></span>
<span data-ttu-id="2fe33-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe33-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fe33-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fe33-116">-Name</span></span>
<span data-ttu-id="2fe33-117">Określa nazwę ustawienia HTTP zaplecza, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fe33-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe33-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe33-118">CommonParameters</span></span>
<span data-ttu-id="2fe33-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe33-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe33-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe33-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe33-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fe33-121">INPUTS</span></span>

### <span data-ttu-id="2fe33-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2fe33-122">System.String</span></span>

## <span data-ttu-id="2fe33-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fe33-123">OUTPUTS</span></span>

### <span data-ttu-id="2fe33-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fe33-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fe33-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fe33-125">NOTES</span></span>

## <span data-ttu-id="2fe33-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fe33-126">RELATED LINKS</span></span>

[<span data-ttu-id="2fe33-127">Dodaj-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fe33-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="2fe33-128">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fe33-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="2fe33-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fe33-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="2fe33-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fe33-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

