---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189107"
---
# <span data-ttu-id="ef8b0-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ef8b0-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="ef8b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8b0-103">Usuwa przestrzeń nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="ef8b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef8b0-104">SYNTAX</span></span>

### <span data-ttu-id="ef8b0-105">NamespacePropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ef8b0-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8b0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef8b0-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8b0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef8b0-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef8b0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef8b0-108">DESCRIPTION</span></span>
<span data-ttu-id="ef8b0-109">Polecenie **cmdlet Remove-AzServiceBusNamespace** usuwa przestrzeń nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="ef8b0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef8b0-110">EXAMPLES</span></span>

### <span data-ttu-id="ef8b0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef8b0-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="ef8b0-112">Usuwa przestrzeń nazw autobusu usług `SB-Example1` z określonej grupy `Default-ServiceBus-WestUS` zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="ef8b0-113">Przykład 2.1 — InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="ef8b0-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="ef8b0-114">Usuwa przestrzeń nazw autobusu usług zapewnianą za pośrednictwem $inputobject.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="ef8b0-115">Przykład 2.2 — InputObject — używanie funkcji pipingu:</span><span class="sxs-lookup"><span data-stu-id="ef8b0-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="ef8b0-116">Usuwa przestrzeń nazw autobusu usług przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="ef8b0-117">Przykład 3. ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef8b0-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="ef8b0-118">Usuwa przestrzeń nazw typu service bus zapewnianą za pośrednictwem ARM identyfikatora w $resourceid dla parametru -ResourceId lub za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="ef8b0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef8b0-119">PARAMETERS</span></span>

### <span data-ttu-id="ef8b0-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ef8b0-120">-AsJob</span></span>
<span data-ttu-id="ef8b0-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ef8b0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef8b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef8b0-122">-DefaultProfile</span></span>
<span data-ttu-id="ef8b0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef8b0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef8b0-124">-InputObject</span></span>
<span data-ttu-id="ef8b0-125">Obiekt przestrzeni nazw typu service bus</span><span class="sxs-lookup"><span data-stu-id="ef8b0-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8b0-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ef8b0-126">-Name</span></span>
<span data-ttu-id="ef8b0-127">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8b0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef8b0-128">-PassThru</span></span>
<span data-ttu-id="ef8b0-129">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ef8b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef8b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="ef8b0-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ef8b0-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8b0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef8b0-132">-ResourceId</span></span>
<span data-ttu-id="ef8b0-133">Identyfikator zasobu przestrzeni nazw autobusu usług</span><span class="sxs-lookup"><span data-stu-id="ef8b0-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8b0-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef8b0-134">-Confirm</span></span>
<span data-ttu-id="ef8b0-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef8b0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef8b0-136">-WhatIf</span></span>
<span data-ttu-id="ef8b0-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef8b0-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef8b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8b0-139">CommonParameters</span></span>
<span data-ttu-id="ef8b0-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef8b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef8b0-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef8b0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8b0-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef8b0-142">INPUTS</span></span>

### <span data-ttu-id="ef8b0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ef8b0-143">System.String</span></span>

### <span data-ttu-id="ef8b0-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ef8b0-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ef8b0-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef8b0-145">OUTPUTS</span></span>

### <span data-ttu-id="ef8b0-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef8b0-146">System.Boolean</span></span>

## <span data-ttu-id="ef8b0-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef8b0-147">NOTES</span></span>

## <span data-ttu-id="ef8b0-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef8b0-148">RELATED LINKS</span></span>
