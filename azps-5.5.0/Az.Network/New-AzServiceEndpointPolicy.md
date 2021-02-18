---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 4fbc1729debb7f5cf822f152107797e10b1f7ba9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240738"
---
# <span data-ttu-id="a55ca-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a55ca-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="a55ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a55ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a55ca-103">Tworzy zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="a55ca-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="a55ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a55ca-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a55ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a55ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a55ca-106">Polecenie **cmdlet New-AzServiceEndpointPolicy** umożliwia utworzenie zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="a55ca-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="a55ca-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a55ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a55ca-108">Przykład 1. Tworzenie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="a55ca-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="a55ca-109">To polecenie tworzy zasady punktu końcowego usługi o nazwie Zasady1 z definicjami zdefiniowanymi przez obiekt $serviceEndpointDefinition i zapisuje je w $serviceEndpointPolicy danych.</span><span class="sxs-lookup"><span data-stu-id="a55ca-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="a55ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a55ca-110">PARAMETERS</span></span>

### <span data-ttu-id="a55ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55ca-111">-DefaultProfile</span></span>
<span data-ttu-id="a55ca-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a55ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a55ca-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a55ca-113">-Force</span></span>
<span data-ttu-id="a55ca-114">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="a55ca-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a55ca-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a55ca-115">-Location</span></span>
<span data-ttu-id="a55ca-116">.</span><span class="sxs-lookup"><span data-stu-id="a55ca-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a55ca-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a55ca-117">-Name</span></span>
<span data-ttu-id="a55ca-118">Nazwa podsieci</span><span class="sxs-lookup"><span data-stu-id="a55ca-118">The name of the subnet</span></span>

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

### <span data-ttu-id="a55ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a55ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="a55ca-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a55ca-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a55ca-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a55ca-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="a55ca-122">Lista definicji punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="a55ca-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a55ca-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a55ca-123">-Confirm</span></span>
<span data-ttu-id="a55ca-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a55ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a55ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a55ca-125">-WhatIf</span></span>
<span data-ttu-id="a55ca-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a55ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a55ca-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a55ca-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a55ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55ca-128">CommonParameters</span></span>
<span data-ttu-id="a55ca-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a55ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55ca-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55ca-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55ca-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a55ca-131">INPUTS</span></span>

### <span data-ttu-id="a55ca-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a55ca-132">System.String</span></span>

## <span data-ttu-id="a55ca-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a55ca-133">OUTPUTS</span></span>

### <span data-ttu-id="a55ca-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a55ca-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a55ca-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a55ca-135">NOTES</span></span>

## <span data-ttu-id="a55ca-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a55ca-136">RELATED LINKS</span></span>

[<span data-ttu-id="a55ca-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a55ca-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a55ca-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a55ca-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a55ca-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a55ca-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
