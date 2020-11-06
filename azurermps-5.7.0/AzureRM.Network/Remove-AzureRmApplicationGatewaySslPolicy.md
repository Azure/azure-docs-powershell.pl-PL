---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 8019cb905859e6e46fbf5ae90b90d72b170c631e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553658"
---
# <span data-ttu-id="8edca-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8edca-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8edca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8edca-102">SYNOPSIS</span></span>
<span data-ttu-id="8edca-103">Usuwa zasady SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8edca-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8edca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8edca-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8edca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8edca-105">DESCRIPTION</span></span>
<span data-ttu-id="8edca-106">Polecenie cmdlet Remove-AzureRmApplicationGatewaySslPolicy usuwa zasady SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8edca-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="8edca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8edca-107">EXAMPLES</span></span>

### <span data-ttu-id="8edca-108">Przykład 1: usuwanie zasad SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8edca-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="8edca-109">To polecenie usuwa zasady SSL z bramy Application Gateway o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="8edca-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="8edca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8edca-110">PARAMETERS</span></span>

### <span data-ttu-id="8edca-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8edca-111">-ApplicationGateway</span></span>
<span data-ttu-id="8edca-112">Określa bramę aplikacji, z której to polecenie cmdlet usuwa zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="8edca-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="8edca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8edca-113">-DefaultProfile</span></span>
<span data-ttu-id="8edca-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8edca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8edca-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8edca-115">-Force</span></span>
<span data-ttu-id="8edca-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8edca-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8edca-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8edca-117">-Confirm</span></span>
<span data-ttu-id="8edca-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8edca-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8edca-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8edca-119">-WhatIf</span></span>
<span data-ttu-id="8edca-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8edca-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8edca-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8edca-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8edca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8edca-122">CommonParameters</span></span>
<span data-ttu-id="8edca-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8edca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8edca-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8edca-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8edca-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8edca-125">INPUTS</span></span>

### <span data-ttu-id="8edca-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8edca-126">System.String</span></span>

## <span data-ttu-id="8edca-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8edca-127">OUTPUTS</span></span>

### <span data-ttu-id="8edca-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8edca-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8edca-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8edca-129">NOTES</span></span>
<span data-ttu-id="8edca-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="8edca-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8edca-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8edca-131">RELATED LINKS</span></span>

[<span data-ttu-id="8edca-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8edca-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="8edca-133">Nowe — AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8edca-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="8edca-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8edca-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

