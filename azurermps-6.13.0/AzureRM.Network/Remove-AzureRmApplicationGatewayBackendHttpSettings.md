---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 036fef4e43d8d754bd0798e72159cba367a3e2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541672"
---
# <span data-ttu-id="5b770-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b770-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="5b770-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b770-102">SYNOPSIS</span></span>
<span data-ttu-id="5b770-103">Usuwa ustawienia HTTP zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b770-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b770-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b770-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b770-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b770-105">DESCRIPTION</span></span>
<span data-ttu-id="5b770-106">Polecenie cmdlet Remove-AzureRmApplicationGatewayBackendHttpSettings usuwa ustawienia protokołu HTTP (Hypertext Transfer Protocol) z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b770-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="5b770-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b770-107">EXAMPLES</span></span>

### <span data-ttu-id="5b770-108">Przykład 1: usuwanie ustawień wewnętrznych protokołu HTTP z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5b770-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="5b770-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5b770-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5b770-110">Drugie polecenie usuwa ustawienie HTTP zaplecza o nazwie BackEndSetting02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5b770-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5b770-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b770-111">PARAMETERS</span></span>

### <span data-ttu-id="5b770-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b770-112">-ApplicationGateway</span></span>
<span data-ttu-id="5b770-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5b770-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="5b770-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b770-114">-DefaultProfile</span></span>
<span data-ttu-id="5b770-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b770-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b770-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b770-116">-Name</span></span>
<span data-ttu-id="5b770-117">Określa nazwę ustawienia HTTP zaplecza, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b770-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b770-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b770-118">CommonParameters</span></span>
<span data-ttu-id="5b770-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b770-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b770-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b770-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b770-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b770-121">INPUTS</span></span>

### <span data-ttu-id="5b770-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b770-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5b770-123">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b770-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5b770-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b770-124">OUTPUTS</span></span>

### <span data-ttu-id="5b770-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b770-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b770-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b770-126">NOTES</span></span>

## <span data-ttu-id="5b770-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b770-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b770-128">Dodaj-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b770-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="5b770-129">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b770-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="5b770-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b770-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="5b770-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b770-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

