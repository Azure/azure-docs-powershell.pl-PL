---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504459"
---
# <span data-ttu-id="9a413-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a413-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="9a413-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a413-102">SYNOPSIS</span></span>
<span data-ttu-id="9a413-103">Umożliwia usunięcie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9a413-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="9a413-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a413-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a413-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a413-105">DESCRIPTION</span></span>
<span data-ttu-id="9a413-106">Polecenie cmdlet **Remove-AzPrivateEndpoint** umożliwia usunięcie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9a413-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="9a413-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a413-107">EXAMPLES</span></span>

### <span data-ttu-id="9a413-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a413-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="9a413-109">W tym przykładzie jest usuwany prywatny punkt końcowy o nazwie MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="9a413-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="9a413-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a413-110">PARAMETERS</span></span>

### <span data-ttu-id="9a413-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a413-111">-AsJob</span></span>
<span data-ttu-id="9a413-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9a413-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a413-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a413-113">-DefaultProfile</span></span>
<span data-ttu-id="9a413-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a413-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a413-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9a413-115">-Force</span></span>
<span data-ttu-id="9a413-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="9a413-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9a413-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a413-117">-Name</span></span>
<span data-ttu-id="9a413-118">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9a413-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="9a413-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a413-119">-PassThru</span></span>
<span data-ttu-id="9a413-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9a413-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a413-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9a413-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a413-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a413-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a413-123">Nazwa grupy zasobów prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9a413-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="9a413-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a413-124">-Confirm</span></span>
<span data-ttu-id="9a413-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a413-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a413-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a413-126">-WhatIf</span></span>
<span data-ttu-id="9a413-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a413-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a413-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a413-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a413-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a413-129">CommonParameters</span></span>
<span data-ttu-id="9a413-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a413-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a413-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a413-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a413-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a413-132">INPUTS</span></span>

### <span data-ttu-id="9a413-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9a413-133">System.String</span></span>

## <span data-ttu-id="9a413-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a413-134">OUTPUTS</span></span>

### <span data-ttu-id="9a413-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a413-135">System.Boolean</span></span>

## <span data-ttu-id="9a413-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a413-136">NOTES</span></span>

## <span data-ttu-id="9a413-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a413-137">RELATED LINKS</span></span>

[<span data-ttu-id="9a413-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a413-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="9a413-139">Nowe — AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a413-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)