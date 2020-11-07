---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 75cf6bac1913a2baa55a28135ba2d59f5ceaa07f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708933"
---
# <span data-ttu-id="4fa1d-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="4fa1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fa1d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa1d-103">Aktualizuje zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="4fa1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fa1d-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4fa1d-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa1d-106">Polecenie cmdlet **Set-AzServiceEndpointPolicy** Tworzenie zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4fa1d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fa1d-107">EXAMPLES</span></span>

### <span data-ttu-id="4fa1d-108">Przykład 1: Ustawianie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="4fa1d-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4fa1d-109">To polecenie aktualizuje zasady punktu końcowego usługi o nazwie Policy1 zdefiniowane przez obiekt $serviceEndpointPolicy należą do obiektu resourceName "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="4fa1d-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4fa1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fa1d-110">PARAMETERS</span></span>

### <span data-ttu-id="4fa1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa1d-111">-DefaultProfile</span></span>
<span data-ttu-id="4fa1d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa1d-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4fa1d-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4fa1d-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fa1d-115">-Confirm</span></span>
<span data-ttu-id="4fa1d-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa1d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa1d-117">-WhatIf</span></span>
<span data-ttu-id="4fa1d-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fa1d-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa1d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa1d-120">CommonParameters</span></span>
<span data-ttu-id="4fa1d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fa1d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa1d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa1d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa1d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fa1d-123">INPUTS</span></span>

### <span data-ttu-id="4fa1d-124">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4fa1d-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fa1d-125">OUTPUTS</span></span>

### <span data-ttu-id="4fa1d-126">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4fa1d-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fa1d-127">NOTES</span></span>

## <span data-ttu-id="4fa1d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fa1d-128">RELATED LINKS</span></span>

[<span data-ttu-id="4fa1d-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4fa1d-130">Nowe — AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4fa1d-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa1d-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
