---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549319"
---
# <span data-ttu-id="8892b-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8892b-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="8892b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8892b-102">SYNOPSIS</span></span>
<span data-ttu-id="8892b-103">Modyfikuje ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8892b-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8892b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8892b-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8892b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8892b-105">DESCRIPTION</span></span>
<span data-ttu-id="8892b-106">Polecenie cmdlet **Set-AzureRmExpressRoutePort** zapisuje zmodyfikowane ExpressRoutePort na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8892b-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="8892b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8892b-107">EXAMPLES</span></span>

### <span data-ttu-id="8892b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8892b-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="8892b-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8892b-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="8892b-110">Modyfikuje stan administratora linku ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8892b-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="8892b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8892b-111">PARAMETERS</span></span>

### <span data-ttu-id="8892b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8892b-112">-AsJob</span></span>
<span data-ttu-id="8892b-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8892b-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8892b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8892b-114">-DefaultProfile</span></span>
<span data-ttu-id="8892b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8892b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8892b-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8892b-116">-ExpressRoutePort</span></span>
<span data-ttu-id="8892b-117">Obiekt ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8892b-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8892b-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8892b-118">-Confirm</span></span>
<span data-ttu-id="8892b-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8892b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8892b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8892b-120">-WhatIf</span></span>
<span data-ttu-id="8892b-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8892b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8892b-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8892b-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8892b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8892b-123">CommonParameters</span></span>
<span data-ttu-id="8892b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8892b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8892b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8892b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8892b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8892b-126">INPUTS</span></span>

### <span data-ttu-id="8892b-127">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8892b-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="8892b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8892b-128">OUTPUTS</span></span>

### <span data-ttu-id="8892b-129">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8892b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="8892b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8892b-130">NOTES</span></span>

## <span data-ttu-id="8892b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8892b-131">RELATED LINKS</span></span>
