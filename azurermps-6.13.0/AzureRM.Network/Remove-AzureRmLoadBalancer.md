---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: d725735caf7806233688e6f0bcdddb4edb0f62b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543631"
---
# <span data-ttu-id="4191f-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4191f-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="4191f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4191f-102">SYNOPSIS</span></span>
<span data-ttu-id="4191f-103">Umożliwia usunięcie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4191f-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4191f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4191f-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4191f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4191f-105">DESCRIPTION</span></span>
<span data-ttu-id="4191f-106">Polecenie cmdlet **Remove-AzureRmLoadBalancer** umożliwia usunięcie modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4191f-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="4191f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4191f-107">EXAMPLES</span></span>

### <span data-ttu-id="4191f-108">Przykład 1: usuwanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4191f-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4191f-109">To polecenie powoduje usunięcie modułu równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="4191f-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4191f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4191f-110">PARAMETERS</span></span>

### <span data-ttu-id="4191f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4191f-111">-AsJob</span></span>
<span data-ttu-id="4191f-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4191f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4191f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4191f-113">-DefaultProfile</span></span>
<span data-ttu-id="4191f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4191f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4191f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4191f-115">-Force</span></span>
<span data-ttu-id="4191f-116">Wskazuje, że to polecenie cmdlet powoduje usunięcie modułu równoważenia obciążenia bez względu na to, czy zasoby są do niego przydzielone.</span><span class="sxs-lookup"><span data-stu-id="4191f-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="4191f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4191f-117">-Name</span></span>
<span data-ttu-id="4191f-118">Określa nazwę modułu równoważenia obciążenia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4191f-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="4191f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4191f-119">-PassThru</span></span>
<span data-ttu-id="4191f-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="4191f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4191f-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4191f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4191f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4191f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4191f-123">Określa nazwę grupy zasobów zawierającej moduł równoważenia obciążenia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4191f-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="4191f-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4191f-124">-Confirm</span></span>
<span data-ttu-id="4191f-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4191f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4191f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4191f-126">-WhatIf</span></span>
<span data-ttu-id="4191f-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4191f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4191f-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4191f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4191f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4191f-129">CommonParameters</span></span>
<span data-ttu-id="4191f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4191f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4191f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4191f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4191f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4191f-132">INPUTS</span></span>

### <span data-ttu-id="4191f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4191f-133">System.String</span></span>

### <span data-ttu-id="4191f-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4191f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4191f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4191f-135">OUTPUTS</span></span>

### <span data-ttu-id="4191f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4191f-136">System.Boolean</span></span>

## <span data-ttu-id="4191f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4191f-137">NOTES</span></span>

## <span data-ttu-id="4191f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4191f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4191f-139">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4191f-139">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4191f-140">Nowe — AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4191f-140">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="4191f-141">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4191f-141">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

