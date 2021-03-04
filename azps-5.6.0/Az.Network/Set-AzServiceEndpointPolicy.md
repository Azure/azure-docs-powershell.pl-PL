---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008705"
---
# <span data-ttu-id="5655b-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="5655b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5655b-102">SYNOPSIS</span></span>
<span data-ttu-id="5655b-103">Aktualizuje zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="5655b-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="5655b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5655b-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5655b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5655b-105">DESCRIPTION</span></span>
<span data-ttu-id="5655b-106">Polecenie **cmdlet Set-AzServiceEndpointPolicy** umożliwia utworzenie zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="5655b-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="5655b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5655b-107">EXAMPLES</span></span>

### <span data-ttu-id="5655b-108">Przykład 1. Ustawianie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="5655b-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="5655b-109">To polecenie aktualizuje zasady punktu końcowego usługi o nazwie Zasady1 zdefiniowane przez obiekt, $serviceEndpointPolicy należą do grupy zasobów "grupa zasobów1".</span><span class="sxs-lookup"><span data-stu-id="5655b-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="5655b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5655b-110">PARAMETERS</span></span>

### <span data-ttu-id="5655b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5655b-111">-DefaultProfile</span></span>
<span data-ttu-id="5655b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5655b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5655b-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5655b-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5655b-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5655b-115">-Confirm</span></span>
<span data-ttu-id="5655b-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5655b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5655b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5655b-117">-WhatIf</span></span>
<span data-ttu-id="5655b-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5655b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5655b-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5655b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5655b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5655b-120">CommonParameters</span></span>
<span data-ttu-id="5655b-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5655b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5655b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5655b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5655b-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5655b-123">INPUTS</span></span>

### <span data-ttu-id="5655b-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5655b-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5655b-125">OUTPUTS</span></span>

### <span data-ttu-id="5655b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5655b-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5655b-127">NOTES</span></span>

## <span data-ttu-id="5655b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5655b-128">RELATED LINKS</span></span>

[<span data-ttu-id="5655b-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="5655b-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="5655b-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5655b-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
