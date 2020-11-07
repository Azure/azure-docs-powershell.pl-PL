---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871187"
---
# <span data-ttu-id="7391f-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7391f-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7391f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7391f-102">SYNOPSIS</span></span>
<span data-ttu-id="7391f-103">Umożliwia usunięcie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7391f-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="7391f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7391f-104">SYNTAX</span></span>

### <span data-ttu-id="7391f-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7391f-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7391f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7391f-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7391f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7391f-107">DESCRIPTION</span></span>
<span data-ttu-id="7391f-108">Polecenie cmdlet **Remove-AzPrivateEndpointConnection** umożliwia usunięcie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7391f-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="7391f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7391f-109">EXAMPLES</span></span>

### <span data-ttu-id="7391f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7391f-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="7391f-111">W tym przykładzie zostanie usunięte połączenie prywatne punktu końcowego o nazwie MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="7391f-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="7391f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7391f-112">PARAMETERS</span></span>

### <span data-ttu-id="7391f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7391f-113">-AsJob</span></span>
<span data-ttu-id="7391f-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7391f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7391f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7391f-115">-DefaultProfile</span></span>
<span data-ttu-id="7391f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7391f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7391f-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="7391f-117">-Description</span></span>
<span data-ttu-id="7391f-118">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="7391f-118">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7391f-119">-Force</span></span>
<span data-ttu-id="7391f-120">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="7391f-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="7391f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7391f-121">-Name</span></span>
<span data-ttu-id="7391f-122">Nazwa połączenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7391f-122">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7391f-123">-PassThru</span></span>
<span data-ttu-id="7391f-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7391f-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7391f-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7391f-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7391f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7391f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7391f-127">Nazwa grupy zasobów połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="7391f-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7391f-128">-ResourceId</span></span>
<span data-ttu-id="7391f-129">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="7391f-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7391f-130">-ServiceName</span></span>
<span data-ttu-id="7391f-131">Nazwa usługi linku prywatnego z połączeniem prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7391f-131">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391f-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7391f-132">-Confirm</span></span>
<span data-ttu-id="7391f-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7391f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7391f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7391f-134">-WhatIf</span></span>
<span data-ttu-id="7391f-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7391f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7391f-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7391f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7391f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7391f-137">CommonParameters</span></span>
<span data-ttu-id="7391f-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7391f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7391f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7391f-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7391f-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7391f-140">INPUTS</span></span>

### <span data-ttu-id="7391f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7391f-141">System.String</span></span>

## <span data-ttu-id="7391f-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7391f-142">OUTPUTS</span></span>

### <span data-ttu-id="7391f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7391f-143">System.Boolean</span></span>

## <span data-ttu-id="7391f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7391f-144">NOTES</span></span>

## <span data-ttu-id="7391f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7391f-145">RELATED LINKS</span></span>

[<span data-ttu-id="7391f-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7391f-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
