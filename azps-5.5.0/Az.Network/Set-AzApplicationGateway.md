---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184227"
---
# <span data-ttu-id="34617-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34617-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="34617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34617-102">SYNOPSIS</span></span>
<span data-ttu-id="34617-103">Aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34617-103">Updates an application gateway.</span></span>

## <span data-ttu-id="34617-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34617-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34617-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="34617-105">DESCRIPTION</span></span>
<span data-ttu-id="34617-106">Polecenie **cmdlet Set-AzApplicationGateway** aktualizuje bramę aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34617-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="34617-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34617-107">EXAMPLES</span></span>

### <span data-ttu-id="34617-108">Przykład 1. Aktualizowanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="34617-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="34617-109">Te polecenia aktualizują bramę aplikacji przy użyciu ustawień zmiennej $AppGw i zapisuje zaktualizowaną bramę w $UpdatedAppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="34617-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="34617-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34617-110">PARAMETERS</span></span>

### <span data-ttu-id="34617-111">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34617-111">-ApplicationGateway</span></span>
<span data-ttu-id="34617-112">Określa obiekt bramy aplikacji reprezentujący stan, dla którego powinna zostać ustawiona brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34617-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="34617-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="34617-113">-AsJob</span></span>
<span data-ttu-id="34617-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34617-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34617-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34617-115">-DefaultProfile</span></span>
<span data-ttu-id="34617-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34617-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34617-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34617-117">CommonParameters</span></span>
<span data-ttu-id="34617-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34617-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34617-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34617-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34617-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34617-120">INPUTS</span></span>

### <span data-ttu-id="34617-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34617-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34617-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34617-122">OUTPUTS</span></span>

### <span data-ttu-id="34617-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34617-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34617-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34617-124">NOTES</span></span>

## <span data-ttu-id="34617-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34617-125">RELATED LINKS</span></span>

[<span data-ttu-id="34617-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34617-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


