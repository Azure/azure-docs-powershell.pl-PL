---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355873"
---
# <span data-ttu-id="06a2a-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="06a2a-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="06a2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="06a2a-103">Umożliwia usunięcie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="06a2a-103">Removes a load balancer.</span></span>

## <span data-ttu-id="06a2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06a2a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a2a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="06a2a-106">Polecenie cmdlet **Remove-AzLoadBalancer** umożliwia usunięcie modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06a2a-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="06a2a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="06a2a-108">Przykład 1: usuwanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="06a2a-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="06a2a-109">To polecenie powoduje usunięcie modułu równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="06a2a-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="06a2a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06a2a-110">PARAMETERS</span></span>

### <span data-ttu-id="06a2a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06a2a-111">-AsJob</span></span>
<span data-ttu-id="06a2a-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="06a2a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06a2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a2a-113">-DefaultProfile</span></span>
<span data-ttu-id="06a2a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06a2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a2a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06a2a-115">-Force</span></span>
<span data-ttu-id="06a2a-116">Wskazuje, że to polecenie cmdlet powoduje usunięcie modułu równoważenia obciążenia bez względu na to, czy zasoby są do niego przydzielone.</span><span class="sxs-lookup"><span data-stu-id="06a2a-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="06a2a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06a2a-117">-Name</span></span>
<span data-ttu-id="06a2a-118">Określa nazwę modułu równoważenia obciążenia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="06a2a-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a2a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06a2a-119">-PassThru</span></span>
<span data-ttu-id="06a2a-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="06a2a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06a2a-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="06a2a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06a2a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a2a-122">-ResourceGroupName</span></span>
<span data-ttu-id="06a2a-123">Określa nazwę grupy zasobów zawierającej moduł równoważenia obciążenia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="06a2a-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="06a2a-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06a2a-124">-Confirm</span></span>
<span data-ttu-id="06a2a-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06a2a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a2a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a2a-126">-WhatIf</span></span>
<span data-ttu-id="06a2a-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06a2a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a2a-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06a2a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a2a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a2a-129">CommonParameters</span></span>
<span data-ttu-id="06a2a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a2a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a2a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a2a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a2a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06a2a-132">INPUTS</span></span>

### <span data-ttu-id="06a2a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06a2a-133">System.String</span></span>

## <span data-ttu-id="06a2a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06a2a-134">OUTPUTS</span></span>

### <span data-ttu-id="06a2a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06a2a-135">System.Boolean</span></span>

## <span data-ttu-id="06a2a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06a2a-136">NOTES</span></span>

## <span data-ttu-id="06a2a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06a2a-137">RELATED LINKS</span></span>

[<span data-ttu-id="06a2a-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="06a2a-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="06a2a-139">Nowe — AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="06a2a-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="06a2a-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="06a2a-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


