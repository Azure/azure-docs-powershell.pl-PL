---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 3e1caeb5dec11188cf824bdcddf2b0de78f707c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996157"
---
# <span data-ttu-id="fa79c-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa79c-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="fa79c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa79c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa79c-103">Usuwa prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fa79c-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="fa79c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa79c-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa79c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa79c-105">DESCRIPTION</span></span>
<span data-ttu-id="fa79c-106">Polecenie **cmdlet Remove-AzPrivateEndpoint** usuwa prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fa79c-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="fa79c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa79c-107">EXAMPLES</span></span>

### <span data-ttu-id="fa79c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa79c-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="fa79c-109">W tym przykładzie usuń prywatny punkt końcowy o nazwie MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="fa79c-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="fa79c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa79c-110">PARAMETERS</span></span>

### <span data-ttu-id="fa79c-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fa79c-111">-AsJob</span></span>
<span data-ttu-id="fa79c-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fa79c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa79c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa79c-113">-DefaultProfile</span></span>
<span data-ttu-id="fa79c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa79c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa79c-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fa79c-115">-Force</span></span>
<span data-ttu-id="fa79c-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="fa79c-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="fa79c-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fa79c-117">-Name</span></span>
<span data-ttu-id="fa79c-118">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fa79c-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="fa79c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa79c-119">-PassThru</span></span>
<span data-ttu-id="fa79c-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fa79c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa79c-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fa79c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa79c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa79c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa79c-123">Nazwa grupy zasobów prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fa79c-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="fa79c-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa79c-124">-Confirm</span></span>
<span data-ttu-id="fa79c-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fa79c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa79c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa79c-126">-WhatIf</span></span>
<span data-ttu-id="fa79c-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa79c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa79c-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fa79c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa79c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa79c-129">CommonParameters</span></span>
<span data-ttu-id="fa79c-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa79c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa79c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa79c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa79c-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa79c-132">INPUTS</span></span>

### <span data-ttu-id="fa79c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fa79c-133">System.String</span></span>

## <span data-ttu-id="fa79c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa79c-134">OUTPUTS</span></span>

### <span data-ttu-id="fa79c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa79c-135">System.Boolean</span></span>

## <span data-ttu-id="fa79c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa79c-136">NOTES</span></span>

## <span data-ttu-id="fa79c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa79c-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa79c-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa79c-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="fa79c-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa79c-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)