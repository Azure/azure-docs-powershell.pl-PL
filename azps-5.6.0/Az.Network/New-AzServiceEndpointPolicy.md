---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953793"
---
# <span data-ttu-id="f779d-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f779d-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="f779d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f779d-102">SYNOPSIS</span></span>
<span data-ttu-id="f779d-103">Tworzy zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="f779d-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="f779d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f779d-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f779d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f779d-105">DESCRIPTION</span></span>
<span data-ttu-id="f779d-106">Polecenie **cmdlet New-AzServiceEndpointPolicy** umożliwia utworzenie zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="f779d-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="f779d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f779d-107">EXAMPLES</span></span>

### <span data-ttu-id="f779d-108">Przykład 1. Tworzenie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="f779d-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="f779d-109">To polecenie tworzy zasady punktu końcowego usługi o nazwie Zasady1 z definicjami zdefiniowanymi przez obiekt $serviceEndpointDefinition i zapisuje je w $serviceEndpointPolicy danych.</span><span class="sxs-lookup"><span data-stu-id="f779d-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="f779d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f779d-110">PARAMETERS</span></span>

### <span data-ttu-id="f779d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f779d-111">-DefaultProfile</span></span>
<span data-ttu-id="f779d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f779d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f779d-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f779d-113">-Force</span></span>
<span data-ttu-id="f779d-114">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="f779d-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f779d-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f779d-115">-Location</span></span>
<span data-ttu-id="f779d-116">.</span><span class="sxs-lookup"><span data-stu-id="f779d-116">location.</span></span>

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

### <span data-ttu-id="f779d-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f779d-117">-Name</span></span>
<span data-ttu-id="f779d-118">Nazwa podsieci</span><span class="sxs-lookup"><span data-stu-id="f779d-118">The name of the subnet</span></span>

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

### <span data-ttu-id="f779d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f779d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f779d-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f779d-120">The resource group name.</span></span>

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

### <span data-ttu-id="f779d-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f779d-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="f779d-122">Lista definicji punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="f779d-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="f779d-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f779d-123">-Confirm</span></span>
<span data-ttu-id="f779d-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f779d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f779d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f779d-125">-WhatIf</span></span>
<span data-ttu-id="f779d-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f779d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f779d-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f779d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f779d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f779d-128">CommonParameters</span></span>
<span data-ttu-id="f779d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f779d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f779d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f779d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f779d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f779d-131">INPUTS</span></span>

### <span data-ttu-id="f779d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f779d-132">System.String</span></span>

## <span data-ttu-id="f779d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f779d-133">OUTPUTS</span></span>

### <span data-ttu-id="f779d-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f779d-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f779d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f779d-135">NOTES</span></span>

## <span data-ttu-id="f779d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f779d-136">RELATED LINKS</span></span>

[<span data-ttu-id="f779d-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f779d-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f779d-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f779d-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f779d-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f779d-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
